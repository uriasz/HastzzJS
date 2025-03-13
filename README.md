
![fce40ca2e744285c92ba397cc5ef2354-ezgif com-resize](https://github.com/user-attachments/assets/2f161953-bb53-4044-80e6-1b33c20bf2f3)

# Sistema de Produtos

Este projeto contém um conjunto de funções que operam em um array de produtos. Cada função tem um objetivo específico, como imprimir os produtos, filtrar os produtos por categoria ou aplicar descontos, entre outros. Abaixo, explicaremos como cada função funciona detalhadamente para que qualquer pessoa, mesmo sem conhecimento técnico, consiga entender.

## Estrutura do Projeto

O código contém um array de produtos, onde cada produto tem as seguintes informações:
- `id`: Identificador único do produto.
- `name`: Nome do produto.
- `price`: Preço do produto.
- `category`: Categoria do produto (ex: "Games", "Livros").
- `discount`: Desconto aplicável ao produto (caso tenha).
- `amount`: Quantidade de produtos disponíveis em estoque.

## Funções

### 1. **getPriceWithDiscount(product)**

Esta função é usada para calcular o preço do produto com desconto, caso ele tenha. Se o produto tiver um desconto, ela calcula o preço com base na porcentagem do desconto. Se não houver desconto, ela apenas retorna o preço original do produto.

#### Como funciona:
- Se o produto tiver um desconto (`discount > 0`), a função calcula o preço com desconto.
- Caso contrário, a função retorna o preço original do produto.

### 2. **filterProducts(products, conditionFn)**

Esta função é responsável por filtrar os produtos de acordo com uma condição fornecida. A condição é passada como uma função, e ela define quais produtos serão retornados. Essa função é reutilizada por outras funções, ajudando a evitar repetição de código.

#### Como funciona:
- A função recebe dois parâmetros:
  - `products`: O array de produtos.
  - `conditionFn`: Uma função que define a condição de filtragem (ex: filtrar produtos com desconto).
- A função retorna um novo array de produtos que atendem à condição dada.

### 3. **printProducts(products)**

Essa função imprime todos os produtos no console, mostrando o nome, a categoria e o preço (com ou sem desconto, se houver). Se o produto estiver em promoção, a palavra "(PROMOÇÃO)" será exibida.

#### Como funciona:
- A função usa `forEach` para percorrer todos os produtos do array.
- Para cada produto, ela exibe o nome, categoria e preço (com ou sem desconto) no console.

### 4. **printDiscountedProducts(products)**

Essa função imprime no console todos os produtos que têm algum desconto. Ela usa a função `filterProducts` para filtrar os produtos com desconto e, em seguida, exibe o nome do produto e o preço com desconto.

#### Como funciona:
- A função usa `filterProducts` para obter os produtos com desconto.
- Depois, usa `forEach` para imprimir o nome e preço com desconto de cada produto.

### 5. **printGamesProducts(products)**

Essa função imprime no console todos os produtos da categoria "Games". Ela utiliza `filterProducts` para filtrar os produtos dessa categoria e, em seguida, imprime o nome de cada um deles.

#### Como funciona:
- A função usa `filterProducts` para filtrar os produtos que pertencem à categoria "Games".
- Em seguida, imprime o nome de cada produto dessa categoria.

### 6. **printDiscountedBooks(products)**

Esta função imprime no console todos os produtos da categoria "Livros" que estão em promoção (com desconto). Ela também utiliza `filterProducts` para filtrar esses produtos e depois imprime o nome e o preço com desconto.

#### Como funciona:
- A função usa `filterProducts` para filtrar os livros que estão com desconto.
- Depois, imprime o nome e o preço com desconto de cada livro.

### 7. **printOutOfStockProducts(products)**

Esta função imprime no console todos os produtos que estão fora de estoque (ou seja, `amount === 0`). Ela usa `filterProducts` para filtrar esses produtos e, em seguida, imprime o nome de cada um.

#### Como funciona:
- A função usa `filterProducts` para filtrar os produtos que estão fora de estoque (quantidade igual a zero).
- Em seguida, imprime o nome de cada produto sem estoque.

### 8. **printTotalStockAmount(products)**

Essa função calcula e imprime no console a quantidade total de todos os produtos no estoque. Ela soma o valor do estoque de cada produto e exibe o total.

#### Como funciona:
- A função usa `reduce` para somar o valor de `amount` de todos os produtos.
- O total é então impresso no console.

### 9. **printMostExpensiveProduct(products)**

Essa função encontra o produto mais caro e imprime o nome e o preço no console.

#### Como funciona:
- A função usa `reduce` para comparar os preços de todos os produtos e encontrar o produto mais caro.
- Depois, imprime o nome e o preço do produto mais caro.

### 10. **printMostExpensiveBook(products)**

Esta função encontra o livro mais caro (da categoria "Livros") e imprime seu nome e preço no console.

#### Como funciona:
- A função usa `filter` para filtrar os produtos da categoria "Livros".
- Depois, usa `reduce` para comparar os preços dos livros e encontrar o mais caro.
- Finalmente, imprime o nome e o preço do livro mais caro.

---

## Como Executar o Código

1. Abra o arquivo HTML no seu navegador.
2. Abra o console do navegador para ver os resultados das funções sendo executadas. Para abrir o console:
   - No Google Chrome, pressione `Ctrl+Shift+I` (Windows/Linux) e clique na aba "Console".
3. Quando o arquivo for carregado, as funções serão executadas automaticamente, e você verá os resultados no console do navegador.

