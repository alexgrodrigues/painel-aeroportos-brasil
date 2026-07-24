# Painel METAR Brasil

Este projeto é um painel responsivo em HTML puro para GitHub Pages.

## O que ele faz
- Mostra um mapa clicável do Brasil.
- Exibe aeroportos com METAR disponível.
- Cada marcador leva ao card do aeroporto.
- Mostra METAR, TAF, vento, visibilidade, teto e temperatura.
- Funciona em celular, tablet e desktop.

## Arquivo principal
- `index.html`

## Fonte dos dados
- O painel consulta o Worker da Cloudflare definido em `WORKER_URL` dentro do HTML.
- O Worker deve devolver JSON com `metar` e, se disponível, `taf`.

## Como publicar no GitHub Pages
1. Coloque `index.html` na raiz do repositório.
2. Ative o GitHub Pages no branch/pasta publicada.
3. Acesse a URL do site e verifique se o Worker responde.

## Estrutura de dados esperada
Cada item de `metar` pode conter campos como:
- `icaoId`
- `name`
- `rawOb`
- `fltCat`
- `temp`
- `dewp`
- `visib`
- `clouds`
- `reportTime` ou `receiptTime`

## Observações
- Não é obrigatório publicar CSV.
- As coordenadas dos aeroportos já estão embutidas no HTML.
- O painel mostra apenas aeroportos com METAR disponível no retorno do Worker.
