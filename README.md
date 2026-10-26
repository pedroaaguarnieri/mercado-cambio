# Mercado de Câmbio

Painel de cotações de moedas em tempo real, em uma única página HTML, sem build e sem dependências. Mostra os principais pares de câmbio no formato da tabela "Mercados em um piscar de olhos".

**Demo ao vivo:** https://pedroaaguarnieri.github.io/mercado-cambio/

## Recursos

- 10 pares: EUR/USD, GBP/USD, USD/JPY, USD/CHF, AUD/USD, EUR/GBP, EUR/CHF, GBP/JPY, USD/BRL e EUR/BRL
- Colunas: Último, Abertura, Máxima, Mínima, Variação, Variação %, faixa do dia e hora
- Cartões de destaque (USD/BRL, EUR/BRL, EUR/USD, GBP/USD)
- Atualização automática (10, 30 ou 60 s) e botão de atualizar
- O valor pisca em verde ou vermelho quando o preço muda
- Ordenação por qualquer coluna
- Tema claro e escuro (lembra a escolha do usuário)
- Layout responsivo: tabela larga no desktop e cartões empilhados no celular

## Como usar

Abra o `index.html` no navegador. Não precisa de servidor nem de instalação.

Para publicar no GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / `(root)`**.

## Fonte dos dados

As cotações vêm da [AwesomeAPI](https://docs.awesomeapi.com.br/api-de-moedas) (`economia.awesomeapi.com.br`), uma API pública e gratuita com CORS liberado, então a página funciona direto no navegador.

Observações:

- Os valores podem diferir ligeiramente de outras fontes, como o investing.com, e podem ter alguns segundos de atraso.
- A API não informa a abertura do dia. A coluna **Abertura\*** é calculada como `último − variação`, uma aproximação do fechamento anterior.
- Há limite de requisições da API. Evite intervalos de atualização muito curtos.

## Personalização

No começo do `<script>` do `index.html`:

- `PARES`: lista de pares exibidos (formato `["EUR","USD"]`)
- `DESTAQUES`: pares mostrados nos cartões do topo
- `COR`: cor do emblema de cada moeda

## Aviso

Projeto apenas informativo. Não constitui recomendação de investimento.
