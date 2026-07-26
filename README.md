# Painel de Aeroportos da América Latina (Versão 47)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR e TAF) dos principais aeroportos da América Latina.

## 🚀 O que há de novo na Versão 47
* **Correção da Conexão com o Worker:** Vinculação definitiva da variável `WORKER_URL` para apontar diretamente para o endpoint de produção do Cloudflare Worker (`https://weathered-grass-f181.alexgrodrigues.workers.dev`).
* **Carregamento Automático:** Adicionado evento `onload` para disparar a busca de dados assim que a página é aberta.
* **Organização de Cards:** Exibição completa de dados detalhados incluindo Vento, Pressão QNH, Temperatura, Ponto de Orvalho, METAR e TAF.
* **Filtros Dinâmicos:** Filtragem simultânea por país (Brasil, Argentina, Chile, México, Panamá, Costa Rica, Outros) e por categoria de voo visual/instrumento (VFR, MVFR, IFR, LIFR).

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro (Vanilla JS) hospedado no **GitHub Pages**.
* **Backend:** Cloudflare Workers (JavaScript assíncrono) fazendo o intermédio das requisições via API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração Local / Deploy
1. Clone o repositório.
2. Certifique-se de que o arquivo `index.html` aponta para o Worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";