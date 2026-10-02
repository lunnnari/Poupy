# Poupy

Protótipo de front-end do Poupy, um site de compras de mercado com layout de celular.
Slogan: "Juntos por um consumo mais inteligente".

## Como abrir

Abra o arquivo `index.html` no navegador (dois cliques). Não precisa instalar nada.

## Telas

Login e cadastro, início, menu lateral, categorias, produtos (com caixa de detalhes),
carrinho, pagamento (PIX, débito e crédito), compra concluída, minhas compras,
favoritos e perfil.

## Ligação com o servidor (PHP/Laravel)

No início do JavaScript, dentro do `index.html`, existe a constante `USAR_SERVIDOR_PHP`.

- `false`: o site apenas simula as respostas do servidor (modo demonstração).
- `true`: o site envia os dados às rotas `/api/...`.

Rotas usadas pela função `enviarAoServidor()`:

- `/login` e `/cadastro`
- `/carrinho/finalizar` (o PHP prepara a área de pagamento)
- `/pagamento` (o PHP processa o pagamento)

A lista `PRODUTOS` do JavaScript deve vir, no projeto final, da tabela de produtos do MySQL.

## Observações

- Nesta versão, qualquer e-mail e senha são aceitos no login.
- Carrinho, favoritos e pedidos ficam guardados no navegador (localStorage).
- Os dados do cartão não são guardados.
