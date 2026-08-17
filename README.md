# ✈️ Painel de Aeroportos Globais (Versão 77.0)

Painel web avançado e em tempo real para monitoramento de condições meteorológicas de aviação (**METAR** e **TAF**), desenvolvido para pilotos, operadores de tráfego aéreo e entusiastas da aviação.

---

## 🚀 Novidades da Versão 77.0

* **Subfiltro Dinâmico por País:** Ao selecionar uma região geográfica (como *América do Sul*, *América Central* ou *Caribe*), o painel exibe instantaneamente uma barra secundária contendo os países daquela região específica, permitindo filtrar os aeroportos individualmente com um clique.
* **Cobertura Expandida da América do Sul e Central:** Adicionados os principais hubs e aeroportos internacionais de países como Argentina, Chile, Colômbia, Peru, Uruguai, Paraguai, Bolívia, Equador, Venezuela, Panamá, Costa Rica, Guatemala, Honduras, El Salvador, Nicarágua, República Dominicana e Cuba.
* **Sistema de Favoritos (`⭐` / `☆`):** Permite marcar aeroportos estratégicos ou bases de preferência para acesso rápido através do filtro de favoritos.
* **Modal de Frequências e Pistas:** Clicando no nome de qualquer aeroporto, abre-se um painel dedicado detalhando as frequências de Torre (TWR), Solo (GND) e ATIS, além das dimensões e orientações das pistas disponíveis.
* **Indicadores de Defasagem Temporal:** Alerta visual automático caso algum dado meteorológico do METAR ultrapasse 1 hora de atraso em relação à última emissão oficial.

---

## 🛠️ Tecnologias Utilizadas

* **Front-end:** HTML5, CSS3 Customizado (Design Responsivo/Dark Theme) e JavaScript Puro (*Vanilla JS*).
* **Back-end / Proxy:** Cloudflare Workers para consumo assíncrono e unificado das APIs públicas de meteorologia aeronáutica (*Aviation Weather*).
* **Armazenamento Local (`localStorage`):** Utilizado para salvar permanentemente a lista de aeroportos favoritos configurada pelo usuário no navegador.

---

## 📋 Funcionalidades Principais

1. **Filtros por Categoria de Voo:** Classificação automática baseada nas regras visuais e instrumentais:
   * 🟢 **VFR** (Visual Flight Rules)
   * 🔵 **MVFR** (Marginal VFR)
   * 🔴 **IFR** (Instrument Flight Rules)
   * 🟣 **LIFR** (Low IFR / Crítico)
2. **Busca Inteligente:** Barra de pesquisa em tempo real capaz de filtrar simultaneamente por código **ICAO**, **IATA**, **Nome do Aeroporto** ou **Cidade**.
3. **Filtro de Bases Aéreas do Brasil:** Menu dedicado para isolar rapidamente as bases da Força Aérea Brasileira separadas por regiões militares.
4. **Interpretação Automática de METAR e TAF:** Tradução de dados brutos para leituras intuitivas de vento, visibilidade, pressão atmosférica (hPa) e temperaturas.

---

## 📦 Como Executar o Projeto

1. Hospede o arquivo front-end (`index.html`) em um serviço de hospedagem estática (como [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/#)).
2. Configure o endpoint do seu **Cloudflare Worker** na constante `WORKER_URL` dentro do script da página para realizar o fetch dos dados em tempo real.