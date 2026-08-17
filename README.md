# ✈️ Painel de Aeroportos Globais (Global Airports Dashboard)

Painel web em tempo real para monitoramento de condições meteorológicas de aeroportos e bases aéreas ao redor do mundo, consumindo dados oficiais de METAR e TAF.

---

## 🚀 Novidades da Versão 76.0

* **⭐ Sistema de Favoritos:** Marque seus aeroportos ou bases prediletas com uma estrela diretamente no card para acessá-los rapidamente através do filtro dedicado. Os favoritos ficam salvos no navegador (`localStorage`).
* **🏳️ Subfiltro por País:** Ao selecionar uma região global (como *América do Sul* ou *Europa*), uma barra secundária aparece automaticamente permitindo filtrar os aeroportos por país específico.
* **❌ Limpeza Rápida na Busca:** Adicionado um botão "X" interativo dentro do campo de pesquisa para limpar o texto digitado instantaneamente com um clique.
* **🏝️ Inclusão de Ilhas do Atlântico:** Adicionadas ilhas estratégicas e bases regionais (como Fernando de Noronha `SBFN`, Mount Pleasant / Falklands `EGYP`, Açores `LPAZ`/`LPPD` e Cabo Verde `GVAC`/`GVNP`).

---

## 🛠️ Tecnologias Utilizadas

* **Front-end:** HTML5, CSS3 e JavaScript Moderno (Vanilla JS com layout responsivo em Grid).
* **Back-end:** Cloudflare Workers (`worker.js`) para cache de requisições, tratamento assíncrono de chunks e traduções/interpretações de METAR/TAF.
* **APIs de Dados:** [Aviation Weather Center API](https://aviationweather.gov/).

---

## 📦 Estruturação do Projeto

```text
├── index.html        # Interface de usuário completa (Painel, Favoritos, Filtros e Busca)
└── worker.js         # Cloudflare Worker responsável por buscar, estruturar e processar os dados