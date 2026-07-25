# ✈️ Painel de Aeroportos da América do Sul — Versão 42.0

Este documento detalha as atualizações e melhorias implementadas no [Painel de Aeroportos da América do Sul](https://alexgrodrigues.github.io/painel-aeroportos-brasil/), consolidando o monitoramento de aeroportos estratégicos do Brasil e das principais capitais e hubs do continente.

---

## 📋 Resumo das Alterações (Versão 42.0)

### 🔹 Principais Novidades e Recursos
* **Filtros Rápidos por Categoria de Voo:** Adicionados botões interativos (chips) na interface para isolar instantaneamente estações operando sob regras **VFR** (Visual), **MVFR** (Marginal), **IFR** (Restrito) ou **LIFR** (Crítico).
* **Previsão TAF Traduzida para Leigos:** O campo técnico de previsão (*TAF*) agora conta com uma interpretação em texto amigável (`Previsão Traduzida`), facilitando a compreensão rápida para qualquer usuário, mantendo o código técnico original recolhido em um botão expansível opcional.
* **Alertas Visuais para Condições Críticas:** Cards de aeroportos operando em condições meteorológicas restritivas ou críticas (**IFR** / **LIFR**) ganham destaque visual em vermelho.
* **Atualização Automática (Auto-Refresh):** Implementada rotina em segundo plano que atualiza os dados meteorológicos a cada 10 minutos de forma automatizada, exibindo também a barra de status dinâmica com o horário e contagem de estações ativas.
* **Expansão Continental Completa:** Monitoramento unificado cobrindo o Brasil e hubs internacionais na Argentina, Bolívia, Chile, Colômbia, Equador, Paraguai, Peru, Uruguai e Venezuela.

---

## 🛠️ Tecnologias e Arquitetura
* **Frontend:** Interface moderna e responsiva utilizando HTML5, CSS Variables e JavaScript puro (Vanilla JS).
* **Backend / API:** Cloudflare Worker dedicado para requisições assíncronas, tratamento de CORS e cache otimizado das estações de aeródromo.

---

*Gerado automaticamente para o repositório oficial do [Painel de Aeroportos da América do Sul](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).*