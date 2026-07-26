# ✈️ Painel de Aeroportos da América Latina — Versão 45.11

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.11)

* **Botão de Limpeza e Ícone de Busca:** Adicionado botão interativo rápido (`✕`) dentro do campo de pesquisa para facilitar a remoção de termos digitados tanto em computadores quanto em dispositivos móveis, complementado por placeholder com ícone de lupa.
* **Filtro de ICAO por Prefixo Exato:** Aprimorada a regra de busca textual (`startsWith` no código ICAO), erradicando definitivamente falsos positivos (como aeroportos contendo letras em posições intermediárias do código).
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.11**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento e normalização nativa de dados geográficos e meteorológicos.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*