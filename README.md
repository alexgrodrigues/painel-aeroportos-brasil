# ✈️ Painel de Aeroportos da América do Sul — Versão 40.0

Este repositório hospeda o **Painel de Aeroportos da América do Sul**, uma ferramenta web desenvolvida para monitoramento meteorológico em tempo real (METAR e TAF) de aeroportos estratégicos do Brasil e das principais capitais e hubs internacionais do continente.

---

## 🌟 O Que Há de Novo na Versão 40.0

* **Expansão Continental:** Inclusão de estações meteorológicas de países vizinhos da América do Sul (como Argentina, Chile, Colômbia, Uruguai, Paraguai, Bolívia, Equador, Peru e Venezuela).
* **Alertas Visuais para Condições Críticas:** Os cards de aeroportos operando sob regras restritivas (**IFR** ou **LIFR**) agora contam com destaque visual em vermelho para identificação imediata de segurança.
* **Previsão TAF Interativa:** O bloco de previsão (*TAF*) foi integrado com botão retrátil ("Ver Previsão TAF"), otimizando o espaço visual dos cards sem perder informações técnicas avançadas.
* **Barra de Status Dinâmica:** Indicador em tempo real do horário da última atualização e contagem total de aeroportos monitorados.
* **Filtros Regionais Customizados:** Seletor rápido por nação na barra de controles superior para facilitar a filtragem por país.

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 moderno (com variáveis e suporte responsivo em Grid) e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Workers integrado à API da *Aviation Weather* para cache, alta performance e tratamento de CORS assíncrono.
* **Hospedagem:** GitHub Pages.

---

*Painel mantido para o monitoramento otimizado de voos e condições meteorológicas da aviação civil.*