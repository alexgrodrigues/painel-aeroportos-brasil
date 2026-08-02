# Painel de Aeroportos Globais (Versão 72.2)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) e dados operacionais de aeroportos estratégicos distribuídos globalmente.

## 🚀 Novidades e Evoluções Recentes (Versões 71.8 a 72.2)

Esta seção resume todas as melhorias arquiteturais, funcionais e de experiência de usuário adicionadas recentemente ao painel:

### 1. 🌍 Expansão Global e Inclusão da África (`Versão 72.0`)
* **Cobertura Intercontinental Completa:** Além da América do Sul, América Central, Caribe, América do Norte, Europa e Ásia/Oriente Médio/Rússia, o painel agora monitora oficialmente os principais hubs do **continente africano** (`AFRICA`), incluindo:
  * **Johanesburgo:** Aeroporto Internacional O. R. Tambo (`FAOR` / `JNB`)
  * **Cairo:** Aeroporto Internacional do Cairo (`HECA` / `CAI`)
  * **Casablanca:** Aeroporto Internacional Mohammed V (`GMAD` / `CMN`)
  * **Cidade do Cabo:** Aeroporto Internacional da Cidade do Cabo (`FACT` / `CPT`)

### 2. 📡 Suporte a Unidades Internacionais de Vento (`Versão 71.9`)
* **Leitura de `MPS` e `KT`:** Ajuste nas expressões regulares do backend para capturar e exibir perfeitamente ventos medidos em nós (*Knots* - `KT`) quanto em metros por segundo (*Meters per Second* - `MPS`), comumente utilizados em aeroportos da Rússia e Ásia (ex: UUEE).

### 3. 🛠️ Ferramenta Operacional e Modal de Aeroportos (`Versão 72.1`)
* **Nomes Clicáveis:** Ao clicar no nome de qualquer aeroporto no cabeçalho do cartão, um modal interativo é aberto exibindo:
  * **Frequências de Comunicação:** Canais oficiais de Torre (`TWR`), Solo (`GND`) e `ATIS`.
  * **Dimensões e Designações de Pistas:** Listagem completa das cabeceiras ativas e comprimentos em metros.
* **Visibilidade na Interpretação do METAR:** A tradução automática do METAR passou a incluir de forma clara os dados de visibilidade horizontal (metros/km) e condições ativas (chuva, névoa, trovoada).

### 4. 🎨 Otimização Visual e Padronização de Cards (`Versão 72.2`)
* **Layout Compacto e Limpo:** A interpretação do METAR e as previsões TAF foram encapsuladas em tags `<details>` estilizadas (*"💡 Ver Interpretação do METAR"* e *"⏱️ Ver TAF (Previsão / Bruto)"*). Isso garante que todos os cartões mantenham uma altura limpa, padronizada e visualmente organizada, independentemente da extensão dos boletins meteorológicos.

### 🏛️ Arquitetura & Persistência (Cloudflare Worker & KV)
* **Padronização Semântica Completa:** Alinhamento rigoroso nas três camadas do sistema (dados via `group`, UI via `regionFilters` e lógica via `currentRegion`).
* **Armazenamento KV Permanente:** Leitura instantânea e carregamento sem latência na primeira abertura da página.
* **Controle Rigoroso de Cache HTTP:** Cabeçalhos `no-store` e `no-cache` garantindo dados atualizados direto do Cloudflare.
* **Atualização Automática (Polling):** Varredura autônoma em segundo plano a cada 5 minutos para capturar boletins METAR horários e mensagens SPECI sem recarregar a aba manualmente.