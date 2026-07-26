# ✈️ Painel de Aeroportos da América Latina — Versão 45.8

Este repositório hospeda o **Painel de Aeroportos da América Latina**, ferramenta web voltada para o monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil, América do Sul, América Central e México.

---

## 📋 Resumo das Alterações (Versão 45.8)

* **Idade do Dado (Timestamp com Tempo Decorrido):** Aprimorado o rodapé dos cartões para calcular dinamicamente o tempo decorrido desde a emissão do METAR UTC (ex: *04:00Z (há 25m)*).
* **Alerta Visual de Defasagem:** Adicionado destaque automático em tom de aviso caso o relatório meteorológico ultrapasse o limiar de 90 minutos sem nova emissão, aumentando o rigor na mitigação de riscos operacionais.
* **Manutenção dos Contadores Dinâmicos e Resumo Ativo:** Preservada a lógica inteligente de contagem por filtro regional e a exibição explícita do filtro atual no topo.
* **Controle de Versão:** Atualizado formalmente para a **VERSÃO 45.8**.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* com enriquecimento e normalização nativa de dados geográficos e meteorológicos.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*