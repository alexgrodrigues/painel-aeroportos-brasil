# Painel de Aeroportos da América Latina (Versão 48)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos da América Latina.

## 🚀 O que há de novo na Versão 48
* **Interpretação de TAF Implementada:** Adicionado mecanismo no backend (Cloudflare Worker) para decodificar e traduzir termos e condições dos boletins TAF (como CAVOK, TEMPO, BECMG, chuvas e tempestades) para linguagem clara.
* **Exibição Visual Dinâmica:** Inclusão de um bloco estilizado de "💡 Interpretação" abaixo dos dados de TAF em cada cartão de aeroporto.
* **Correção de Parser do TAF:** Ajustado o mapeamento e extração do payload JSON do Aviation Weather Center (`rawTAF` / `rawTaf`) para garantir que os dados das previsões apareçam consistentemente.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediano as requisições assíncronas à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a versão desejada.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";