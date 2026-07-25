# README v36.7

## Projeto
Painel de Principais Aeroportos Mercosul com METAR, TAF e dados de estação, otimizado para Cloudflare Workers.

## Identificação da versão
A interface principal foi reidentificada como **Principais Aeroporto Mercosul v36.7**.

## Correções incluídas
- Botão de atualizar ajustado para forçar nova leitura dos dados.
- Frontend com cache-busting por query string ao atualizar.
- Título da página alinhado com a versão v36.7.
- Mantido o suporte ao nome completo dos aeroportos, cidade e horário do METAR.
- Mantido o backend com cache de 15 minutos.

## Arquivos
- `frontend_v36_7_fixed.html`
- `worker_v36_cache_15min_fix4.js`

## Observações
O botão de atualização agora dispara uma nova busca com parâmetro de tempo para evitar reaproveitamento indevido de cache do navegador.

## Status
A versão v36.7 representa a correção de identificação da página e do botão de atualização.
