# ✈️ Painel de Aeroportos Globais

Painel web progressivo para monitoramento meteorológico aeronáutico em tempo real (METAR e TAF) de aeroportos civis, bases aéreas e terminais internacionais, integrado com Cloudflare Workers e cache KV.

---

## 🚀 Funcionalidades Principais

* **Monitoramento em Tempo Real:** Consulta otimizada por blocos de aeroportos na API oficial da [Aviation Weather](https://aviationweather.gov/).
* **Decodificador Gramatical Avançado:** Tradução automática de METAR e TAF em linguagem natural para facilitar a leitura operacional por pilotos, operadores e entusiastas.
* **Filtros Geográficos e de Categoria:** Suporte a favoritos, bases aéreas, continentes (América do Sul, América do Norte, Europa, Ásia/Oriente Médio, África) e categorias de voo (`VFR`, `MVFR`, `IFR`, `LIFR`).
* **Resiliência e Cache (Cloudflare KV):** Backend rodando em Cloudflare Workers com TTL de 15 minutos e gatilhos agendados (Cron Trigger) para evitar estouro de requisições na API externa.
* **Identificador Visual Único:** Favicon SVG integrado otimizado para abas de navegadores modernos.

---

## 🛠️ Tecnologias Utilizadas

* **Front-end:** HTML5, Tailwind CSS via CDN, JavaScript Vanilla (ES6+).
* **Back-end / Proxy:** Cloudflare Workers (JavaScript).
* **Armazenamento / Cache:** Cloudflare KV (`WEATHER_KV`).

---

## 📦 Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone [https://github.com/alexgrodrigues/painel-aeroportos-brasil.git](https://github.com/alexgrodrigues/painel-aeroportos-brasil.git)