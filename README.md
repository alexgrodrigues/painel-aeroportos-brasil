# ✈️ Painel de Aeroportos da América Latina — Versão 45.6

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.6)

* **Contadores Operacionais Dinâmicos:** Os contadores no topo (`Total`, `VFR`, `MVFR`, `IFR`, `LIFR`) agora se adaptam em tempo real conforme a aba de país/região é selecionada. Ao filtrar por um país específico, os números refletem exclusivamente o cenário daquela malha, retornando ao panorama geral global quando a aba **"Todos"** está ativa.
* **Adição de Contadores Operacionais Globais:** Introduzida a barra de resumo estatístico no topo na versão anterior para leitura imediata da gravidade meteorológica.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.6**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento e normalização nativa de dados geográficos e meteorológicos.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*