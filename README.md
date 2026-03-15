# 🍫 Feira de Páscoa Florybal Osório

Projeto de catálogo web para divulgação e organização dos produtos da Feira de Páscoa Florybal em Osório.  
O site foi pensado para ser simples de atualizar, visualmente agradável e fácil de navegar tanto no celular quanto no desktop.

## ✨ O que este projeto faz

- Exibe o catálogo de produtos por categoria
- Lê os produtos diretamente do arquivo `dados-produtos.json`
- Gera categorias dinamicamente com base no JSON
- Permite busca por produto
- Mostra carrinho e finalização por WhatsApp
- Controla visibilidade de itens com `temEstoque`

## 🧁 Categorias do catálogo

Atualmente o projeto organiza os produtos em categorias como:

- `Ao leite`
- `Branco`
- `Diversos`
- `Infantil`
- `Cestas`
- `Meio amargo`
- `70% cacau`
- `Diet`
- `Soja`

As categorias não ficam fixas no HTML: elas são montadas com base no conteúdo do JSON.

## 🗂️ Estrutura principal

```text
.
├── index.html
├── css/
│   └── style.css
├── js/
│   └── carregar-dados.js
├── assets/
│   ├── chocolates/
│   ├── imgs/
│   ├── logo.png
│   └── sem-imagem.png
└── dados-produtos.json
```

## 📦 Como os produtos são cadastrados

Cada produto fica dentro de uma categoria no arquivo `dados-produtos.json`.

Exemplo:

```json
{
  "descricao": "Ovo ao Leite 300g",
  "preco": 108,
  "imagem": "./assets/chocolates/ao-leite/ovo-300g.webp",
  "desconto": 88,
  "temEstoque": true
}
```

### Significado dos campos

- `descricao`: nome exibido no site
- `preco`: preço base do produto
- `imagem`: caminho da foto
- `desconto`: preço promocional, quando existir
- `temEstoque`: controla se o item aparece ou não no site

## 🛠️ Regras importantes de manutenção

- Se `temEstoque` estiver como `true`, o produto aparece no catálogo
- Se `temEstoque` estiver como `false`, o produto fica oculto
- Quando não houver foto correta, use `./assets/sem-imagem.png`
- Sempre que possível, mantenha a imagem na pasta da categoria correspondente
- Produtos como bombons e drágeas devem ficar em `Diversos`

## 🖼️ Organização das imagens

As imagens ficam em `assets/chocolates/`, separadas por tipo de chocolate ou grupo de produtos.

Exemplos:

- `assets/chocolates/ao-leite/`
- `assets/chocolates/branco/`
- `assets/chocolates/diversos/`
- `assets/chocolates/infantil/`
- `assets/chocolates/cesta/`

Quando novas fotos chegam em pasta temporária, o ideal é:

1. mover para a pasta definitiva correta
2. renomear de forma clara
3. atualizar o caminho no `dados-produtos.json`

## 🚀 Como abrir o projeto

Como este é um projeto estático, basta abrir o `index.html` no navegador.

Se preferir rodar com servidor local.

## 💡 Objetivo do projeto

Este projeto existe para facilitar a divulgação dos produtos da feira, acelerar o atendimento e deixar a atualização do catálogo muito mais prática durante a temporada de Páscoa. 🐰🍬

## ❤️ Melhorias futuras

- painel simples para editar produtos sem mexer no JSON
- filtros por peso, tipo e faixa de preço
- destaque visual para promoções
- controle de estoque mais detalhado
- importação automática a partir de planilhas

## 📱 Fluxo do cliente

1. A pessoa acessa o catálogo
2. Busca ou navega pelas categorias
3. Adiciona produtos ao carrinho
4. Finaliza o pedido pelo WhatsApp
