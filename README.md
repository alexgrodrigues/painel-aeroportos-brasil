# Painel de Aeroportos da América Latina e EUA (Versão 50)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 O que há de novo na Versão 50
* **Inclusão dos Principais Hubs dos EUA:** Adicionados os 5 aeroportos norte-americanos que mais recebem voos de passageiros do Brasil: Miami (KMIA), Orlando (KMCO), Nova York / JFK (KJFK), Atlanta (KATL) e Houston (KIAH).
* **Filtro Dedicado para os EUA (`🇺🇸 EUA`):** Implementado o botão de filtro rápido no cabeçalho do frontend para isolar e monitorar exclusivamente o grupo de aeroportos norte-americanos.
* **Sincronização de Estado de Filtros:** Manutenção da consistência visual automática dos botões de categorias e países ativos na interface.
* **Micro-legenda de Condições e Parser Blindado:** Indicadores visuais intuitivos no topo e motor de interpretação de TAF baseado em tokens.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o script do seu Cloudflare Worker com o array ampliado contendo os hubs dos EUA (`US`).
2. Atualize o arquivo `index.html` com o código completo da **Versão 50**.
3. Faça o commit e publique as atualizações no repositório do GitHub.