# ✈️ Painel de Aeroportos Globais (Versão 78.0)

Painel web avançado, responsivo e em tempo real para monitoramento de condições meteorológicas de aviação (**METAR** e **TAF**), desenvolvido com arquitetura robusta para pilotos, operadores de tráfego aéreo e entusiastas da aviação.

---

## 🚀 Novidades e Melhorias da Versão 78.0

* **Validação Estrita no Back-end:** O Worker valida rigorosamente a integridade das respostas HTTP, status code e formato JSON da Aviation Weather API, evitando falhas silenciosas.
* **Versionamento de Cache Inteligente (`v78-strict`):** Previne que dados desatualizados continuem sendo servidos após novos deploys na Cloudflare.
* **Horário Oficial e Data Completa:** Registro temporal unificado por timestamp ISO e fuso horário oficial (`America/Sao_Paulo`), calculando com precisão a idade dos relatórios.
* **Segurança Reforçada (Anti-XSS):** Sanitização e escape automático de todos os textos dinâmicos vindos de APIs externas inseridos no DOM.
* **Remoção de Eventos Inline:** Total desacoplamento entre marcação HTML e lógica JavaScript, garantindo alta manutenibilidade.
* **Contadores Separados (Total vs. Filtrados):** Exibição clara e simultânea da quantidade de aeroportos exibidos na tela em relação ao total global monitorado.
* **Gerenciamento Avançado de Favoritos:** Inclusão de botão dedicado para limpar todos os favoritos instantaneamente.
* **Preservação de Contexto:** Manutenção rigorosa do país selecionado e dos filtros ativos durante as atualizações automáticas e manuais.

---

## 🛠️ Tecnologias Utilizadas

* **Front-end:** HTML5, CSS3 Customizado (Dark Theme responsivo) e JavaScript Puro (*Vanilla JS*) em módulos organizados.
* **Back-end / Proxy:** Cloudflare Workers com KV Storage e tratamento de erros detalhado.
* **Armazenamento Local (`localStorage`):** Persistência segura da lista de aeroportos favoritos do usuário.

---

## 📋 Funcionalidades Principais

1. **Filtros por Categoria de Voo:** Classificação baseada nas regras visuais e instrumentais:
   * 🟢 **VFR** (Visual Flight Rules)
   * 🔵 **MVFR** (Marginal VFR)
   * 🔴 **IFR** (Instrument Flight Rules)
   * 🟣 **LIFR** (Low IFR / Crítico)
   * ⚪ **N/A** (Sem METAR disponível no momento)
2. **Subfiltro Dinâmico por País:** Permite filtrar os aeroportos por nações específicas dentro de cada grande continente ou região geográfica.
3. **Filtro Nativo de Bases Aéreas do Brasil:** Utiliza dados estruturados para separar rapidamente as bases militares por regiões do país.
4. **Modal Técnico:** Clicando no nome de qualquer aeroporto, abre-se um painel de frequências (TWR, GND, ATIS) e dimensões de pistas.