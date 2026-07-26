# ✈️ Painel de Aeroportos da América Latina — Versão 45.3

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.3)

* **Refatoração do Contrato do Worker (Campo `group`):** O backend agora envia de forma explícita a propriedade `group` (`BR`, `AR`, `CL`, `MX`, `PA`, `CR`, `OTHER`) calculada diretamente no servidor com base nos prefixos ICAO.
* **Limpeza de Lógica no Frontend:** Removida a regra de negações em cadeia no navegador, tornando a filtragem por abas limpa, direta e baseada na propriedade `a.group === activeCountryFilter`.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.3**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento de dados por grupo geográfico e tratamento de CORS.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*