# Painel de Aeroportos da América Latina (Versão 49.8)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, hubs internacionais e bases aéreas da América Latina.

## 🚀 O que há de novo na Versão 49.8
* **Correção no Mapeamento do METAR:** Ajustado o script de renderização no frontend para garantir que os dados brutos de METAR e os parâmetros de vento, pressão, temperatura e ponto de orvalho sejam exibidos perfeitamente em todos os cartões.
* **Sincronização de Estado de Filtros:** Implementação da função auxiliar `syncActiveButtons()` para manter o feedback visual dos botões de país e categoria perfeitamente alinhados com o estado ativo da interface.
* **Micro-legenda de Condições:** Barra compacta no topo com indicadores coloridos explicativos para os estados de voo (**VFR**, **MVFR**, **IFR** e **LIFR**), melhorando a experiência visual.
* **Inclusão de Bases Aéreas Militares (49.4 a 49.6):** Incorporação de bases estratégicas da Força Aérea Brasileira (FAB), como Canoas (SBCO), Santa Maria (SBSM), Santa Cruz (SBSC) e Afonsos (SBAF).
* **Interpretação Avançada de TAF por Tokens:** Leitura automatizada baseada em tokens isolados e qualificadores estritos, eliminando falsos positivos na identificação de fenômenos adversos.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers intermediando as requisições assíncronas à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a **Versão 49.8**.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";