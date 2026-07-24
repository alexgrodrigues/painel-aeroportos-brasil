# Painel METAR Brasil

Este projeto mostra os aeroportos disponíveis no momento, separados por região geográfica do país.

## Arquivos
- `index.html`: interface responsiva com lista por região, filtros e blocos detalhados.
- `README.md`: documentação do projeto.

## O que a página mostra
- Lista de aeroportos disponíveis no instante da consulta.
- Separação por região: Norte, Nordeste, Centro-Oeste, Sudeste, Sul e Outras.
- Bloco de detalhes com METAR interpretado, TAF interpretado e raw.
- Navegação por âncoras a partir da lista.
- O bloco de cada aeroporto mostra um resumo interpretado do METAR antes do raw.

## Fonte dos dados
- O painel consulta o Worker da Cloudflare definido em `WORKER_URL` dentro do HTML.
- O Worker deve devolver JSON com `metar` e, se existir, `taf`.

## Atualização automática
- A lista é recarregada a cada 15 minutos.
- Há botão de atualização manual.
- Os botões ficam desabilitados durante a consulta e são reativados ao terminar.

## Como publicar no GitHub Pages
1. Coloque `index.html` e `README.md` na raiz do repositório.
2. Ative o GitHub Pages no branch/pasta publicada.
3. Verifique se o Worker responde corretamente.

## Estrutura esperada do retorno
Cada item de `metar` pode conter:
- `icaoId`
- `name`
- `rawOb`
- `fltCat`
- `temp`
- `dewp`
- `visib`
- `clouds`
- `reportTime` ou `receiptTime`

## Observação
- O painel exibe apenas os aeroportos com METAR disponível no retorno do Worker.


## TAF interpretado
- O resumo agora tenta mostrar vento, visibilidade, nuvens e grupos de mudança do TAF antes do raw.


## Versão
- Esta edição é a v15.
