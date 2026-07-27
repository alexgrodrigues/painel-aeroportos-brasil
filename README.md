# Painel de Aeroportos da América Latina e EUA (Versão 51)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 O que há de novo na Versão 51
* **Suporte a Códigos IATA na Pesquisa e Exibição:** Adicionados os códigos de 3 letras (IATA) para todos os aeroportos, bases e hubs do painel. Agora é possível buscar diretamente por códigos como `GRU`, `MIA`, `JFK`, além de visualizá-los diretamente nos títulos dos cartões.
* **Filtro Dedicado para os EUA (`🇺🇸 EUA`):** Botão de filtro rápido no cabeçalho do frontend para isolar o monitoramento dos aeroportos norte-americanos.
* **Sincronização de Estado de Filtros:** Manutenção da consistência visual automática dos botões ativos de categorias e países.
* **Micro-legenda de Condições e Parser Blindado:** Indicadores visuais intuitivos no topo e motor de interpretação de TAF baseado em tokens.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o script do seu Cloudflare Worker com o array contendo os códigos IATA da **Versão 51**.
2. Atualize o arquivo `index.html` com o código completo da **Versão 51**.
3. Faça o commit e publique as atualizações no repositório do GitHub.