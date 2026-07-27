# Painel de Aeroportos da América Latina (Versão 49.6)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, hubs internacionais e bases aéreas da América Latina.

## 🚀 O que há de novo nas Versões 49.x
* **Feedback Visual de Filtros (Versão 49.6):** Correção do comportamento dos botões de filtro de país e categorias. Agora, o botão ativo recebe instantaneamente o destaque visual correto (classe `active`), permitindo identificar com clareza qual filtro está aplicado na tela.
* **Inclusão de Bases Aéreas Militares (Versões 49.4 a 49.6):** Adicionadas bases operacionais estratégicas e exclusivas da Força Aérea Brasileira (FAB) que possuem estações meteorológicas próprias, como a Base Aérea de Canoas (SBCO), Base Aérea de Santa Maria (SBSM), Base Aérea de Santa Cruz (SBSC), Base Aérea dos Afonsos (SBAF), entre outras.
* **Interpretação Avançada de TAF por Tokens (Versões 49.1 e 49.2):** O parser de previsões meteorológicas foi totalmente reescrito para analisar tokens isolados e termos qualificados, eliminando falsos positivos indesejados (especialmente no tratamento do código restrito de névoa úmida `BR`).
* **Tratamento Robusto de Pressão QNH e Fallbacks de METAR (Versão 49):** Implementada verificação de faixa inteligente para conversão de pressões altimétricas (inHg para hPa) e ampliação de chaves de busca para garantir 100% de captura de dados brutos da API de meteorologia.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediando as requisições assíncronas de alta performance à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a **Versão 49.6**.
2. Garanta que a constante de conexão aponte para o Cloudflare Worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";