# Painel de Aeroportos Globais & Bases Aéreas (v75.0)

Sistema avançado de monitoramento meteorológico aeronáutico (METAR/TAF) voltado para aviação comercial, unidades militares da FAB e estações meteorológicas em **ilhas estratégicas do Oceano Atlântico** (como Fernando de Noronha, Açores e Cabo Verde).

## 🚀 Principais Atualizações da Versão 75.0
- **Limpeza Arquitetural (*Zero Dívida Técnica*):** A lógica de classificação de bases aéreas e regiões brasileiras foi totalmente descentralizada do front-end. O backend agora injeta propriedades nativas (`isAirBase: true/false` e `brazilRegion`), tornando o código do painel limpo, modular e altamente escalável.
- **Ilhas Estratégicas do Atlântico:** Adicionadas estações essenciais para monitoramento oceânico e transatlântico:
  - **SBFN** (Fernando de Noronha, Brasil)
  - **LPAZ** (Santa Maria - Açores, Portugal)
  - **LPPD** (Ponta Delgada - Açores, Portugal)
  - **GVAC** (Boa Vista, Cabo Verde)
  - **GVNP** (São Vicente, Cabo Verde)
- **Padronização Oficial:** Nomes de instalações civis/militares unificados e validação robusta de cache e tratamento de cold starts.

---

## 📂 Estrutura de Arquivos

1. **`worker.js`** (Backend - Cloudflare Worker)
   - Executa buscas assíncronas em lotes na API oficial de meteorologia.
   - Processa METAR e TAF gerando descrições legíveis em linguagem natural.
   - Armazena dados no Cloudflare KV (`WEATHER_KV`) com TTL otimizado de 15 minutos e suporte completo a CORS.

2. **`index.html`** (Frontend)
   - Interface web responsiva em tema escuro profissional (`Dark Theme`).
   - Cards dinâmicos com categorias visuais de voo (`VFR`, `MVFR`, `IFR`, `LIFR`).
   - Modais interativos contendo frequências oficiais (TWR, GND, ATIS) e dimensões das pistas.

---

## 🛠️ Como Implantar

1. **Cloudflare Worker:** Cole o código atualizado em `worker.js`, configure o binding do KV Namespace (`WEATHER_KV`) e publique.
2. **Frontend:** Atualize a constante `WORKER_URL` no arquivo `index.html` com a nova URL do seu Worker e hospede estaticamente.