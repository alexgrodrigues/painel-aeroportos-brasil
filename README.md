# ✈️ Painel de Aeroportos Globais (Versão 83.1)

Painel web progressivo para monitoramento meteorológico aeronáutico em tempo real (METAR e TAF) de aeroportos globais e bases aéreas, desenvolvido com foco em precisão temporal, rigor gramatical aeronáutico e robustez de persistência.

---

## 🚀 Principais Atualizações e Histórico de Evolução (v79 a v83.1)

### 📌 Versão 83.1 — Correção de Renderização de Cache e Segurança
* **Serialização DOM Segura:** Adaptação da persistência do TAF interpretado para strings HTML limpas, corrigindo exceções de `cloneNode` ao restaurar dados do `localStorage`.
* **Parser de Cabeçalho via RegEx:** Identificação flexível de `TAF`, emendas (`AMD`) e correções (`COR`) independentemente de índices fixos ou formatações inconsistentes.
* **Grupos Compostos (`PROB30/40 TEMPO`):** Tratamento combinatório exato entre probabilidades estatísticas e flutuações temporárias de vento, visibilidade e fenômenos.
* **Variação Direcional do Vento:** Decodificação e tradução de faixas de variação direcional (ex: `150V210`).
* **Validação de Versão do Parser no Cache:** Auto-limpeza de cache local quando detectada divergência no `parserVersion`, forçando o re-processamento com o motor mais recente.

### ⏱️ Versão 82.0 — Motor Parser de TAF de Alta Fidelidade
* **Decodificador de Intensidade e Descritores:** Mapeamento gramatical de intensidade (`-`, moderada, `+`), descritores (`TS`, `SH`, `FZ`, `BL`, etc.) e fenômenos (`RA`, `SN`, `DZ`, `FG`, `BR`, `HZ`, etc.).
* **Tratamento Rigoroso do Grupo FM:** Conversão exata de `FM171200` para *"A partir do dia 17 às 12:00 UTC"*, herdando descontinuidades de forma isolada.
* **Identificação de Teto Mínimo:** Extração automática da camada restritiva mais baixa (`BKN`, `OVC` ou `VV`) para cada período da previsão.

### 🛡️ Versão 81.0 — Parser Estruturado por Blocos
* Substituição de buscas textuais genéricas por divisão estrutural do TAF (Cabeçalho, Condições Predominantes, Grupos de Mudança e Temperaturas).
* Estilização visual dedicada por categoria de alteração e aviso nativo de grupos não interpretados.

### ⏳ Versão 80.0 — Rigor Temporal, Persistência e Acessibilidade
* **Compatibilidade Dupla de `observationTime`:** Suporte simultâneo a timestamps numéricos (Epoch) e strings ISO.
* **Idade Real de Dados:** Cálculo dinâmico da idade do METAR em relação ao momento atual (`Date.now()`), mesmo para cartões restaurados do cache local.
* **Acessibilidade de Teclado:** Suporte completo a `Enter` e `Barra de Espaço` no título do aeroporto para abertura do modal, com devolução automática de foco ao elemento de origem.

---

## 🛠️ Tecnologias e Arquitetura

* **Front-end:** HTML5, CSS3 Moderno (Variáveis Customizadas, Grid/Flexbox), JavaScript Vanilla (ES6+).
* **Back-end / Proxy:** Cloudflare Workers integrado à API da Aviation Weather.
* **Armazenamento:** `localStorage` com controle estrito de versão de estado e parser (`v83.1-taf-pro`).

---

## 📦 Como Executar Localmente

1. Clone o repositório do [GitHub de Aeroportos Brasil](https://github.com/alexgrodrigues/painel-aeroportos-brasil) ou salve os códigos acima.
2. Certifique-se de que o endpoint do Worker (`CONFIG.WORKER_URL`) está ativo.
3. Abra o arquivo `index.html` diretamente em qualquer navegador moderno ou utilize um servidor local (Live Server).