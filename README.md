# ✈️ Painel de Aeroportos da América Latina — Versão 45.10

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.10)

* **Refinamento da Busca por Texto:** Ajustada a regra de filtragem do campo de pesquisa para priorizar correspondências por prefixo exato no código ICAO (início do código) ou ocorrências diretas no nome da cidade/aeroporto, eliminando falsos positivos e ruídos operacionais (como correspondências em caracteres intermediários).
* **Consolidação dos Alertas Visuais e Idade do METAR:** Mantido o ecossistema robusto de alertas para dados ausentes e cálculo dinâmico da idade das observações UTC.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.10**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento e normalização nativa de dados geográficos e meteorológicos.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*