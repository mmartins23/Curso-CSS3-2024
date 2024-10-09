A propriedade `justify-content` no CSS é usada no contexto do **Flexbox** para alinhar e distribuir itens dentro de um contêiner flexível ao longo do **eixo principal** (horizontal por padrão, mas depende da direção definida pelo `flex-direction`). Ela controla o espaçamento entre os itens, permitindo que você crie layouts que são bem distribuídos, centralizados, ou alinhados nas bordas do contêiner.

## Valores Comuns de `justify-content`

1. **`flex-start`** (padrão):
   - Os itens são alinhados no início do eixo principal (à esquerda se `flex-direction` for `row`).
   
2. **`flex-end`**:
   - Os itens são alinhados no final do eixo principal (à direita se `flex-direction` for `row`).
   
3. **`center`**:
   - Os itens são centralizados ao longo do eixo principal.
   
4. **`space-between`**:
   - Os itens são distribuídos uniformemente ao longo do eixo principal, com o primeiro item colado no início e o último item colado no final do contêiner. Os espaços entre os itens são iguais.
   
5. **`space-around`**:
   - Os itens são distribuídos uniformemente, com espaçamento igual ao redor de cada item. Isso significa que o espaço antes do primeiro item e após o último item será a metade do espaço entre os itens internos.

### Visualização do Eixo Principal

- **Eixo Principal (Main Axis)**: É determinado pela propriedade `flex-direction`. Se `flex-direction` for `row` (o padrão), o eixo principal será **horizontal**. Se for `column`, o eixo principal será **vertical**.

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
    <link rel="stylesheet" href="css/justify.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
</head>
<body>

    <h2>Property: <code>justify-content</code></h2>

    <code>justify-content: flex-start;</code>
    <div class="justify-start container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>justify-content: flex-end;</code>
    <div class="justify-end container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>justify-content: center;</code>
    <div class="justify-center container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>justify-content: space-around;</code>
    <div class="justify-around container outlined">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </div>

    <code>justify-content: space-between;</code>
    <div class="justify-between container outlined">
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

/* Alinhamento dos itens usando diferentes valores de justify-content */
.justify-start {
  justify-content: flex-start; /* Alinha os itens no início (à esquerda) */
}

.justify-end {
  justify-content: flex-end; /* Alinha os itens no final (à direita) */
}

.justify-center {
  justify-content: center; /* Centraliza os itens ao longo do eixo principal */
}

.justify-around {
  justify-content: space-around; /* Espaçamento igual ao redor de cada item */
}

.justify-between {
  justify-content: space-between; /* Espaçamento igual entre os itens */
}
```

### Explicação:

1. **Contêiner Flexível (`display: flex`)**:
   - A classe `.container` define que os contêineres usarão Flexbox, o que permite que os itens filhos (os `<div>` numerados de 1 a 4) sejam dispostos de acordo com a propriedade `justify-content`.

2. **Alinhamentos Diferentes com `justify-content`**:

   - **`justify-content: flex-start;`**:
     - Os itens são alinhados à esquerda (ou no início do eixo principal). Isso é o comportamento padrão do Flexbox.
     - A ordem visual dos itens será: `1 2 3 4` à esquerda do contêiner.

   - **`justify-content: flex-end;`**:
     - Os itens são alinhados à direita (ou no final do eixo principal).
     - A ordem visual dos itens será: `1 2 3 4`, mas alinhados à direita.

   - **`justify-content: center;`**:
     - Os itens são centralizados ao longo do eixo principal.
     - A ordem visual dos itens será: `1 2 3 4`, todos concentrados no meio do contêiner.

   - **`justify-content: space-around;`**:
     - Os itens são distribuídos com espaçamento igual ao redor de cada item.
     - O espaço ao redor do primeiro e último item será metade do espaço entre os itens internos.
     - A ordem visual será: `1 (espaço) 2 (espaço) 3 (espaço) 4`.

   - **`justify-content: space-between;`**:
     - O primeiro item é colado no início do contêiner, o último item no final, e o espaço restante é distribuído uniformemente entre os itens internos.
     - A ordem visual será: `1 (espaço) 2 (espaço) 3 (espaço) 4`.

---

### Resumo Visual:

1. **`flex-start`**: 
   ```
   | 1  2  3  4                       |
   ```

2. **`flex-end`**: 
   ```
   |                        1  2  3  4 |
   ```

3. **`center`**: 
   ```
   |        1  2  3  4        |
   ```

4. **`space-around`**:
   ```
   |   1    2    3    4   |
   ```

5. **`space-between`**:
   ```
   | 1      2      3      4 |
   ```

---

### Uso Prático:

- `justify-content` é uma propriedade poderosa para controlar o **alinhamento horizontal** (ou vertical, dependendo do eixo principal) de itens flexíveis dentro de um contêiner. Ele é útil para layouts responsivos, permitindo ajustes de espaçamento e alinhamento conforme o tamanho do contêiner muda.