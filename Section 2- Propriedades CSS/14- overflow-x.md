A propriedade `overflow-x` no CSS3 controla o comportamento de **transbordo horizontal** do conteúdo de um elemento, ou seja, o que acontece quando o conteúdo de um elemento é maior do que a largura definida. Essa propriedade é usada para decidir se as **barras de rolagem horizontais** serão exibidas, ocultadas ou se o conteúdo será cortado.

### Valores de `overflow-x`:

- **`visible`** (padrão): O conteúdo não é cortado e pode transbordar horizontalmente além das bordas do elemento.
- **`hidden`**: O conteúdo que ultrapassa a largura do elemento é cortado (não será visível) e nenhuma barra de rolagem é exibida.
- **`scroll`**: Uma barra de rolagem horizontal é sempre exibida, independentemente de o conteúdo transbordar ou não.
- **`auto`**: Uma barra de rolagem horizontal aparece **apenas se o conteúdo transbordar**. Caso contrário, nenhuma barra é exibida.

---

### 1. **`overflow-x: visible`** (Padrão)

Quando o valor é `visible`, o conteúdo que transborda não será cortado e ficará visível, mesmo que saia da área do elemento.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-x: visible</title>
  <style>
    .visible-box {
      width: 200px;
      height: 100px;
      background-color: lightblue;
      border: 2px solid blue;
      overflow-x: visible; /* O conteúdo transbordará horizontalmente */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-x: visible`</h2>
  <div class="visible-box">
    Este é um exemplo de conteúdo que está além da largura do elemento. Ele vai continuar visível, mesmo que saia da caixa!
  </div>

</body>
</html>
```

### Explicação:
- O conteúdo que ultrapassa a largura de 200px **não será cortado** e continuará aparecendo, mesmo que saia do contorno do elemento.

---

### 2. **`overflow-x: hidden`**

Com `overflow-x: hidden`, o conteúdo que ultrapassa a largura do elemento será cortado, e o usuário não verá o conteúdo que excede o limite.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-x: hidden</title>
  <style>
    .hidden-box {
      width: 200px;
      height: 100px;
      background-color: lightgreen;
      border: 2px solid green;
      overflow-x: hidden; /* O conteúdo será cortado horizontalmente */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-x: hidden`</h2>
  <div class="hidden-box">
    Este texto vai além da largura do elemento, mas o que ultrapassar será cortado e não ficará visível.
  </div>

</body>
</html>
```

### Explicação:
- O conteúdo que ultrapassa a largura de 200px **será cortado**, e o usuário não poderá ver o conteúdo excedente.

---

### 3. **`overflow-x: scroll`**

Com `overflow-x: scroll`, uma barra de rolagem horizontal é **sempre exibida**, independentemente de o conteúdo transbordar ou não.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-x: scroll</title>
  <style>
    .scroll-box {
      width: 200px;
      height: 100px;
      background-color: lightyellow;
      border: 2px solid orange;
      overflow-x: scroll; /* Sempre mostra a barra de rolagem horizontal */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-x: scroll`</h2>
  <div class="scroll-box">
    Este conteúdo é maior que a largura da caixa, então você pode rolar horizontalmente para ver o restante. A barra de rolagem aparece mesmo que o conteúdo caiba na caixa.
  </div>

</body>
</html>
```

### Explicação:
- A barra de rolagem horizontal será exibida **mesmo que o conteúdo caiba dentro da caixa**, permitindo que o usuário role horizontalmente se necessário.

---

### 4. **`overflow-x: auto`**

Com `overflow-x: auto`, uma barra de rolagem horizontal **aparece apenas quando necessário**, ou seja, apenas se o conteúdo ultrapassar a largura definida do elemento.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-x: auto</title>
  <style>
    .auto-box {
      width: 200px;
      height: 100px;
      background-color: lightpink;
      border: 2px solid red;
      overflow-x: auto; /* A barra de rolagem aparece apenas se o conteúdo transbordar */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-x: auto`</h2>
  <div class="auto-box">
    Este conteúdo é maior que a largura do elemento. Quando isso acontece, uma barra de rolagem horizontal aparecerá.
  </div>

</body>
</html>
```

### Explicação:
- Uma barra de rolagem horizontal só aparecerá **se o conteúdo transbordar**. Se o conteúdo couber dentro da caixa, nenhuma barra de rolagem será exibida.

---

### Resumo dos Valores:

| Valor          | Comportamento                                                          |
|----------------|------------------------------------------------------------------------|
| **`visible`**  | O conteúdo transborda e é visível além da área do elemento.            |
| **`hidden`**   | O conteúdo que transborda é cortado e não pode ser visualizado.        |
| **`scroll`**   | A barra de rolagem horizontal é sempre exibida, mesmo sem transbordo.  |
| **`auto`**     | A barra de rolagem horizontal é exibida apenas se o conteúdo transbordar.|

---

### Combinação com `overflow-y`:

Você pode combinar `overflow-x` com a propriedade **`overflow-y`**, que controla o transbordo vertical, para gerenciar o comportamento de rolagem tanto no eixo horizontal quanto no vertical. Por exemplo:

```css
/* Definindo o transbordo vertical e horizontal */
overflow-x: auto;
overflow-y: hidden;
```

---

### Exemplo Prático de Combinação:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Combinação de overflow-x e overflow-y</title>
  <style>
    .box-combinada {
      width: 200px;
      height: 100px;
      background-color: lightgray;
      border: 2px solid black;
      overflow-x: auto;  /* Barra de rolagem horizontal, se necessário */
      overflow-y: hidden; /* Nenhuma barra de rolagem vertical */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-x: auto` e `overflow-y: hidden`</h2>
  <div class="box-combinada">
    Este conteúdo vai além da largura do elemento, então uma barra de rolagem horizontal aparecerá. O conteúdo vertical que ultrapassa será cortado, sem barra de rolagem.
  </div>

</body>
</html>
```

Neste exemplo, o transbordo horizontal será controlado com uma barra de rolagem (se necessário), enquanto o conteúdo que ultrapassa verticalmente será cortado.

---

### **Resumo Final:**

- `overflow-x` permite controlar como o conteúdo horizontal transbordante será tratado.
- Os principais valores são `visible`, `hidden`, `scroll`, e `auto`.
- Ele pode ser combinado com `overflow-y` para controlar rolagem em ambas as direções (horizontal e vertical).
