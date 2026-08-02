# Painel de Aeroportos Globais (Versão 71.5)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos estratégicos no Brasil, Américas, Europa, Ásia, Rússia e Oriente Médio.

## 🚀 Versão 71.5 - Atualizações e Melhorias Recentes

Esta versão consolida a grande expansão intercontinental da malha monitorada e aprimora a robustez de cache e atualização autônoma.

### 📡 Backend (Cloudflare Worker & KV)
* **Expansão Global (Ásia, Rússia, Oriente Médio, Istambul e Gibraltar):** Inclusão de grandes hubs internacionais e rotas de longa distância:
  * **Moscou:** Sheremetyevo (`UUEE`) e Domodedovo (`UUDD`)
  * **Dubai:** Aeroporto Internacional de Dubai (`OMDB`)
  * **Japão:** Narita (`RJAA`) e Haneda (`RJTT`)
  * **China:** Pequim-Capital (`ZBAA`) e Xangai-Pudong (`ZSPD`)
  * **Cingapura & Seul:** Changi (`WSSS`) e Incheon (`RKSI`)
  * **Turquia & Gibraltar:** Istambul (`LTFM`) e Gibraltar (`LXGB`)
* **Cache Persistente via Cloudflare KV:** Armazenamento KV permanente garantindo abertura instantânea e carregamento sem latência na primeira requisição.
* **Controle Rigoroso de Cache HTTP:** Cabeçalhos restritos (`no-store`, `no-cache`, `must-revalidate`) para evitar versões defasadas no navegador.
* **Interpretação Avançada do TAF:** Decodificação detalhada linha por linha cobrindo validades, variações graduais (`BECMG`), temporárias (`TEMPO`), temperaturas extremas e observações finais (`RMK`).

### 💻 Frontend (Interface)
* **Atualização Automática em Segundo Plano:** Sistema de varredura periódica a cada 5 minutos para capturar novas emissões horárias e mensagens SPECI automaticamente.
* **Indicadores Visuais de Defasagem:** Contadores em tempo real do METAR por cartão e alerta global em caso de defasagem superior a 1 hora.
* **Bandeiras SVG Padronizadas:** Ícones em formato SVG (`flagcdn`) nos botões de filtro regional para renderização perfeita em qualquer sistema operacional.
* **Versão 71.5 Sincronizada:** Indicador visual oficial atualizado no cabeçalho do painel.