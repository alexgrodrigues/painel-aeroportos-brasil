# Painel de Aeroportos da América Latina e EUA (Versão 67)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 Histórico de Atualizações Recentes (Versões 61 a 67)

* **Versão 67 (Padronização Visual dos Filtros):** Ajuste milimétrico nas dimensões e proporções simétricas dos ícones SVG das bandeiras nos botões de filtro, garantindo alinhamento visual perfeito e simétrico.
* **Versão 66 (Resturação de Parsers e Estabilidade):** Reversão de ajustes pontuais no motor de parsing para assegurar leitura nativa e estável de todos os relatórios METAR.
* **Versão 65 (Reestruturação de Países):** Costa Rica integrada ao grupo "Outros" e inclusão oficial do Uruguai com suporte a bandeira vetorial dedicada.
* **Versão 64 (Implementação de SVGs Nativos):** Substituição de emojis de bandeira por vetores SVG inline para garantir renderização perfeita e idêntica em 100% dos navegadores (Chrome, Brave, Edge e Firefox).
* **Versão 63 (Limpeza de Interface):** Ajustes no favicon exclusivo da aba e remoção de redundâncias textuais nos filtros.
* **Versão 61-62 (Formatação de Ventos e Horário Zulu):** Formatação aprimorada de ventos direcionados (`340 / 03KT`) e variáveis (`VRB 02KT`), além da adição do rodapé de horário exato de publicação e alerta de dados desatualizados.

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com o código da **Versão 67**.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";