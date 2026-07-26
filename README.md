# 🛫 Painel de Aeroportos da América Latina

Painel em tempo real para monitoramento de condições meteorológicas de voo (**METAR** e **TAF**) de aeroportos selecionados na América Latina, estruturado com alta resiliência e suporte a cache dinâmico via Cloudflare Worker.

---

## 🏗️ Arquitetura do Sistema

O projeto é dividido em duas camadas principais:

1. **Frontend (GitHub Pages):** 
   - Interface limpa baseada em componentes web modernos (HTML5, CSS3, JavaScript Vanilla).
   - Filtros dinâmicos por país/região, categoria de voo (VFR, MVFR, IFR, LIFR) e busca textual por código ICAO ou cidade.
   - Atualização automática em segundo plano a cada 5 minutos.

2. **Backend (Cloudflare Worker):**
   - Atua como um proxy seguro para a API oficial de meteorologia aeronáutica (`aviationweather.gov`).
   - Realiza o particionamento inteligente em lotes de requisições paralelas para contornar limites de tamanho de URL da origem.
   - Faz o mapeamento rigoroso utilizando chaves de identificação robustas (`icaoId`, `stationId`).
   - Aplica degradação graciosa: se o provedor externo retornar valores vazios ou instáveis, o painel mantém os metadados estruturais intactos, evitando quebras de interface.

---

## 🚀 Como Executar Localmente

1. Clone o repositório em sua máquina:
   ```bash
   git clone [https://github.com/alexgrodrigues/painel-aeroportos-brasil.git](https://github.com/alexgrodrigues/painel-aeroportos-brasil.git)