# ✈️ Painel de Aeroportos da América Latina — Versão 45.7

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.7)

* **Timestamp por Cartão:** Adicionado o indicador do horário de observação UTC extraído diretamente do METAR (`HH:MMZ`), permitindo que o operador valide instantaneamente o frescor do dado meteorológico.
* **Resumo do Filtro Ativo:** Incluída uma linha explicativa no topo exibindo em tempo real os critérios combinados de visualização (ex: *Filtro ativo: Brasil + IFR*), eliminando qualquer ambiguidade de navegação.
* **Contadores Operacionais Dinâmicos:** Mantida a adaptação automática dos contadores estatísticos globais e regionais conforme as abas de países e categorias são selecionadas.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.7**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento e normalização nativa de dados geográficos e meteorológicos.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*