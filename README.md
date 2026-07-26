# 🛫 Painel de Aeroportos da América Latina (Versão 47)

Painel em tempo real para monitoramento de condições meteorológicas de voo (**METAR** e **TAF**) de aeroportos selecionados na América Latina, estruturado com alta resiliência, tratamento otimizado de parsing de dados e integração via Cloudflare Worker.

---

## 🏗️ Arquitetura do Sistema

1. **Frontend (GitHub Pages):** 
   - Interface limpa e responsiva (HTML5, CSS3, JavaScript Vanilla).
   - Filtros dinâmicos por região/país, condições de voo (VFR, MVFR, IFR, LIFR) e busca textual por código ICAO ou cidade.
   - Atualização automática programada a cada 5 minutos.

2. **Backend (Cloudflare Worker):**
   - Proxy seguro integrado à API de meteorologia aeronáutica da origem.
   - Particionamento inteligente de requisições paralelas em blocos para evitar truncamento de dados.
   - Mapeamento rigoroso e unificado de chaves de identificação (`icaoId`, `stationId`, `rawTaf`) assegurando a exibição completa para todos os aeroportos da grade.

---

## 🚀 Como Executar Localmente

1. Clone o repositório em sua máquina:
   ```bash
   git clone [https://github.com/alexgrodrigues/painel-aeroportos-brasil.git](https://github.com/alexgrodrigues/painel-aeroportos-brasil.git)