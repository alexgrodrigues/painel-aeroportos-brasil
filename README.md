# Painel de Aeroportos Globais (Versão 71.7)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos estratégicos distribuídos globalmente.

## 🚀 Versão 71.7 - Atualizações e Melhorias Recentes

Esta versão traz uma reestruturação completa na categorização regional e na experiência de navegação do painel.

### 🌎 Nova Organização por Regiões e Continentes
* **América do Sul (`SOUTH_AMERICA`):** Terminais do Brasil, Argentina, Chile, Colômbia, Peru, Uruguai e Paraguai.
* **América Central (`CENTRAL_AMERICA`):** Panamá, Costa Rica, Guatemala, Honduras, Nicarágua e El Salvador.
* **Caribe (`CARIBBEAN`):** Cuba (Havana) e Porto Rico (San Juan).
* **América do Norte (`NORTH_AMERICA`):** Estados Unidos e México.
* **Europa (`EUROPE`):** Lisboa, Madri, Paris, Londres, Frankfurt, Istambul e Gibraltar.
* **Ásia / Oriente Médio / Rússia (`ASIA_ME`):** Moscou, Dubai, Tóquio, Pequim, Xangai, Cingapura e Seul.

### 📡 Arquitetura & Persistência (Cloudflare Worker & KV)
* **Armazenamento KV Permanente:** Leitura instantânea e carregamento sem latência na primeira abertura da página.
* **Controle Rigoroso de Cache HTTP:** Cabeçalhos `no-store` e `no-cache` garantindo dados atualizados direto do Cloudflare.
* **Atualização Automática (Polling):** Varredura autônoma em segundo plano a cada 5 minutos para capturar boletins METAR horários e mensagens SPECI sem recarregar a aba manualmente.