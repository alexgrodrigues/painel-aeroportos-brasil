# ✈️ Painel de Aeroportos da América Latina — Versão 45.3

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.3)

* **Contrato do Worker Unificado (`group` e `country`):** O backend agora envia de forma limpa as propriedades `group` e `country` derivadas de uma única fonte de verdade centralizada, sem tabelas ou mapas intermediários redundantes.
* **Filtragem Otimizada no Frontend:** O sistema de abas consome diretamente a propriedade `group` do payload do Worker, eliminando lógicas condicionais complexas no navegador.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.3**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento e normalização nativa de dados geográficos e meteorológicos.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*