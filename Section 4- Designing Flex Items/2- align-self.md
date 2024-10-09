A propriedade **`align-self`** no CSS Flexbox permite ajustar o alinhamento de um único item flexível de forma diferente dos outros itens dentro do mesmo contêiner flexível. Isso é útil quando você quer que um item específico tenha um comportamento de alinhamento diferente do padrão definido pelo **`align-items`**.

### Sintaxe:

```css
.item {
  align-self: <valor>;
}
```

### Valores Aceitos:

1. **`auto`** (padrão): O item herda o valor do seu contêiner pai.
2. **`flex-start`**: O item é alinhado ao início do eixo cruzado (cross axis).
3. **`flex-end`**: O item é alinhado ao final do eixo cruzado.
4. **`center`**: O item é alinhado ao centro do eixo cruzado.
5. **`baseline`**: O item é alinhado de acordo com a linha de base do conteúdo de texto.
6. **`stretch`**: O item se estende para preencher o contêiner flexível (se não houver uma altura explícita definida).

### Diferença Entre `align-self` e `align-items`:

- **`align-items`**: Define o alinhamento de todos os itens flexíveis dentro de um contêiner.  
- **`align-self`**: Sobrescreve o alinhamento de um item específico, ignorando o valor definido por `align-items`.

---

### Exemplo de Código Explicado:

O código que você forneceu demonstra diferentes comportamentos de alinhamento com a propriedade **`align-self`**.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/alignself.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>align-self</code></h2>

    <!-- Exemplo 1: align-self: flex-start -->
    <code>align-self: flex-start;</code>
    <div class="container outlined">
      <div>1</div>
      <div class="self-start">align-self: flex-start</div>
      <div>3</div>
      <div>4</div>
    </div>

    <!-- Exemplo 2: align-self: flex-end -->
    <code>align-self: flex-end;</code>
    <div class="container outlined">
      <div>1</div>
      <div class="self-end">align-self: flex-end</div>
      <div>3</div>
      <div>4</div>
    </div>

    <!-- Exemplo 3: align-self: center -->
    <code>align-self: center;</code>
    <div class="container outlined">
      <div>1</div>
      <div class="self-center">align-self: center</div>
      <div>3</div>
      <div>4</div>
    </div>

    <!-- Exemplo 4: align-self: stretch -->
    <code>align-self: stretch;</code>
    <div class="container outlined">
      <div>1</div>
      <div class="self-stretch">align-self: stretch</div>
      <div>3</div>
      <div>4</div>
    </div>

    <!-- Exemplo 5: align-self: baseline -->
    <code>align-self: baseline;</code>
    <div class="container outlined baseline">
      <div>1</div>
      <div class="self-baseline">align-self: baseline</div>
      <div class="self-baseline">align-self: baseline</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
    </div>

  </body>
</html>
```

### Explicação de Cada Caso:

#### 1. **`align-self: flex-start`**
```html
<div class="self-start">align-self: flex-start</div>
```
- Esse item (número 2) será alinhado ao **início do eixo cruzado** (por exemplo, o topo da linha).
- Os outros itens seguem o alinhamento padrão do contêiner (ou o valor de `align-items`).

#### 2. **`align-self: flex-end`**
```html
<div class="self-end">align-self: flex-end</div>
```
- O item com `align-self: flex-end` (número 2) será alinhado ao **final do eixo cruzado** (por exemplo, o fundo da linha), enquanto os outros itens não são afetados.

#### 3. **`align-self: center`**
```html
<div class="self-center">align-self: center</div>
```
- O item com `align-self: center` será alinhado ao **centro do eixo cruzado** (por exemplo, centralizado verticalmente no contêiner flexível).

#### 4. **`align-self: stretch`**
```html
<div class="self-stretch">align-self: stretch</div>
```
- Este item (número 2) será **estendido** para preencher toda a altura disponível no eixo cruzado, caso não tenha uma altura definida.

#### 5. **`align-self: baseline`**
```html
<div class="self-baseline">align-self: baseline</div>
```
- Neste caso, o item (ou os itens) são alinhados pela **linha de base** do seu conteúdo de texto. Isso significa que todos os itens dentro do contêiner vão alinhar suas linhas de texto com base em suas respectivas alturas de linha de base.

#### Exemplo `baseline` com diferentes tamanhos de fonte:
- O código CSS a seguir define diferentes tamanhos de fonte para mostrar o comportamento de **alinhamento na linha de base**:
  
  ```css
  .container.baseline div:nth-child(2) {
    font-size: 24px;
  }

  .container.baseline div:nth-child(3) {
    font-size: 14px;
  }

  .container.baseline div:nth-child(4) {
    font-size: 30px;
  }

  .container.baseline div:nth-child(5) {
    font-size: 8px;
  }

  .container.baseline div:nth-child(6) {
    font-size: 50px;
  }
  ```

- Com **`align-self: baseline`**, todos os itens alinharão suas linhas de texto com base no item com o maior tamanho de fonte, no caso o item 6 com `50px`.

---

### Resumo:

- **`align-self`** permite a um item dentro de um contêiner flexível ter um alinhamento individual diferente.
- Os valores comuns para **`align-self`** incluem `flex-start`, `flex-end`, `center`, `stretch`, e `baseline`.
- O comportamento de **`align-self`** pode ser útil quando você deseja que um ou mais itens tenham um alinhamento personalizado sem alterar o comportamento de todo o grupo.