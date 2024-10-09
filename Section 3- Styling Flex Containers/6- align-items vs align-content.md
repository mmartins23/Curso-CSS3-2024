A diferença entre as propriedades **`align-items`** e **`align-content`** no CSS Flexbox está no contexto em que cada uma delas atua e o tipo de alinhamento que controlam. Vamos explorar cada uma em detalhe, com exemplos de código para ilustrar as diferenças.

---

### 1. **`align-items`**:
A propriedade **`align-items`** controla o **alinhamento de itens individuais** dentro de uma **única linha** ao longo do eixo transversal (ou cross-axis). Isso afeta como cada item dentro de uma linha é posicionado verticalmente (ou horizontalmente, se a direção do `flex-direction` for `column`).

- Atua **em cada item** de uma única linha.
- Aplica-se a **todo o conteúdo dentro do contêiner**.

#### Valores Comuns de `align-items`:
- **`flex-start`**: Alinha os itens ao início do contêiner.
- **`flex-end`**: Alinha os itens ao final do contêiner.
- **`center`**: Centraliza os itens dentro do contêiner.
- **`stretch`** (padrão): Estica os itens para preencher o espaço restante ao longo do eixo transversal.
- **`baseline`**: Alinha os itens com base na linha de base do conteúdo.

#### Exemplo de Código:

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .container {
      display: flex;
      height: 200px;
      background-color: lightgray;
    }

    .item {
      width: 100px;
      background-color: lightblue;
      margin: 5px;
    }

    .align-start {
      align-items: flex-start; /* Itens alinhados ao topo */
    }

    .align-center {
      align-items: center; /* Itens centralizados verticalmente */
    }

    .align-end {
      align-items: flex-end; /* Itens alinhados ao fundo */
    }

    .align-stretch {
      align-items: stretch; /* Itens esticados para preencher a altura */
    }
  </style>
</head>
<body>

  <h3>align-items: flex-start</h3>
  <div class="container align-start">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
  </div>

  <h3>align-items: center</h3>
  <div class="container align-center">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
  </div>

  <h3>align-items: flex-end</h3>
  <div class="container align-end">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
  </div>

  <h3>align-items: stretch (default)</h3>
  <div class="container align-stretch">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
  </div>

</body>
</html>
```

#### Explicação:
- **`align-items: flex-start`**: Os itens são alinhados ao início (topo) do contêiner.
- **`align-items: center`**: Os itens são centralizados verticalmente.
- **`align-items: flex-end`**: Os itens são alinhados ao final (fundo) do contêiner.
- **`align-items: stretch`**: Os itens se esticam para preencher a altura total do contêiner, ajustando-se automaticamente ao espaço disponível.

---

### 2. **`align-content`**:
A propriedade **`align-content`** controla o alinhamento do **conjunto de linhas de itens** em um contêiner flexível quando o `flex-wrap` está ativado e há várias linhas de itens. Ela define o espaçamento entre as **linhas inteiras** (não os itens individuais).

- Atua **nas linhas de itens flexíveis** dentro do contêiner.
- Só tem efeito quando há **múltiplas linhas** (ou seja, quando `flex-wrap` está ativo).

#### Valores Comuns de `align-content`:
- **`flex-start`**: Alinha as linhas ao início do contêiner.
- **`flex-end`**: Alinha as linhas ao final do contêiner.
- **`center`**: Centraliza as linhas dentro do contêiner.
- **`space-between`**: Distribui o espaço igualmente entre as linhas, com a primeira linha no topo e a última no fundo.
- **`space-around`**: Distribui o espaço ao redor de cada linha.
- **`stretch`**: As linhas se expandem para preencher todo o espaço disponível.

#### Exemplo de Código:

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .container {
      display: flex;
      flex-wrap: wrap; /* Permite que os itens quebrem em múltiplas linhas */
      height: 200px;
      background-color: lightgray;
    }

    .item {
      width: 100px;
      height: 50px;
      background-color: lightblue;
      margin: 5px;
    }

    .align-start {
      align-content: flex-start; /* Linhas alinhadas ao topo */
    }

    .align-center {
      align-content: center; /* Linhas centralizadas verticalmente */
    }

    .align-end {
      align-content: flex-end; /* Linhas alinhadas ao fundo */
    }

    .align-space-between {
      align-content: space-between; /* Espaço distribuído entre as linhas */
    }

    .align-space-around {
      align-content: space-around; /* Espaço ao redor das linhas */
    }
  </style>
</head>
<body>

  <h3>align-content: flex-start</h3>
  <div class="container align-start">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
  </div>

  <h3>align-content: center</h3>
  <div class="container align-center">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
  </div>

  <h3>align-content: flex-end</h3>
  <div class="container align-end">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
  </div>

  <h3>align-content: space-between</h3>
  <div class="container align-space-between">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
  </div>

  <h3>align-content: space-around</h3>
  <div class="container align-space-around">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
  </div>

</body>
</html>
```

#### Explicação:
- **`align-content: flex-start`**: As linhas de itens são alinhadas ao início (topo) do contêiner.
- **`align-content: center`**: As linhas são centralizadas dentro do contêiner.
- **`align-content: flex-end`**: As linhas de itens são alinhadas ao final (fundo) do contêiner.
- **`align-content: space-between`**: O espaço é distribuído entre as linhas de itens, com a primeira linha no topo e a última no fundo.
- **`align-content: space-around`**: O espaço é distribuído ao redor de cada linha de itens, criando espaço antes da primeira linha e depois da última linha.

---

### Resumo das Diferenças:
- **`align-items`**: Alinha os itens **dentro de uma única linha** ao longo do eixo transversal. Afeta como os itens são posicionados **verticalmente (ou horizontalmente)** dentro de uma linha.
- **`align-content`**: Alinha **múltiplas linhas** dentro de um contêiner flexível, controlando o espaçamento **entre as linhas** quando o `flex-wrap` está ativado. Afeta o **espaçamento entre linhas**.

Essas duas propriedades atuam em níveis diferentes do layout, com `align-items` afetando os itens individuais em uma única linha e `

align-content` lidando com o alinhamento das linhas dentro do contêiner.