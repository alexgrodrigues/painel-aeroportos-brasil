# Painel de Aeroportos da América Latina (Versão 48.3)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos da América Latina.

## 🚀 O que há de novo na Versão 48.3
* **Identidade Visual Aprimorada:** Introdução de um sistema visual especializado com cores, ícones e rótulos semânticos claros para cada bloco de dados:
  * **📡 METAR:** Azul/Ciano (focado em observação atual).
  * **💡 Interpretação:** Verde-azulado (focado em insights de leitura humana).
  * **⏱️ TAF Bruto:** Roxo/Violeta (focado em projeção futura, guardado de forma limpa em `<details>`).
* **Estilização do Título:** Adicionado o ícone do jato (✈️) prestando homenagem ao conceito do Gripen da FAB ao lado do título principal.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediano as requisições assíncronas à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a versão 48.3.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";