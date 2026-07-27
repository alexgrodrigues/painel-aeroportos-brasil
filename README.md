# Painel de Aeroportos da América Latina e EUA (Versão 53)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 O que há de novo na Versão 53
* **Ícones de Bandeiras nos Filtros de País:** Adicionadas bandeiras em formato emoji (`🇧🇷`, `🇺🇸`, `🇦🇷`, `🇨🇱`, `🇲🇽`, `🇵🇦`, `🇨🇷`) em cada botão de filtro de país, tornando a identificação visual muito mais rápida e elegante.
* **Modularização do Cabeçalho do Cartão (`renderCardHeader`):** Extração da lógica de montagem do cabeçalho de cada aeroporto para uma função isolada, limpando o código principal de renderização e garantindo alta manutenibilidade.
* **Desacoplamento de Filtros (País vs Grupo):** Uso estrito de `country` para países reais e `group` reservado para agrupamentos genéricos como `'OTHER'`.
* **Layout Limpo de Códigos ICAO/IATA:** Organização visual em linha de apoio abaixo do nome do aeroporto, evitando poluição visual com nomes longos.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Mantenha o Cloudflare Worker atualizado com a **Versão 53**.
2. Atualize o arquivo `index.html` com o código refatorado da **Versão 53**.
3. Faça o commit e publique as alterações no repositório do GitHub.