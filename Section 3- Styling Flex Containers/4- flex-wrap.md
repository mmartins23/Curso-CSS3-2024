A propriedade `flex-wrap` em CSS Flexbox define como os itens flexíveis (os filhos do contêiner flex) devem se comportar quando não cabem em uma única linha (ou coluna, dependendo do valor de `flex-direction`). Isso permite que os itens se **quebrem** em múltiplas linhas ou colunas dentro do contêiner.

## Valores de `flex-wrap`:

1. **`nowrap` (padrão)**:
   - Todos os itens flexíveis são colocados em uma única linha, mesmo que isso faça com que eles saiam do contêiner. Se os itens não cabem, o Flexbox ainda tentará encolher os itens para encaixá-los, sem permitir a quebra para uma nova linha.

2. **`wrap`**:
   - Os itens flexíveis são dispostos em múltiplas linhas (ou colunas, se `flex-direction` for `column`). Quando o espaço do contêiner se esgota, os itens sobem ou descem para uma nova linha.

3. **`wrap-reverse`**:
   - Funciona de forma similar a `wrap`, mas as linhas ou colunas adicionais são organizadas em ordem inversa. Ou seja, o Flexbox começa a adicionar as novas linhas **de baixo para cima** ou **da direita para a esquerda**, dependendo do eixo.

## Explicação do Código HTML e CSS

### Código HTML:

```html
<html>
  <head>
      <title>Flexbox Grids</title>
      <link rel="stylesheet" href="css/showcase.css">
      <link rel="stylesheet" href="css/flexwrap.css">
      <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>flex-wrap</code></h2>

    <code>flex-wrap: nowrap;</code>
    <div class="nowrap container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>

    <code>flex-wrap: wrap;</code>
    <div class="wrap container outlined">
      <div>1</div> <div>2</div> <div>3</div> <div>4</div>
      <div>5</div> <div>6</div> <div>7</div> <div>8</div>
      <div>9</div> <div>10</div> <div>11</div> <div>12</div>
    </div>

    <code>flex-wrap: wrap-reverse;</code>
    <div class="wrap-reverse container outlined">
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

.container {
  display: flex;
  margin-bottom: 50px;
  border: 1px solid #ddd;
  padding: 10px;
}

.outlined div {
  background-color: lightblue;
  margin: 5px;
  text-align: center;
  padding: 20px;
  width: 50px;
}

/* Alinhamentos usando flex-wrap */
.nowrap {
  flex-wrap: nowrap; /* Não permite quebra de linha */
}

.wrap {
  flex-wrap: wrap; /* Permite quebra de linha quando necessário */
}

.wrap-reverse {
  flex-wrap: wrap-reverse; /* Permite quebra de linha, mas no sentido inverso */
}
```

---

## Explicação Detalhada:

1. **`flex-wrap: nowrap;`**:
   - **Comportamento**: Os itens dentro do contêiner flex são todos dispostos em uma única linha, independentemente do espaço disponível. Se não houver espaço suficiente, os itens continuarão na mesma linha e podem transbordar o contêiner.
   - **Uso**: Este é o comportamento padrão do Flexbox e é útil quando você quer garantir que todos os itens flexíveis permaneçam na mesma linha.

   **Visualização**:
   ```
   [1] [2] [3] [4] [5] [6] [7] [8] [9] [10] [11] [12]
   (Todos os itens na mesma linha, mesmo que saiam do contêiner)
   ```

2. **`flex-wrap: wrap;`**:
   - **Comportamento**: Quando os itens flexíveis atingem a largura máxima do contêiner, eles são movidos para a próxima linha. Isso impede que os itens transbordem e facilita a visualização dos elementos sem sobreposição.
   - **Uso**: Ideal quando você deseja garantir que todos os itens sejam exibidos dentro do contêiner e permitir que o layout se ajuste automaticamente.

   **Visualização**:
   ```
   [1] [2] [3] [4] [5] [6] [7] [8]
   [9] [10] [11] [12]  (Itens distribuídos em duas ou mais linhas)
   ```

3. **`flex-wrap: wrap-reverse;`**:
   - **Comportamento**: Semelhante ao `wrap`, mas o Flexbox organiza os itens em múltiplas linhas no **sentido inverso**. Se `flex-direction: row`, as novas linhas são criadas **de baixo para cima**.
   - **Uso**: Pode ser útil em layouts onde você deseja exibir os itens a partir da linha inferior, como em algumas interfaces de usuário onde os elementos mais recentes são mostrados na parte inferior.

   **Visualização**:
   ```
   [9] [10] [11] [12] 
   [1] [2]  [3]  [4]  [5] [6] [7] [8]  (Linhas começando de baixo para cima)
   ```

---

## Exemplo de Comportamento Visual:

### `nowrap`:
Todos os itens tentam caber em uma única linha:
```
[1] [2] [3] [4] [5] [6] [7] [8] [9] [10] [11] [12]
(Se não houver espaço suficiente, alguns itens podem "vazar" para fora da tela)
```

### `wrap`:
Os itens são movidos para a próxima linha quando o espaço do contêiner acabar:
```
[1] [2] [3] [4] [5] [6] [7] [8]
[9] [10] [11] [12]
(Distribuídos em várias linhas)
```

### `wrap-reverse`:
Os itens são movidos para a próxima linha, mas de baixo para cima:
```
[9] [10] [11] [12]
[1] [2]  [3]  [4]  [5] [6] [7] [8]
(Linhas criadas de baixo para cima)
```

---

## Considerações:
- **Espaço Responsivo**: A propriedade `flex-wrap` é extremamente útil em layouts responsivos, pois permite que os itens se ajustem automaticamente ao espaço disponível, sem a necessidade de definir tamanhos específicos.
- **Comportamento Padrão**: O valor padrão é `nowrap`, o que significa que os itens permanecerão em uma única linha até que sejam forçados a sair do contêiner.

Este código demonstra claramente como o Flexbox pode ser usado para controlar o fluxo e a organização dos itens em um layout, permitindo uma melhor experiência visual e controle do design, especialmente quando trabalhamos com múltiplas resoluções e tamanhos de tela.