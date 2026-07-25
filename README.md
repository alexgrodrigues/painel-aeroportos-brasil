# README v37

## Projeto
Principais Aeroportos Mercosul V37.

## Estrutura da interface
- ICAO no topo.
- Tipo de operação (IFR/LIFR/VFR/MVFR) no extremo da mesma linha.
- Cidade abaixo do ICAO.
- País abaixo da cidade.
- Nome completo do aeroporto em linha secundária.

## Aeroportos cobertos
- 41 aeroportos do Mercosul, com nomes e cidades definidos no frontend.

## Dados exibidos
- METAR.
- TAF.
- Vento.
- Pressão.
- Temperatura.
- Ponto de orvalho.
- Categoria operacional.

## Cache
- O Worker continua com cache de 15 minutos.
- O topo da página mostra o estado do cache e o tempo desde a atualização.

## Arquivos principais
- `frontend_v37.html`
- `worker_v36_cache_15min_fix4.js`

## Observação
A versão v37 reorganiza visualmente os cartões para facilitar leitura rápida e manter o nome completo apenas no frontend.
