# Painel de Aeroportos da América Latina (Versão 48.2)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos da América Latina.

## 🚀 O que há de novo na Versão 48.2
* **UX Aprimorada com `<details>`:** O código técnico bruto do TAF agora fica oculto por padrão dentro de uma gaveta colapsável, deixando o design dos cartões limpo e focado no resumo descritivo (`tafInterpret`).
* **Manutenção de Versão Frontend-Only:** Atualização incremento mantida no frontend sem necessidade de mexer no Cloudflare Worker.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediano as requisições assíncronas à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a versão 48.2.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";