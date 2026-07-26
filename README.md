# ✈️ Painel de Aeroportos da América Latina — Versão 45.1

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.1)

* **Navegação por Abas de Países:** Implementado sistema interativo de abas no topo da interface para isolar instantaneamente os aeroportos por país/região (Brasil, Argentina, Chile, México, Panamá, Costa Rica e Outros).
* **Filtros Simultâneos por Condição de Voo:** Mantidos e otimizados os chips de filtragem rápida para regras de voo (**VFR**, **MVFR**, **IFR**, **LIFR**), permitindo cruzar a seleção de países com as condições meteorológicas críticas.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.1**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* para cache, alta performance e tratamento de CORS assíncrono.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*