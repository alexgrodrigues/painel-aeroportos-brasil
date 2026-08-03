# Painel de Aeroportos Globais & Bases Aéreas

Sistema avançado de monitoramento meteorológico aeronáutico (METAR/TAF) para aeroportos comerciais e bases aéreas da Força Aérea Brasileira (FAB), América Latina, América do Norte, Europa, Ásia e África.

## 🚀 Novidades da Versão Atual (v74.0)
- **Curadoria e Padronização Oficial:** Os nomes das instalações mistas (civis e militares) foram rigorosamente padronizados para garantir consistência operacional e evitar duplicidades (ex: *Aeroporto Internacional de Brasília / Base Aérea*)[cite: 1, 2].
- **Botão Discreto de Bases Aéreas por Região:** Menu dropdown minimalista localizado estrategicamente na barra superior que permite filtrar instantaneamente as bases aéreas e unidades militares da FAB por região do Brasil (*Norte, Nordeste, Centro-Oeste, Sudeste e Sul*).
- **Design Minimalista (*Ghost Button*):** Integração visual limpa com o tema escuro profissional (`#0f172a`), evitando poluição de interface[cite: 2].
- **Mitigação de Cold Cache:** Mecanismo integrado de fallback local (`airportCache`) no frontend e tratamento otimizado de cache no Cloudflare Workers para garantir estabilidade mesmo no primeiro acesso[cite: 1, 2].

---

## 📂 Estrutura de Arquivos

1. **`worker.js`** (Backend - Cloudflare Worker)
   - Realiza requisições em lotes assíncronos à API oficial de meteorologia.
   - Faz o parser inteligente de METAR e TAF para tradução em linguagem natural.
   - Gerencia o armazenamento em cache no Cloudflare KV (`WEATHER_KV`) com TTL otimizado de 15 minutos (`900` segundos) e restrições de CORS[cite: 1].

2. **`index.html`** (Frontend)
   - Interface web responsiva em tema escuro profissional (`Dark Theme`)[cite: 2].
   - Cards dinâmicos classificados por categorias de voo (`VFR`, `MVFR`, `IFR`, `LIFR`)[cite: 2].
   - Modais interativos com frequências oficiais de comunicação (Torre, Solo, ATIS) e dimensões das pistas de pouso e decolagem[cite: 2].
   - Sistema multi-filtros por região global, categoria meteorológica e filtro regional dedicado para bases aéreas brasileiras[cite: 2].

---

## 🛠️ Como Executar e Implantar

### 1. Backend (Cloudflare Worker)
1. Acesse o painel da [Cloudflare Workers](https://workers.cloudflare.com/)[cite: 1].
2. Crie ou atualize um Worker utilizando o código fornecido em `worker.js`[cite: 1].
3. Configure o binding do **KV Namespace** com o nome exato: `WEATHER_KV`[cite: 1].
4. Publique o projeto e copie a URL de produção gerada (ex: `https://seu-worker.seu-subdominio.workers.dev`)[cite: 1, 2].

### 2. Frontend (`index.html`)
1. Abra o arquivo `index.html` em seu editor de código preferido[cite: 2].
2. Certifique-se de que a constante `WORKER_URL` aponta para a URL do seu Cloudflare Worker recém-implantado[cite: 2]:
   ```javascript
   const WORKER_URL = "[https://seu-worker.seu-subdominio.workers.dev](https://seu-worker.seu-subdominio.workers.dev)";