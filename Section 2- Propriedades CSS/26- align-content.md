O `align-content` em CSS 3 controla o espaçamento entre as linhas em um contêiner flexível (ou grid), quando há espaço extra no eixo cruzado (geralmente o eixo vertical). Ele funciona quando há várias linhas de itens e afeta o espaçamento entre essas linhas.

### Propriedades possíveis de `align-content`:
1. **`flex-start`**: As linhas são agrupadas no início do contêiner.
2. **`flex-end`**: As linhas são agrupadas no final do contêiner.
3. **`center`**: As linhas são agrupadas no centro do contêiner.
4. **`space-between`**: As linhas são distribuídas uniformemente, com o primeiro grupo de linhas no início e o último no final.
5. **`space-around`**: As linhas são distribuídas com espaços iguais ao redor de cada linha.
6. **`space-evenly`**: As linhas são distribuídas com espaços iguais entre elas e também nas extremidades.
7. **`stretch`**: As linhas são esticadas para preencher o contêiner.

Aqui está um exemplo em HTML com todos os valores de `align-content`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Align Content Examples</title>
  <style>
    .container {
      display: flex;
      flex-wrap: wrap;
      height: 300px;
      border: 2px solid #000;
      margin-bottom: 20px;
      background-color: #f0f0f0;
    }

    .box {
      width: 80px;
      height: 80px;
      background-color: #e43c5c;
      margin: 5px;
    }

    /* Valor flex-start */
    .flex-start {
      align-content: flex-start;
    }

    /* Valor flex-end */
    .flex-end {
      align-content: flex-end;
    }

    /* Valor center */
    .center {
      align-content: center;
    }

    /* Valor space-between */
    .space-between {
      align-content: space-between;
    }

    /* Valor space-around */
    .space-around {
      align-content: space-around;
    }

    /* Valor space-evenly */
    .space-evenly {
      align-content: space-evenly;
    }

    /* Valor stretch */
    .stretch {
      align-content: stretch;
    }
  </style>
</head>
<body>

  <h1>Exemplos de align-content em CSS</h1>

  <!-- Exemplo 1: flex-start -->
  <h2>align-content: flex-start</h2>
  <div class="container flex-start">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

  <!-- Exemplo 2: flex-end -->
  <h2>align-content: flex-end</h2>
  <div class="container flex-end">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

  <!-- Exemplo 3: center -->
  <h2>align-content: center</h2>
  <div class="container center">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

  <!-- Exemplo 4: space-between -->
  <h2>align-content: space-between</h2>
  <div class="container space-between">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

  <!-- Exemplo 5: space-around -->
  <h2>align-content: space-around</h2>
  <div class="container space-around">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

  <!-- Exemplo 6: space-evenly -->
  <h2>align-content: space-evenly</h2>
  <div class="container space-evenly">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

  <!-- Exemplo 7: stretch -->
  <h2>align-content: stretch</h2>
  <div class="container stretch">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>

</body>
</html>
```

### Explicação dos valores:

1. **`flex-start`**: As linhas de itens são alinhadas no topo do contêiner (o início do eixo cruzado).
2. **`flex-end`**: As linhas de itens são agrupadas na parte inferior do contêiner.
3. **`center`**: As linhas de itens são agrupadas no centro do contêiner.
4. **`space-between`**: O espaço extra entre as linhas é distribuído uniformemente, com a primeira linha no topo e a última na parte inferior.
5. **`space-around`**: Cada linha recebe um espaço igual ao seu redor (espaço antes e depois de cada linha).
6. **`space-evenly`**: O espaço entre as linhas é distribuído de maneira uniforme, incluindo as extremidades.
7. **`stretch`**: As linhas de itens são esticadas verticalmente para preencher o contêiner.

Você pode visualizar como cada valor de `align-content` afeta a disposição e o espaçamento das linhas de itens no contêiner, especialmente em layouts com várias linhas de itens flexíveis.