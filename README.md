# Painel de Aeroportos da América Latina, EUA e Europa

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos selecionados.

## 🚀 Versão 71 - Atualizações e Melhorias

Esta versão expande a cobertura global do painel e consolida as melhorias de estabilidade de dados introduzidas anteriormente.

### 📡 Backend (Cloudflare Worker)
* **Expansão para a Europa:** Inclusão oficial dos 5 principais aeroportos europeus que mais recebem voos do Brasil:
  * **Lisboa (LPPT)**
  * **Madri (LEMD)**
  * **Paris-Charles de Gaulle (LFPG)**
  * **Londres-Heathrow (EGLL)**
  * **Frankfurt (EDDF)**
* **Normalização e Cache:** Mantida a arquitetura robusta com tratamento centralizado de ventos (`item.wind`), conversão de pressão para `hPa` e preservação inteligente de dados via cache local no frontend para evitar falhas durante transições horárias da API.

### 💻 Frontend (Interface)
* **Novo Filtro Regional:** Adicionado o botão de filtro rápido para a **🇪🇺 Europa** na barra de navegação superior, facilitando o agrupamento e monitoramento dos aeroportos do continente.
* **Versão 71 Atualizada:** Indicador de versão visual atualizado para refletir a nova expansão de rotas e melhorias de usabilidade no [Painel de Aeroportos](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).