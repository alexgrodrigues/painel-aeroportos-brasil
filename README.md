# README v31

## Objetivo

Esta versão consolida o painel com pressão atmosférica, vento separado em direção e intensidade, e cabeçalho atualizado para v31.

## O que o Worker faz

- Lê o `METAR raw`.
- Extrai o vento com regex.
- Extrai o QNH (`Qxxxx`) do METAR.
- Gera alerta se a pressão estiver fora da faixa esperada.

## O que o frontend mostra

- Direção.
- Intensidade.
- Pressão Atmosférica.
- Visibilidade.
- Teto.
- Temperatura.

## Arquivos finais

- `worker_v31.js`
- `frontend_v31.html`
- `README_v31.md`
