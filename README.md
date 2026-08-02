# Painel de Aeroportos Globais (Versão 72.0)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos estratégicos distribuídos globalmente.

## 🚀 Versão 72.0 - Atualizações e Melhorias Recentes

Esta versão conclui a cobertura intercontinental global com a inclusão oficial do **continente africano**, além de manter as correções de ventos em unidades `MPS`/`KT` e a padronização de filtros regionais.

### 🌍 Nova Região Adicionada (`AFRICA`)
* **África (`AFRICA`):** Inclusão de principais hubs intercontinentais de referência:
  * **Johanesburgo:** Aeroporto Internacional O. R. Tambo (`FAOR` / `JNB`)
  * **Cairo:** Aeroporto Internacional do Cairo (`HECA` / `CAI`)
  * **Casablanca:** Aeroporto Internacional Mohammed V (`GMAD` / `CMN`)
  * **Cidade do Cabo:** Aeroporto Internacional da Cidade do Cabo (`FACT` / `CPT`)

### 🌐 Coleta e Regiões Padronizadas (`currentRegion`)
* **América do Sul (`SOUTH_AMERICA`)**
* **América Central (`CENTRAL_AMERICA`)**
* **Caribe (`CARIBBEAN`)**
* **América do Norte (`NORTH_AMERICA`)**
* **Europa (`EUROPE`)**
* **Ásia / Oriente Médio / Rússia (`ASIA_ME`)**
* **África (`AFRICA`)**

### 📡 Arquitetura & Persistência (Cloudflare Worker & KV)
* **Armazenamento KV Permanente:** Leitura instantânea e carregamento sem latência na primeira abertura da página.
* **Controle Rigoroso de Cache HTTP:** Cabeçalhos `no-store` e `no-cache` garantindo dados atualizados direto do Cloudflare.
* **Atualização Automática (Polling):** Varredura autônoma em segundo plano a cada 5 minutos para capturar boletins METAR horários e mensagens SPECI sem recarregar a aba manualmente.