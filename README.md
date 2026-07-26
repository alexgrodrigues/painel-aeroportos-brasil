# ✈️ Painel de Aeroportos da América do Sul — Versão 44.1

Este repositório hospeda o **Painel de Aeroportos da América do Sul**, uma ferramenta web desenvolvida para monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil e das principais capitais e hubs internacionais do continente.

---

## 📋 Resumo das Alterações e Correções

* **Correção de METARs Ausentes:** Ajuste na extração de dados e propriedades do Worker para estações específicas como `SCEL`, `SBBE`, `SBCY`, `SBEG`, `SBMQ` e `SBSG`.
* **Inclusão de Estações na Venezuela:** Adicionados tanto o aeroporto internacional civil (`SVMI`) quanto a base aérea militar (`SVBL`) para garantir cobertura completa em Caracas.
* **Limpeza de Interface:** Remoção de textos descritivos longos no cabeçalho superior da aplicação, mantendo apenas a indicação limpa da **VERSÃO 44.1**.
* **Filtros e Tradução TAF:** Preservação dos filtros rápidos por categoria de voo e da tradução amigável do TAF para leigos.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* para cache, alta performance e tratamento de CORS assíncrono.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*