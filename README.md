# ✈️ Painel de Aeroportos da América Latina — Versão 45.14

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.14)

* **Delegação Lógica ao Backend (Cloudflare Worker):** O frontend passou a consumir diretamente os atributos lógicos estruturados enviados pelo Worker (`hasMetar`, `hasTaf`, `metarAgeMins` e `isStale`), reduzindo o processamento cliente e garantindo padronização rigorosa na exibição de dados estagnados ou ausentes.
* **Favicon Aeronáutico Incorporado:** Mantido o ícone estilizado do caça Gripen da FAB na aba do navegador.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.14**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento, cálculo de idade de dados e normalização nativa.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*