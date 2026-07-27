# Painel de Aeroportos da América Latina e EUA (Versão 52)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 O que há de novo na Versão 52
* **Desacoplamento de Filtros (País vs Grupo):** Refatoração da lógica de filtragem para utilizar estritamente a propriedade `country` nas consultas de países reais e reservar a propriedade `group` apenas para agrupamentos genéricos (como `'OTHER'`), mantendo o código limpo e intuitivo.
* **Layout de Cartões Otimizado:** O código IATA foi reorganizado para uma linha limpa de apoio abaixo do nome (`ICAO • IATA`), reduzindo o ruído visual em nomes de aeroportos longos.
* **Pesquisa Abrangente:** Suporte completo para busca instantânea por códigos de 3 letras (IATA) ou 4 letras (ICAO), além de cidades e nomes.
* **Filtros Dedicados:** Inclusão do botão de acesso rápido para os EUA (`🇺🇸 EUA`) e demais regiões.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o seu Cloudflare Worker para a **Versão 52**.
2. Atualize o arquivo `index.html` com o código da **Versão 52**.
3. Faça o commit e publique as atualizações no repositório do GitHub.