# README v27

## Objetivo

Esta versão corrige a leitura real do retorno da Aviation Weather e atualiza o frontend para renderizar os aeroportos corretamente.

## Mudanças principais

- Worker atualizado para ler `icaoId`, `rawOb`, `rawTAF` e `fltCat`.
- Worker agora retorna `rows` com dados prontos para o frontend.
- Frontend atualizado para consumir a URL correta do Worker.
- Interface marcada como versão `v27`.

## Arquivos

- `worker_v27.js`.
- `frontend_v27.html`.

## Campos usados pelo Worker

- `icaoId`.
- `rawOb`.
- `rawTAF`.
- `fltCat`.
- `name`.
- `city`.
- `state`.
- `country`.

## O que o frontend mostra

- ICAO.
- Nome.
- Categoria.
- Vento.
- Visibilidade.
- Teto.
- Temperatura.
- METAR raw.
- TAF raw.
- TAF interpretado.
- Tendência do TAF.
- Alerta do TAF.

## Como aplicar

1. Substitua o Worker pelo conteúdo de `worker_v27.js`.
2. Substitua o frontend pelo conteúdo de `frontend_v27.html`.
3. Publique os dois.
4. Recarregue a página.

## Observação

Se algum aeroporto ainda não aparecer, o problema tende a ser o retorno da API naquele ICAO específico, não o card do frontend.
