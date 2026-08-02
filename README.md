# Painel de Aeroportos da América Latina, EUA e Europa (Versão 71.4)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos selecionados.

## 🚀 Versão 71.4 - Atualizações e Melhorias Recentes

Esta versão traz avanços estruturais importantes na performance, persistência de dados e atualização autônoma do painel.

### 📡 Backend (Cloudflare Worker & KV)
* **Cache Persistente via Cloudflare KV:** Integração com armazenamento KV permanente no Cloudflare, garantindo que o primeiro acesso e o carregamento inicial da página ocorram de forma instantânea (sem depender do tempo de resposta da API externa).
* **Controle Rigoroso de Cache HTTP:** Inclusão de cabeçalhos anti-cache estritos (`no-store`, `no-cache`, `must-revalidate`) nas respostas do Worker, impedindo que navegadores armazenem versões antigas e defasadas dos dados meteorológicos.
* **Expansão Global:** Monitoramento contínuo dos principais aeroportos da América Latina, Estados Unidos e as principais rotas da Europa (**Lisboa - LPPT**, **Madri - LEMD**, **Paris - LFPG**, **Londres - LHR** e **Frankfurt - FRA**).
* **Interpretação Avançada do TAF:** Decodificação detalhada e linha por linha das previsões de aeródromo, cobrindo validade, variações graduais (`BECMG`), temporárias (`TEMPO`), temperaturas extremas e observações finais (`RMK`).

### 💻 Frontend (Interface)
* **Atualização Automática em Segundo Plano:** Implementado sistema de sincronização periódica a cada 5 minutos, buscando novas emissões horárias e mensagens SPECI automaticamente sem necessidade de atualizar a aba manualmente.
* **Indicadores Visuais de Defasagem:** Contadores em tempo real do METAR exibidos diretamente em cada cartão ("Atualizado há X min") e alerta global no topo da página em caso de defasagem superior a 1 hora.
* **Bandeiras SVG Padronizadas:** Utilização de ícones SVG (`flagcdn`) nos botões de filtro regional para assegurar renderização nativa e perfeita em qualquer sistema operacional ou dispositivo.
* **Versão 71.4 Sincronizada:** Indicador visual oficial atualizado no cabeçalho do painel.