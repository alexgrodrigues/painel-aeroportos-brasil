# Painel de Aeroportos da América Latina, EUA e Europa (Versão 71.3)

Painel web em tempo real para monitoramento de condições meteorológicas aeronáuticas (**METAR** e **TAF**) de aeroportos selecionados.

## 🚀 Versão 71.3 - Atualizações e Melhorias Recentes

Esta versão consolida a expansão global da malha de aeroportos monitorados e traz otimizações fundamentais de performance, estabilidade e clareza analítica.

### 📡 Backend (Cloudflare Worker)
* **Expansão Global (América Latina, EUA e Europa):** Inclusão oficial dos principais aeroportos estratégicos, destacando agora a rota de transatlânticos da Europa:
  * **Lisboa (LPPT)**
  * **Madri (LEMD)**
  * **Paris-Charles de Gaulle (LFPG)**
  * **Londres-Heathrow (EGLL)**
  * **Frankfurt (EDDF)**
* **Cache Inteligente e Cron Triggers:** Implementação de cache de 10 minutos na camada do Cloudflare Worker com rotina automática em segundo plano (`Cron Trigger`), garantindo que o primeiro acesso e o carregamento da página ocorram instantaneamente e sem falhas de timeout.
* **Interpretação Avançada do TAF:** Nova rotina de decodificação detalhada e linha por linha das previsões (TAF), decompondo o período de validade, condições iniciais, variações graduais (`BECMG`), períodos temporários (`TEMPO`), probabilidades e observações finais (`RMK`).

### 💻 Frontend (Interface)
* **Indicadores Visuais de Defasagem:** Adicionado contador de tempo decorrido do METAR diretamente nos cartões de cada aeroporto ("Atualizado há X min" ou "Desatualizado") e um aviso global no topo da página quando houver dados com mais de 1 hora de atraso.
* **Filtros Regionais com Bandeiras SVG:** Barra de navegação por países e regiões atualizada para utilizar bandeiras em formato SVG (`flagcdn`), garantindo renderização nativa e perfeita em qualquer sistema operacional (Windows, Linux, macOS, iOS e Android).
* **Tratamento Contra Transições Horárias:** Sistema de cache local persistente para impedir que cartões fiquem vazios ou exibam `N/A` durante a janela de transição e virada de hora da API de meteorologia.
* **Versão 71.3 Atualizada:** Interface visualmente sincronizada com o indicador oficial de versão no topo do painel.