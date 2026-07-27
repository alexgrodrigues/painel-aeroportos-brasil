# Painel de Aeroportos da América Latina e EUA (Versão 60)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (METAR, TAF e interpretação automatizada de previsões) nos principais aeroportos, bases aéreas e hubs internacionais da América Latina e dos Estados Unidos.

## 🚀 Histórico de Atualizações Recentes (Versões 57 a 60)

* **Versão 60 (Correção Crítica na Leitura de Ventos):** Ajuste cirúrgico na formatação da exibição de ventos nos cartões do painel, garantindo que a separação de 3 dígitos para direção e velocidade (`340 / 03KT`) seja mantida com total precisão operacional, eliminando leituras ambíguas.
* **Versão 59 (Rodapé de Publicação do METAR):** Adicionada linha dedicada no bloco meteorológico informando o horário Zulu exato de publicação (`Publicado às 03:00Z`) junto ao tempo decorrido.
* **Versão 58 (Sistema de Alerta de Dados Desatualizados):** Implementação de banner global discreto e badges nos cartões para identificar aeroportos com METAR com mais de 1 hora de atraso, mantendo a estabilidade da consulta de dados.
* **Versão 57 (Parser Robusto de METAR):** Blindagem do script para garantir a leitura contínua e estável de relatórios em aeroportos de grande porte (`SBGL`, `SBGR`, `SBBR`, etc.).

## 🛠️ Tecnologias Utilizadas
* **Frontend:** HTML5, CSS3, JavaScript puro hospedado no [GitHub Pages](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).
* **Backend:** Cloudflare Workers integrado à API pública da [Aviation Weather Center](https://aviationweather.gov/).

## ⚙️ Configuração e Execução
1. Atualize o arquivo `index.html` com o código da **Versão 60** contendo a formatação precisa de ventos e o carimbo de tempo Zulu.
2. Certifique-se de que a constante aponta para o worker ativo:
   ```javascript
   const WORKER_URL = "[https://weathered-grass-f181.alexgrodrigues.workers.dev](https://weathered-grass-f181.alexgrodrigues.workers.dev)";