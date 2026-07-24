# README v36.7

## Projeto
Painel METAR com Worker e frontend para consulta de aeroportos na América do Sul, com dados de METAR, TAF, estação e exibição responsiva.

## Alterações incluídas até a v36.7
- Worker com cache de 15 minutos.
- Parser de METAR extraindo vento, direção, intensidade, pressão, temperatura, visibilidade e teto a partir da string bruta.
- Suporte para leitura combinada de METAR, TAF e stationinfo para preencher aeroportos que não vierem completos em um único endpoint.
- Tratamento de `CAVOK` em visibilidade e teto.
- Frontend mostrando a hora do METAR ao lado do nome do aeroporto quando disponível.
- Frontend com nome completo dos aeroportos e cidade.
- Identificação da versão no topo da página como v36.7.

## Arquivos principais
- `worker_v36_cache_15min_fix4.js`
- `frontend_v36.7.html`

## Observações técnicas
A API da Aviation Weather foi atualizada em 2025 e os endpoints usados no projeto seguem o padrão `/api/data/metar`, `/api/data/taf` e `/api/data/stationinfo` com `format=json`.

## Status atual
A versão v36.7 foi ajustada para exibir os dados no frontend com o nome completo, cidade e horário do METAR quando houver informação disponível.
