# Painel de Aeroportos Globais & Bases Aéreas

Sistema completo de monitoramento meteorológico aeronáutico (METAR/TAF) para aeroportos e bases aéreas do Brasil, América Latina, América do Norte, Europa, Ásia e África.

## 🚀 Novidades desta Versão (v73.0)
- **Botão Discreto de Bases Aéreas por Região:** Adicionado um menu dropdown minimalista junto à barra de pesquisa e atualização que permite selecionar instantaneamente as bases aéreas e aeródromos militares do Brasil filtrados por região (Norte, Nordeste, Centro-Oeste, Sudeste e Sul).
- **Design Minimalista (*Ghost Button*):** O botão se integra perfeitamente ao layout escuro (`#0f172a`), evitando poluição visual e mantendo a interface limpa.
- **Tratamento de Cache Robusto:** Integração completa com Cloudflare Workers e KV storage, além de fallback local no frontend (`airportCache`) para mitigar atrasos na primeira requisição (*Cold Cache*).

---

## 📂 Estrutura de Arquivos

1. **`worker.js`** (Backend - Cloudflare Worker)
   - Realiza consultas em lotes à API do AviationWeather.gov.
   - Faz o parser inteligente de METAR e TAF.
   - Gerencia o armazenamento em cache no Cloudflare KV (`WEATHER_KV`) com TTL de 15 minutos (`900` segundos) e cabeçalhos CORS restritos.

2. **`index.html`** (Frontend)
   - Interface web responsiva em tema escuro profissional (`Dark Theme`).
   - Cards dinâmicos com categorias de voo (`VFR`, `MVFR`, `IFR`, `LIFR`).
   - Modais interativos com frequências de comunicação (Torre, Solo, ATIS) e dimensões de pistas.
   - Sistema de filtragem por região global, categoria de voo e o novo seletor discreto de bases aéreas por região brasileira.

---

## 🛠️ Como Executar e Implantar

### 1. Backend (Cloudflare Worker)
1. Acesse o painel da [Cloudflare Workers](https://workers.cloudflare.com/).
2. Crie ou atualize um Worker com o código fornecido em `worker.js`.
3. Configure o binding do **KV Namespace** com o nome exato: `WEATHER_KV`.
4. Publique o worker e copie a URL gerada (ex: `https://seu-worker.seu-subdominio.workers.dev`).

### 2. Frontend (`index.html`)
1. Abra o arquivo `index.html` em um editor de texto.
2. Certifique-se de que a constante `WORKER_URL` aponta para a URL do seu Cloudflare Worker:
   ```javascript
   const WORKER_URL = "https://seu-worker.seu-subdominio.workers.dev";
   ```
3. Hospede o arquivo estático em serviços como Cloudflare Pages, GitHub Pages ou Netlify.
