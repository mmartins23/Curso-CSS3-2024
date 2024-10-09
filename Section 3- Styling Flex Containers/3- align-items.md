A propriedade `align-items` no CSS Flexbox é usada para alinhar os itens ao longo do **eixo transversal** (cross axis), que é perpendicular ao **eixo principal** (main axis). O eixo transversal é determinado pelo `flex-direction`:

- Se `flex-direction: row`, o eixo transversal é **vertical**.
- Se `flex-direction: column`, o eixo transversal é **horizontal**.

`align-items` controla como os itens flexíveis são distribuídos ao longo deste eixo, permitindo que eles sejam alinhados no topo, no meio, no final ou estendidos ao longo do eixo transversal.

## Valores Comuns de `align-items`

1. **`flex-start`**:
   - Alinha os itens no início do eixo transversal (normalmente no topo, se o `flex-direction` for `row`).

2. **`flex-end`**:
   - Alinha os itens no final do eixo transversal (normalmente na parte inferior, se o `flex-direction` for `row`).

3. **`center`**:
   - Centraliza os itens ao longo do eixo transversal.

4. **`stretch`** (padrão):
   - Estende os itens para preencher todo o eixo transversal. Esse comportamento só ocorre se os itens não tiverem uma altura ou largura definida.

5. **`baseline`**:
   - Alinha os itens de acordo com a **linha de base** do conteúdo de texto. Este é um valor útil quando você tem itens de diferentes tamanhos de fonte ou altura.

---

## Código HTML e CSS Explicado

### Código HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/alignment.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
</head>
<body>

    <h2>Property: <code>align-items</code></h2>

    <code>align-items: flex-start;</code>
    <div class="align-start container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>align-items: flex-end;</code>
    <div class="align-end container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>align-items: center;</code>
    <div class="align-center container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>align-items: stretch;</code>
    <div class="align-stretch container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>align-items: baseline;</code>
    <div class="align-baseline container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

</body>
</html>
```

### Código CSS:

```css
/* Estilos básicos para os contêineres flex */
.container {
  display: flex;  /* Torna o contêiner flexível usando Flexbox */
  margin-bottom: 30px;
  border: 1px solid #ddd;
  padding: 10px;
}

.outlined div {
  padding: 20px;
  background-color: lightblue;
  margin: 5px;
  text-align: center;
  font-size: 20px;
  width: 50px;
}

/* Alinhamento dos itens usando diferentes valores de align-items */
.align-start {
  align-items: flex-start; /* Alinha os itens no início (topo) */
}

.align-end {
  align-items: flex-end; /* Alinha os itens no final (parte inferior) */
}

.align-center {
  align-items: center; /* Centraliza os itens ao longo do eixo transversal */
}

.align-stretch {
  align-items: stretch; /* Estica os itens ao longo do eixo transversal */
}

.align-baseline {
  align-items: baseline; /* Alinha os itens com base na linha de base do conteúdo de texto */
}

/* Modificando o tamanho da fonte para demonstrar alinhamento de baseline */
.align-baseline div:nth-child(2) {
  font-size: 24px;
}

.align-baseline div:nth-child(3) {
  font-size: 14px;
}

.align-baseline div:nth-child(4) {
  font-size: 30px;
}
```

---

## Explicação:

1. **Contêiner Flexível (`display: flex`)**:
   - A classe `.container` define que os contêineres usarão Flexbox, permitindo que os itens filhos (os `<div>` numerados de 1 a 4) sejam dispostos de acordo com a propriedade `align-items`.

2. **Alinhamentos Diferentes com `align-items`**:

   - **`align-items: flex-start;`**:
     - Os itens são alinhados no início do eixo transversal, ou seja, no topo do contêiner flexível.
     - Isso faz com que os itens sejam empurrados para o topo, independentemente da sua altura.

   - **`align-items: flex-end;`**:
     - Os itens são alinhados no final do eixo transversal, ou seja, na parte inferior do contêiner.
     - Os itens serão empurrados para baixo.

   - **`align-items: center;`**:
     - Os itens são centralizados verticalmente (se o eixo transversal for vertical).
     - Isso alinha os itens no meio do contêiner ao longo do eixo transversal.

   - **`align-items: stretch;`**:
     - Os itens são estendidos ao longo do eixo transversal para preencher todo o espaço disponível.
     - Esse comportamento ocorre apenas se os itens não tiverem uma altura ou largura definida.

   - **`align-items: baseline;`**:
     - Os itens são alinhados de acordo com a linha de base do texto.
     - Se os itens tiverem diferentes tamanhos de fonte, o alinhamento será feito com base na linha de base do texto (a linha onde o texto se "assenta").

---

### Alinhamento Visual:

- **`flex-start`**:
  ```
  1
  2
  3
  4
  (alinhados ao topo)
  ```

- **`flex-end`**:
  ```
  (espaço no topo)
  1
  2
  3
  4
  (alinhados ao final)
  ```

- **`center`**:
  ```
  (espaço)
  1
  2
  3
  4
  (alinhados ao centro)
  ```

- **`stretch`**:
  - Os itens serão esticados ao longo do eixo transversal, ocupando todo o espaço disponível verticalmente.

- **`baseline`**:
  - Os itens com diferentes tamanhos de fonte serão alinhados pela linha de base. Por exemplo:
  ```
  1   2     3      4
      (alinhados pela linha de base do texto)
  ```

---

### Demonstração Prática:

Esses diferentes valores de `align-items` permitem criar layouts flexíveis que se ajustam dinamicamente ao conteúdo dos elementos filhos. Eles são úteis, por exemplo, para centralizar conteúdo verticalmente em uma página (usando `center`), ou para garantir que todos os itens tenham a mesma altura (usando `stretch`).