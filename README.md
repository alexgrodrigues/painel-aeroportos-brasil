# Principais Aeroportos Mercosul

Este projeto exibe METAR, TAF e dados interpretados de aeroportos do Brasil e de países do Mercosul em uma interface web leve.

## Versão atual

**v38.21**

## Atualizações desde a v37

### v38
- Inclusão do bloco de TAF interpretado na interface.
- Exibição da base do TAF e das evoluções previstas.
- Suporte a cartões com destaque visual para condições severas.
- Melhorias na leitura e na exibição de METAR e TAF.
- Adição de novos aeroportos e refinamentos de blocos regionais.
- Ajustes no carregamento com atualização manual via botão.

### v38.1 a v38.9
- Revisões na estrutura do frontend para manter o carregamento estável.
- Inclusão da classe CSS `alerta-severo` para destacar condições críticas.
- Aplicação dinâmica da classe no card do aeroporto quando o TAF indicar risco severo.
- Refinos na exibição de TAF interpretado e evoluções previstas.

### v38.10 a v38.14
- Correção do carregamento do frontend.
- Ajustes no botão Atualizar para forçar nova requisição e evitar cache.
- Inclusão de parâmetros de bypass de cache na URL do Worker.
- Mensagens de status atualizadas durante o recarregamento.

### v38.15 a v38.21
- Inclusão de aeroportos adicionais no frontend e no Worker.
- Ajuste do aeroporto de Petrolina para a região Nordeste.
- Inclusão de Rio Branco, Palmas, Boa Vista, Porto Velho, Belém, Teresina e Natal/SBSG conforme o mapeamento correto.
- Correção de classificação regional para SBPE, SBBE e demais aeroportos.
- Ajuste do subtítulo da página para refletir a versão correta.
- Refinamento da lista de ICAOs e nomes completos dos aeroportos.

## Arquivos principais

- `index.html`: interface principal.
- `worker.js`: coleta e entrega dos dados meteorológicos.

## Observações

- O Worker utiliza a API de meteorologia aeronáutica para buscar METAR, TAF e station info.
- O frontend foi ajustado para lidar com mudanças de estrutura nos dados e evitar perda de exibição.
- As versões mais recentes priorizam estabilidade, carregamento consistente e destaque de alertas.

## Estrutura de exibição

- **METAR**: texto bruto da observação.
- **TAF**: texto bruto da previsão.
- **TAF Interpretado**: resumo da base da previsão.
- **Evoluções Previstas**: grupos de tendência como `BECMG`, `TEMPO`, `PROB` e `FM`.

## Aeroportos adicionados ou ajustados

- **SBSG** — São Gonçalo do Amarante - Governador Aluízio Alves (Natal).
- **SBTI** — Aeroporto de Teresina - Senador Petrônio Portela.
- **SBPE** — Petrolina, agora na região Nordeste.
- **SBBE** — Belém, corretamente classificado no Norte.
- **SBFI** — Foz do Iguaçu, incluído na região Sul.
- **SBEI** — Rio Branco - Plácido de Castro.
- **SBPJ** — Palmas - Brigadeiro Lysias Rodrigues.
- **SBBV** — Boa Vista - Atlas Brasil Cantanhede.
- **SBPV** — Porto Velho - Governador Jorge Teixeira de Oliveira.

## Histórico resumido

- A partir da v37, o projeto passou por expansão visual e funcional.
- As versões v38 introduziram interpretação de TAF, alertas severos, ajustes de cache e novas localidades.
- A v38.21 consolidou a divisão regional correta e estabilizou o carregamento do frontend.

## Uso

1. Abrir o arquivo HTML no navegador.
2. O Worker entrega os dados JSON consumidos pela interface.
3. Use o botão Atualizar para forçar uma nova consulta.
