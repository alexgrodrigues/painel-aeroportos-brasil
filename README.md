# Histórico de versões

## v27
- Worker compatível com o retorno real da Aviation Weather.
- Frontend consumindo `rows` do Worker.
- Campos de vento, pressão, teto e temperatura preparados para exibição.

## v28
- Worker em modo debug para identificar formato do retorno.
- Adicionado bloco `debug` com contagens dos dados carregados.

## v29
- Frontend com vento dividido em direção e intensidade.
- Campo de vento exibido no card como `Direção` e `Intensidade`.

## v30
- Adicionado campo `Pressão Atmosférica` no painel.
- Alerta para variação brusca de pressão.
- Vento exibido como `Direção` e `Intensidade: YY KT`.

## v31
- Worker consolidado com parsing direto do METAR raw.
- Regex para vento e pressão atmosférica.
- Frontend com cabeçalho `v31`.

## v31.1
- Ajuste no Worker para voltar a extrair corretamente vento e pressão.
- Simplificação da leitura do `METAR raw`.

## v31.2
- Ajuste da temperatura para separar temperatura atual e ponto de orvalho.
- Regex atualizada para o grupo `XX/YY`.

## v32
- Frontend com temperatura em duas linhas: temperatura atual e ponto de orvalho.
- Formato solicitado: `Temperatura Atual: XXºC` e `Ponto de Orvalho: YYºC`.

## v32.1
- Atualização da versão do frontend para `v32.1`.
- Correção do cabeçalho e do título da aba.

## v32.2
- Frontend substituído pelo layout HTML fornecido.
- Mantidos cards de exemplo com SBKP e SBSP.

## v32.3
- Frontend dinâmico consumindo os aeroportos conforme vierem do Worker.
- Remoção dos cards estáticos como única fonte de dados.

## v32.4
- Separação dos aeroportos por região geográfica.
- Ordem das regiões: Sul, Sudeste, Centro-Oeste, Nordeste, Norte.

## v32.5
- Correção das regiões para os ICAOs informados pelo usuário.
- `SBCH` e `SBCO` no Sul.
- `SBJP` e `SBRF` no Nordeste.

## v33
- Worker consolidado com versão `v33`.
- Frontend atualizado para refletir a versão.
- Ajuste das regiões no frontend.

## v33.1
- Correção adicional do mapeamento regional.
- `SBCH` e `SBCO` mantidos no Sul.
- `SBJP` e `SBRF` mantidos no Nordeste.

## v33.2
- Inclusão de aeroportos das capitais faltantes no Centro-Oeste e Nordeste.
- Adição de aeroportos como Brasília, Goiânia, Campo Grande, Cuiabá, Fortaleza, Salvador, Recife, João Pessoa, Natal, Teresina, São Luís, Aracaju e Maceió.

## v34
- Worker atualizado com capitais do Norte e Nordeste faltantes.
- Frontend alinhado para versão `v34`.

## v34.1
- Correção da lista do Worker para incluir `SBGO`, `SBCY` e `SBCG`.

## v35
- Inclusão de Manaus (`SBEG`) no Worker.
- Frontend atualizado para `v35`.

## v35.1
- Correção da lista do Worker com aeroportos faltantes.
- Ajustes para `SBMO`, `SBFZ`, `SBCY`, `SBBR`, `SBCG`, `SBRF`, `SBRP`, `SBMA`, `SBAR`, `SBBE` e `SBEG`.

## v35.2
- Correção regional de `SBRP`, que passou a ficar no Sudeste.
