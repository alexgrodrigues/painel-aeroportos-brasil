# Painel de Aeroportos da América Latina e EUA

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos selecionados na América Latina e Estados Unidos.

## 🚀 Versão 70 - Atualizações e Melhorias

Esta versão consolida a arquitetura do sistema, dividindo as responsabilidades de forma limpa e estruturada entre o **Backend (Cloudflare Worker)** e o **Frontend**.

### 📡 Backend (Cloudflare Worker)
* **Normalização Centralizada do Vento:** O tratamento e a formatação da string de vento (`item.wind`) passaram a ser realizados inteiramente no servidor. O Worker entrega o dado perfeitamente formatado (ex: `200 / 04KT`, `VRB 02KT` ou com rajadas), evitando processamentos redundantes na interface.
* **Prioridade Absoluta para Categorias Oficiais:** A determinação da condição de voo (`VFR`, `MVFR`, `IFR`, `LIFR`) prioriza estritamente os campos oficiais da API da AWC (`flightCategory` / `fltCat`), utilizando heurísticas de texto apenas como plano de contingência (*fallback*).
* **Pressão Altimétrica Transparente:** Conversão automatizada de polegadas de mercúrio (`inHg`) para hectopascais (`hPa`), garantindo total precisão operacional.
* **Segregação Geográfica:** Inclusão oficial do **Uruguai (`SUMU`)** alocado em seu grupo exclusivo (`group: "UY"`).

### 💻 Frontend (Interface)
* **Limpeza e Desacoplamento:** Remoção definitiva da função local `formatWindDisplay()` do código HTML. O frontend atua de forma direta, consumindo e exibindo a string pronta entregue pelo Worker.
* **Consistência Visual:** Alinhamento total entre a API e a renderização dos cartões no [Painel de Aeroportos](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).