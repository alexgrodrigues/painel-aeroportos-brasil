# Painel de Aeroportos da América Latina (Versão 48.1)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos da América Latina.

## 🚀 O que há de novo na Versão 48.1
* **Priorização da Interpretação do TAF:** O resumo amigável e traduzido das previsões (`tafInterpret`) agora aparece em destaque logo acima do código bruto do TAF em cada cartão de aeroporto.
* **Layout Aprimorado:** Melhor legibilidade e hierarquia visual na seção de previsões meteorológicas.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediano as requisições assíncronas à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a versão desejada.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";