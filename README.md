# Painel Aeroportos Brasil

Este repositório contém a versão documentada do painel estático para GitHub Pages.

## Arquivo principal
- `index.html`: página completa com mapa, marcadores clicáveis, tabela de METAR/TAF, filtros e tema claro/escuro.

## Dependências externas
- O painel consulta um Worker da Cloudflare definido em `WORKER_URL` dentro do HTML.
- Não há dependência obrigatória de bibliotecas JavaScript adicionais.

## Como publicar
1. Suba o `index.html` para a raiz do repositório.
2. Mantenha o GitHub Pages apontando para esse branch/pasta.
3. O browser carregará o painel direto do `index.html`.

## Como funciona
- O painel busca `metar` e `taf` no Worker.
- Cada aeroporto vira um card com link de ancoragem.
- Os marcadores no mapa levam até o card correspondente.

## Arquivos opcionais
- `index.html.meta.json`: metadados do arquivo.
- Não é necessário publicar CSV para o site funcionar; coordenadas já estão embutidas no HTML.
