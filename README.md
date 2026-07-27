# Painel de Aeroportos da América Latina (Versão 49.7)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, hubs internacionais e bases aéreas da América Latina.

## 🚀 O que há de novo na Versão 49.7
* **Sincronização de Estado de Filtros:** Implementada a função auxiliar `syncActiveButtons()` para garantir que a interface e as classes CSS de destaque (`active`) dos botões de país e categoria estejam sempre perfeitamente alinhadas com o estado atual da aplicação.
* **Micro-legenda de Condições:** Adicionada uma barra compacta e elegante no topo do painel com indicadores coloridos explicativos para os estados de voo (**VFR**, **MVFR**, **IFR** e **LIFR**), melhorando a acessibilidade e a experiência do usuário.
* **Inclusão de Bases Aéreas Militares (49.4 a 49.6):** Incorporação de bases aéreas estratégicas e exclusivas da Força Aérea Brasileira (FAB) com estações meteorológicas próprias, como Canoas (SBCO), Santa Maria (SBSM), Santa Cruz (SBSC) e Afonsos (SBAF).
* **Interpretação Avançada de TAF por Tokens (49.1 e 49.2):** Sistema de leitura automatizada inteligente baseado em tokens isolados e qualificadores estritos, eliminando falsos positivos na identificação de fenômenos adversos.
* **Tratamento de Pressão QNH e Fallbacks (49):** Conversão inteligente e segura de pressões altimétricas (inHg para hPa) e ampla redundância de chaves para captura de dados da API de meteorologia.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediando as requisições assíncronas à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a **Versão 49.7**.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";