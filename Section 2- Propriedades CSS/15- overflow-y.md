A propriedade `overflow-y` no CSS3 é usada para controlar o comportamento de **transbordo vertical** de um conteúdo, ou seja, o que acontece quando o conteúdo de um elemento ultrapassa a sua altura definida. Essa propriedade define como o conteúdo que excede a altura do elemento será tratado, e se uma **barra de rolagem vertical** será exibida.

### Valores de `overflow-y`:

- **`visible`** (padrão): O conteúdo não é cortado e pode transbordar verticalmente além das bordas do elemento.
- **`hidden`**: O conteúdo que ultrapassa a altura do elemento é cortado, e nenhuma barra de rolagem vertical é exibida.
- **`scroll`**: Uma barra de rolagem vertical é sempre exibida, independentemente de o conteúdo transbordar ou não.
- **`auto`**: Uma barra de rolagem vertical aparece **apenas se o conteúdo transbordar**. Caso contrário, nenhuma barra é exibida.

---

### 1. **`overflow-y: visible`** (Padrão)

Quando o valor é `visible`, o conteúdo que transborda verticalmente não é cortado e permanece visível, mesmo que ultrapasse a área do elemento.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-y: visible</title>
  <style>
    .visible-box {
      width: 200px;
      height: 100px;
      background-color: lightblue;
      border: 2px solid blue;
      overflow-y: visible; /* O conteúdo transbordará verticalmente */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-y: visible`</h2>
  <div class="visible-box">
    Este é um exemplo de conteúdo que está além da altura do elemento. Ele vai continuar visível, mesmo que saia da caixa!
    <p>Texto extra para aumentar a altura.</p>
    <p>Mais texto para forçar o transbordo vertical.</p>
  </div>

</body>
</html>
```

### Explicação:
- O conteúdo que ultrapassa a altura de 100px **não será cortado** e continuará aparecendo, mesmo que saia do contorno do elemento.

---

### 2. **`overflow-y: hidden`**

Com `overflow-y: hidden`, o conteúdo que ultrapassa a altura do elemento será cortado, e o usuário não verá o conteúdo excedente.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-y: hidden</title>
  <style>
    .hidden-box {
      width: 200px;
      height: 100px;
      background-color: lightgreen;
      border: 2px solid green;
      overflow-y: hidden; /* O conteúdo será cortado verticalmente */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-y: hidden`</h2>
  <div class="hidden-box">
    Este texto vai além da altura do elemento, mas o que ultrapassar será cortado e não ficará visível.
    <p>Texto adicional para forçar o transbordo vertical.</p>
  </div>

</body>
</html>
```

### Explicação:
- O conteúdo que ultrapassa a altura de 100px **será cortado**, e o usuário não poderá ver o conteúdo excedente.

---

### 3. **`overflow-y: scroll`**

Com `overflow-y: scroll`, uma barra de rolagem vertical é **sempre exibida**, independentemente de o conteúdo transbordar ou não.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-y: scroll</title>
  <style>
    .scroll-box {
      width: 200px;
      height: 100px;
      background-color: lightyellow;
      border: 2px solid orange;
      overflow-y: scroll; /* Sempre mostra a barra de rolagem vertical */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-y: scroll`</h2>
  <div class="scroll-box">
    Este conteúdo é maior que a altura da caixa, então você pode rolar verticalmente para ver o restante. A barra de rolagem aparece mesmo que o conteúdo caiba na caixa.
    <p>Mais texto.</p>
    <p>Mais texto.</p>
    <p>Mais texto.</p>
  </div>

</body>
</html>
```

### Explicação:
- A barra de rolagem vertical será exibida **mesmo que o conteúdo caiba dentro da caixa**, permitindo que o usuário role verticalmente se necessário.

---

### 4. **`overflow-y: auto`**

Com `overflow-y: auto`, uma barra de rolagem vertical **aparece apenas quando necessário**, ou seja, apenas se o conteúdo ultrapassar a altura definida do elemento.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-y: auto</title>
  <style>
    .auto-box {
      width: 200px;
      height: 100px;
      background-color: lightpink;
      border: 2px solid red;
      overflow-y: auto; /* A barra de rolagem aparece apenas se o conteúdo transbordar */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-y: auto`</h2>
  <div class="auto-box">
    Este conteúdo é maior que a altura do elemento. Quando isso acontece, uma barra de rolagem vertical aparecerá.
    <p>Texto extra para aumentar o conteúdo e forçar o transbordo.</p>
  </div>

</body>
</html>
```

### Explicação:
- Uma barra de rolagem vertical só aparecerá **se o conteúdo transbordar**. Se o conteúdo couber dentro da caixa, nenhuma barra de rolagem será exibida.

---

### Resumo dos Valores:

| Valor          | Comportamento                                                         |
|----------------|----------------------------------------------------------------------|
| **`visible`**  | O conteúdo transborda e é visível além da área do elemento.           |
| **`hidden`**   | O conteúdo que transborda é cortado e não pode ser visualizado.       |
| **`scroll`**   | A barra de rolagem vertical é sempre exibida, mesmo sem transbordo.   |
| **`auto`**     | A barra de rolagem vertical é exibida apenas se o conteúdo transbordar.|

---

### Combinação com `overflow-x`:

Assim como com `overflow-x`, você pode combinar `overflow-y` com a propriedade **`overflow-x`** para gerenciar o comportamento de rolagem em ambas as direções.

#### Exemplo de combinação:

```css
/* Definindo o transbordo horizontal e vertical */
overflow-y: auto;
overflow-x: hidden;
```

---

### Exemplo Prático de Combinação:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Combinação de overflow-y e overflow-x</title>
  <style>
    .box-combinada {
      width: 200px;
      height: 100px;
      background-color: lightgray;
      border: 2px solid black;
      overflow-y: auto;  /* Barra de rolagem vertical, se necessário */
      overflow-x: hidden; /* Nenhuma barra de rolagem horizontal */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-y: auto` e `overflow-x: hidden`</h2>
  <div class="box-combinada">
    Este conteúdo vai além da altura do elemento, então uma barra de rolagem vertical aparecerá. O conteúdo horizontal será cortado.
    <p>Mais conteúdo para demonstrar o transbordo vertical.</p>
    <p>Mais conteúdo.</p>
  </div>

</body>
</html>
```

Neste exemplo, o transbordo vertical será controlado com uma barra de rolagem (se necessário), enquanto o conteúdo que ultrapassa horizontalmente será cortado.

---

### **Resumo Final:**

- `overflow-y` permite controlar como o conteúdo vertical transbordante será tratado.
- Os principais valores são `visible`, `hidden`, `scroll`, e `auto`.
- Ele pode ser combinado com `overflow-x` para controlar rolagem em ambas as direções (horizontal e vertical).