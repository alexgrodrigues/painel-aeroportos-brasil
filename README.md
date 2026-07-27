# Painel de Aeroportos da América Latina e EUA (Versão 57)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 Histórico de Atualizações Recentes (Versões 49.9 a 57)

* **Versão 57 (Correção Cirúrgica no Frontend de METAR):** Blindagem completa do script de renderização no frontend para garantir exibição contínua e estável dos relatórios METAR e TAF em todos os aeroportos da rede (como `SBGL`, `SBGR`, `SBBR`, etc.), independentemente de variações de chaves da API.
* **Versão 53 a 56 (Interface e Módulos):**
  * **Ícones de Bandeiras nos Filtros:** Adicionadas bandeiras em formato emoji (`🇧🇷`, `🇺🇸`, `🇦🇷`, `🇨🇱`, `🇲🇽`, `🇵🇦`, `🇨🇷`) em cada botão de filtro por país.
  * **Modularização do Cabeçalho (`renderCardHeader`):** Extração da montagem do cabeçalho do aeroporto para uma função auxiliar isolada.
  * **Fallback Humanizado para IATA:** Exibição do texto *"sem IATA"* em aeroportos e bases sem código de 3 letras associado, preservando a harmonia do layout.
* **Versão 50 a 52 (Expansão Geográfica e Arquitetura):**
  * **Hubs dos EUA:** Inclusão dos 5 principais aeroportos mais frequentados por voos vindos do Brasil (`KMIA`, `KMCO`, `KJFK`, `KATL`, `KIAH`) e botão de filtro rápido dedicado para os EUA (`🇺🇸 EUA`).
  * **Códigos IATA na Pesquisa e Exibição:** Suporte a buscas por códigos de 3 letras e organização visual limpa em linha de apoio (`ICAO • IATA`) abaixo do nome do aeroporto.
  * **Desacoplamento de Filtros:** Separação estrita entre a propriedade `country` (para países reais) e a propriedade `group` (reservada para agrupamentos genéricos como `'OTHER'`).

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com a versão mais recente contendo o parser blindado e o design modularizado.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";