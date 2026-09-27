# 🛫 Painel de Aeroportos Globais (Versão 47)

Painel em tempo real para monitoramento global de condições meteorológicas de voo (**METAR** e **TAF**) e metadados operacionais de aeroportos estratégicos nas Américas, Europa, Ásia, Oriente Médio, África, Oceania e Antártida.

---

## 🛠️ Alterações e Evoluções Recentes (Versão 47)

1. **Expansão Global Completa:**
   - Adicionados os principais hubs internacionais da **Europa** (Londres-Heathrow, Paris-Charles de Gaulle, Frankfurt), **Ásia** (Tóquio-Haneda, Singapura-Changi) e **Oriente Médio** (Dubai, Doha).
   - Inclusão oficial de estações estratégicas regionais como o **Aeroporto de Bagé (SBBG)** e o aeródromo antártico **SCRM**.

2. **Aprimoramento de Metadados Militares e de Rádio:**
   - Atualização e verificação de frequências reais de rádio (Torre, Solo e ATIS).
   - **Inclusão de frequências militares** para todas as Bases Aéreas da Força Aérea Brasileira (FAB) e postos mistos (ex: Canoas-BACO em `122.80 MHz`).
   - Ajuste no frontend (`index.html`) para renderizar de forma limpa as frequências militares (`Mil`) nos cartões de cada base aérea.

3. **Arquitetura e Resiliência:**
   - Divisão em lotes paralelos para requisições seguras à API de meteorologia.
   - Sistema de cache otimizado via Cloudflare KV.

---

## 🚀 Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone [https://github.com/alexgrodrigues/painel-aeroportos-brasil.git](https://github.com/alexgrodrigues/painel-aeroportos-brasil.git)