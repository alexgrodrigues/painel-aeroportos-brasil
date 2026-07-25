# ✈️ Painel de Aeroportos do Mercosul — Atualizações e Mudanças

Este documento detalha as alterações, melhorias e correções implementadas nesta versão do painel de monitoramento meteorológico aeroportuário.

---

## 📋 Resumo das Alterações

### 🔹 Região Sul (`Brasil — Sul`)
* **Chapecó (SBCH):** Atualização dos dados meteorológicos com vento a `040° / 08 KT`, pressão `Q1019` e temperatura de `19°C`.
* **Canoas (SBCO):** Inclusão de dados METAR e TAF interpretado com previsões detalhadas de visibilidade e nuvens.
* **Curitiba (SBCT):** Atualização do Afonso Pena com vento a `210° / 07 KT`, pressão `Q1022` e adições nas previsões de TAF (incluindo transições para CAVOK).
* **Foz do Iguaçu (SBFI):** Monitoramento atualizado com previsão de pancadas de chuva e tempestades (`TSRA`) nos horários previstos.
* **Florianópolis (SBFL), Navegantes (SBNF), Porto Alegre (SBPA) e Pelotas (SBPK):** Atualizações regulares de relatórios METAR/TAF com novas condições de vento, umidade e nevoeiros previstos.

### 🔹 Região Sudeste (`Brasil — Sudeste`)
* **Confins (SBCF):** Ajustes nos dados do aeroporto internacional com vento a `260° / 06 KT` e temperatura de `21°C`.
* **Galeão (SBGL) & Santos Dumont (SBRJ):** Atualizações de condições de pista, visibilidade e previsões de chuvisco (`DZ`) para o Rio de Janeiro.
* **Guarulhos (SBGR), Viracopos (SBKP) & Congonhas (SBSP):** Dados meteorológicos e previsões de TAF atualizados para os principais terminais paulistas.
* **Ribeirão Preto (SBRP):** Atualização do Aeroporto Leite Lopes com vento a `170° / 07 KT`.

### 🔹 Região Centro-Oeste (`Brasil — Centro-Oeste`)
* **Brasília (SBBR), Campo Grande (SBCG), Várzea Grande (SBCY) e Goiânia (SBGO):** Dados de temperatura e pressão atualizados (destaque para temperaturas elevadas em Cuiabá atingindo `33°C` com céu claro/CAVOK).

### 🔹 Região Nordeste (`Brasil — Nordeste`)
* **Aracaju (SBAR), Fortaleza (SBFZ), João Pessoa (SBJP), Marabá (SBMA) e Maceió (SBMO):** Atualizações de relatórios METAR e TAF com condições locais de vento e umidade.

---

## 🛠️ Melhorias Técnicas e Interface
* Aprimoramento da leitura e interpretação automática dos blocos **METAR** e **TAF**.
* Atualização dos cards informativos por região com indicadores visuais de regras de voo (**VFR**, **MVFR**, etc.).
* Otimização do cache de atualização de dados e tempo de resposta do painel.

---

*Gerado automaticamente para o repositório do [Painel de Aeroportos do Brasil](https://alexgrodrigues.github.io/painel-aeroportos-brasil/).*