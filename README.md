# ✈️ Painel de Aeroportos Globais (METAR & TAF)

Painel web interativo para monitoramento meteorológico aeronáutico em tempo real, integrando dados oficiais de METAR e TAF por meio de um Cloudflare Worker e exibindo em uma interface moderna baseada em Tailwind CSS.

## 🚀 Novidades da Versão v4
- **Aeroportos Adicionados:** 
  - Paso de los Libres (SARI - Argentina)
  - Uruguaiana - Ruben Berta (SBUG - Brasil)
  - Porto Seguro (SBPS - Brasil)
  - Principais aeroportos da Austrália/Oceania (`YSSY`, `YMML`, `YBBN`, `YPPH`).
- **Favoritos no Topo:** A listagem de aeroportos agora ordena automaticamente os itens favoritados para o topo da exibição.
- **Filtro da Oceania:** Adicionada aba de filtro específica para a região da Oceania.

---

## 🛠️ Tecnologias Utilizadas
- **Frontend:** HTML5, JavaScript Moderno (Vanilla JS), Tailwind CSS (via CDN).
- **Backend / Cache:** Cloudflare Workers (JavaScript/ES Modules) com armazenamento em Cloudflare KV (`weather:v4:global-airports`).
- **Fonte de Dados:** Aviation Weather API (`aviationweather.gov`).

---

## 📱 Funcionalidades
1. **Pesquisa Instantânea:** Filtre aeroportos por código ICAO, código IATA, nome da cidade ou nome do aeroporto em tempo real.
2. **Categorias de Voo Visuais:** Identificação imediata por cores baseadas nas regras de voo (VFR, MVFR, IFR, LIFR).
3. **Interpretação Automática:** Conversão de códigos crus de METAR e TAF em textos legíveis e analíticos.
4. **Sistema de Favoritos:** Fixe seus aeroportos de preferência no topo da lista utilizando armazenamento local (`localStorage`).
5. **Dados Complementares:** Exibição de frequências de rádio (Torre/ATIS) e especificações de pistas.

---

## ⚙️ Configuração e Execução

### Front-end
Basta hospedar o arquivo `index.html` em qualquer servidor estático (como o GitHub Pages) garantindo que a constante `WORKER_URL`ponha corretamente para o seu Cloudflare Worker ativo.

### Back-end (Cloudflare Worker)
1. Crie um Worker no Cloudflare com o script fornecido em `worker.js`.
2. Configure um binding de KV chamado `WEATHER_KV`.
3. Publique o worker e atualize a URL no arquivo do frontend.