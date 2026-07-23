[README.md](https://github.com/user-attachments/files/30326404/README.md)
# Painel web de aeroportos do Brasil

Este projeto abre no navegador e busca todos os aeroportos brasileiros online com METAR disponível, além do TAF quando existir, usando a API pública do Aviation Weather Center.

## Arquivos

### `painel-aeroportos-brasil.html`
Arquivo principal da aplicação.

Funções:
- busca METAR em JSON;
- busca TAF em JSON;
- busca metadados de estações/aeroportos;
- filtra ICAOs do Brasil pelos prefixos `SB`, `SD`, `SI`, `SJ` e `SN`;
- calcula categoria `VFR`, `MVFR`, `IFR` e `LIFR`;
- mostra tabela operacional;
- mostra cards detalhados por aeroporto;
- permite filtro por texto, categoria, prefixo ICAO e ordenação;
- atualiza automaticamente a cada 15 minutos.

### `README.md`
Este arquivo de instruções.

## Como usar

### Opção 1: abrir localmente com um servidor simples

Por causa de políticas de CORS e segurança do navegador, o ideal é abrir o HTML através de um servidor local, e não com duplo clique em `file:///`.

#### Com Python

Se você tiver Python instalado:

```bash
cd brasil-metar-web
python -m http.server 8080
```

Depois abra no navegador:

[http://localhost:8080/painel-aeroportos-brasil.html](http://localhost:8080/painel-aeroportos-brasil.html)

#### Com VS Code Live Server

1. Abra a pasta `brasil-metar-web` no VS Code.
2. Instale a extensão **Live Server**.
3. Clique com o botão direito em `painel-aeroportos-brasil.html`.
4. Escolha **Open with Live Server**.

### Opção 2: publicar em hospedagem estática

Você também pode subir o arquivo em:
- GitHub Pages;
- Netlify;
- Vercel;
- qualquer servidor web estático.

Nesse caso, basta publicar o arquivo HTML e acessar pela URL gerada.

## Como funciona no browser

1. Ao abrir a página, o JavaScript chama três endpoints públicos do Aviation Weather Center.
2. O app baixa METAR, TAF e informações de estação.
3. Ele mantém apenas aeroportos brasileiros que estejam online no momento.
4. Depois calcula a categoria operacional e preenche a tabela e os cards.
5. A atualização automática roda a cada 15 minutos.

## Filtros disponíveis

- **Busca textual**: ICAO, cidade ou trecho do METAR.
- **Categoria**: todas, VFR, MVFR, IFR, LIFR.
- **Prefixo ICAO**: SB, SD, SI, SJ, SN.
- **Ordenação**: pior categoria, ICAO, cidade ou horário.

## Observações importantes

- A lista exibida depende do que estiver online na API no momento da consulta.
- Alguns aeroportos terão METAR mas não TAF.
- Se o navegador bloquear a chamada por CORS, rode a página via servidor local ou publique em hospedagem estática.
- O painel não precisa de backend próprio; tudo roda no navegador.

## Personalizações fáceis

Você pode editar o HTML para:
- mudar o intervalo do auto-refresh;
- trocar os prefixos filtrados;
- destacar apenas IFR/LIFR;
- exportar a tabela para CSV;
- adicionar mapa com Leaflet;
- agrupar por estado ou região.
