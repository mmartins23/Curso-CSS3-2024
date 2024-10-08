As propriedades de **borda** no CSS3 permitem controlar a aparência das bordas de um elemento HTML. Especificamente, as propriedades `border-top-color`, `border-right-color`, `border-bottom-color`, `border-left-color`, e `border-color` controlam as **cores** das bordas em cada lado do elemento.

A seguir, vamos explorar cada uma dessas propriedades em detalhes com exemplos.

---

## 1. **`border-top-color`**: Cor da Borda Superior

A propriedade `border-top-color` define a **cor** da borda superior de um elemento.

### Sintaxe:

```css
elemento {
  border-top-color: cor;
}
```

### Exemplo de `border-top-color`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Top-Color</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-top: 5px solid; /* Define a largura e o estilo da borda superior */
      border-top-color: red; /* Define a cor da borda superior */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda superior vermelha.
  </div>

</body>
</html>
```

Neste exemplo, a borda **superior** da caixa será vermelha (`red`) com **5px de largura**.

---

## 2. **`border-right-color`**: Cor da Borda Direita

A propriedade `border-right-color` define a cor da **borda direita** do elemento.

### Sintaxe:

```css
elemento {
  border-right-color: cor;
}
```

### Exemplo de `border-right-color`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Right-Color</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-right: 5px solid; /* Define a largura e o estilo da borda direita */
      border-right-color: blue; /* Define a cor da borda direita */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda direita azul.
  </div>

</body>
</html>
```

Neste exemplo, a borda **direita** da caixa será azul (`blue`) com **5px de largura**.

---

## 3. **`border-bottom-color`**: Cor da Borda Inferior

A propriedade `border-bottom-color` define a cor da **borda inferior** do elemento.

### Sintaxe:

```css
elemento {
  border-bottom-color: cor;
}
```

### Exemplo de `border-bottom-color`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Bottom-Color</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-bottom: 5px solid; /* Define a largura e o estilo da borda inferior */
      border-bottom-color: green; /* Define a cor da borda inferior */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda inferior verde.
  </div>

</body>
</html>
```

Aqui, a borda **inferior** da caixa será verde (`green`) com **5px de largura**.

---

## 4. **`border-left-color`**: Cor da Borda Esquerda

A propriedade `border-left-color` define a cor da **borda esquerda** do elemento.

### Sintaxe:

```css
elemento {
  border-left-color: cor;
}
```

### Exemplo de `border-left-color`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Left-Color</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-left: 5px solid; /* Define a largura e o estilo da borda esquerda */
      border-left-color: purple; /* Define a cor da borda esquerda */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda esquerda roxa.
  </div>

</body>
</html>
```

Neste exemplo, a borda **esquerda** da caixa será roxa (`purple`) com **5px de largura**.

---

## 5. **`border-color`**: Definindo Todas as Cores de Bordas de Uma Só Vez

A propriedade `border-color` permite definir a cor das bordas de **todos os lados** (superior, direita, inferior, esquerda) de uma só vez.

### Sintaxe:

```css
elemento {
  border-color: cor;
}
```

### Valores para `border-color`:
- Um valor: Aplica a mesma cor a todas as bordas. Exemplo: `border-color: black;`.
- Dois valores: O primeiro valor define a cor para as bordas **superior e inferior**, e o segundo valor define a cor para as bordas **laterais**. Exemplo: `border-color: red green;`.
- Três valores: O primeiro valor aplica-se à **borda superior**, o segundo às **bordas laterais**, e o terceiro à **borda inferior**. Exemplo: `border-color: red green blue;`.
- Quatro valores: Aplica cores individualmente para **cada borda** (superior, direita, inferior, esquerda). Exemplo: `border-color: red green blue yellow;`.

### Exemplo de `border-color`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Color</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 5px; /* Define a largura de todas as bordas */
      border-style: solid; /* Define o estilo da borda */
      border-color: red green blue yellow; /* Define cores diferentes para cada lado */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com bordas coloridas de forma individual.
  </div>

</body>
</html>
```

Neste exemplo:
- **Borda superior** será vermelha (`red`).
- **Borda direita** será verde (`green`).
- **Borda inferior** será azul (`blue`).
- **Borda esquerda** será amarela (`yellow`).

---