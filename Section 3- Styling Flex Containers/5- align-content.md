A propriedade **`align-content`** em CSS Flexbox controla como várias linhas dentro de um contêiner flexível são distribuídas ao longo do eixo transversal (ou "cross-axis"). Ela afeta o **espaçamento vertical** (se o contêiner for configurado como `flex-direction: row`) ou **espaçamento horizontal** (se configurado como `flex-direction: column`), mas **somente quando há mais de uma linha** de itens flexíveis.

Essa propriedade é importante para controlar o espaço entre e ao redor das linhas em contêineres que usam `flex-wrap` para criar múltiplas linhas. Se o conteúdo estiver em uma única linha, a propriedade `align-content` **não terá efeito**.

## Valores de `align-content`:

1. **`flex-start`**: As linhas de itens flexíveis são empilhadas no início do contêiner (lado superior se `flex-direction` for `row`, lado esquerdo se for `column`), sem espaço extra entre elas.
2. **`flex-end`**: As linhas são empilhadas no final do contêiner (lado inferior ou direito, dependendo da direção), novamente sem espaço extra entre elas.
3. **`center`**: As linhas são centralizadas no eixo transversal, com espaços iguais acima e abaixo (ou nas laterais).
4. **`space-between`**: O espaço entre as linhas é maximizado, com a primeira linha alinhada ao início e a última ao final do contêiner, distribuindo o restante do espaço entre as linhas intermediárias.
5. **`space-around`**: As linhas são distribuídas uniformemente com espaçamento igual ao redor de cada uma, deixando um espaço igual entre as linhas e entre as bordas do contêiner e as primeiras/últimas linhas.
6. **`stretch`** (valor padrão): As linhas se esticam para preencher o espaço disponível. Se o tamanho mínimo das linhas for menor do que o tamanho do contêiner, elas se expandem para ocupar todo o espaço.

## Explicação do Código HTML e CSS

### Código HTML:

```html
<html>
  <head>
      <title>Flexbox Grids</title>
      <link rel="stylesheet" href="css/showcase.css">
      <link rel="stylesheet" href="css/aligncontent.css">
      <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>align-content</code></h2>

    <code>align-content: flex-start;</code>
    <div class="align-start container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>

    <code>align-content: flex-end;</code>
    <div class="align-end container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>

    <code>align-content: center;</code>
    <div class="align-center container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>

    <code>align-content: space-around;</code>
    <div class="align-around container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>

    <code>align-content: space-between;</code>
    <div class="align-between container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>
  </body>
</html>
```

### Código CSS:

```css
body {
  padding: 200px;
}

/* Estilos aplicados aos divs filhos do contêiner */
.container div {
  padding-top: 10px;
  padding-bottom: 10px;
  background-color: lightblue;
  text-align: center;
  margin: 5px;
  width: 50px;
}

.container {
  display: flex;
  flex-wrap: wrap; /* Permite que os itens flexíveis quebrem em múltiplas linhas */
  align-items: flex-start; /* Alinhamento dos itens dentro de cada linha */
}

.align-start {
  align-content: flex-start; /* Linhas agrupadas no topo */
}

.align-end {
  align-content: flex-end; /* Linhas agrupadas no final do contêiner */
}

.align-center {
  align-content: center; /* Linhas centralizadas no meio do contêiner */
}

.align-around {
  align-content: space-around; /* Espaçamento ao redor de cada linha */
}

.align-between {
  align-content: space-between; /* Espaçamento máximo entre as linhas, com a primeira e última encostadas no topo/fundo */
}
```

---

## Explicação Detalhada:

1. **`align-content: flex-start;`**:
   - **Comportamento**: As linhas de itens flexíveis são alinhadas ao início do contêiner. Se houver espaço extra, ele ficará no final do contêiner.
   - **Visualização**: Todas as linhas serão agrupadas no topo.
   ```
   [1] [2] [3] [4] [5] [6] [7] [8]
   [9] [10] [11] [12]
   (Espaço extra em branco abaixo das linhas)
   ```

2. **`align-content: flex-end;`**:
   - **Comportamento**: As linhas são empurradas para o final do contêiner. O espaço extra ficará no topo.
   - **Visualização**: Todas as linhas serão agrupadas na parte inferior.
   ```
   (Espaço extra em branco acima das linhas)
   [1] [2] [3] [4] [5] [6] [7] [8]
   [9] [10] [11] [12]
   ```

3. **`align-content: center;`**:
   - **Comportamento**: As linhas de itens flexíveis são centralizadas no eixo transversal, com espaço igual acima e abaixo.
   - **Visualização**: As linhas estarão no meio do contêiner.
   ```
   (Espaço extra em branco no topo)
   [1] [2] [3] [4] [5] [6] [7] [8]
   [9] [10] [11] [12]
   (Espaço extra em branco abaixo)
   ```

4. **`align-content: space-around;`**:
   - **Comportamento**: O espaço extra é distribuído uniformemente ao redor de cada linha, garantindo que o espaçamento entre as linhas seja o mesmo e que as bordas superior e inferior do contêiner também tenham espaço proporcional.
   - **Visualização**: Espaço uniforme entre e ao redor de cada linha.
   ```
   (Espaço extra)
   [1] [2] [3] [4] [5] [6] [7] [8]
   (Espaço extra)
   [9] [10] [11] [12]
   (Espaço extra)
   ```

5. **`align-content: space-between;`**:
   - **Comportamento**: A primeira linha é alinhada ao início do contêiner e a última ao final, com o espaço restante distribuído igualmente entre as linhas.
   - **Visualização**: Espaço uniforme **somente entre** as linhas, mas sem espaço nas bordas superior ou inferior.
   ```
   [1] [2] [3] [4] [5] [6] [7] [8]
   (Espaço extra entre as linhas)
   [9] [10] [11] [12]
   ```

## Considerações:
- A propriedade `align-content` é útil **quando há várias linhas de itens flexíveis** e você deseja controlar como essas linhas são distribuídas dentro do contêiner.
- Quando só há uma única linha de itens, `align

-content` não terá efeito, e o comportamento será ditado por `align-items`.

Se precisar de mais detalhes ou exemplos específicos, fique à vontade para perguntar!