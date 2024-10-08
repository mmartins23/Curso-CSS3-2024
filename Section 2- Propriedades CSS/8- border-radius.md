As propriedades relacionadas a `border-radius` no CSS3 permitem criar cantos arredondados em elementos HTML, aplicando um raio de curvatura aos cantos das bordas. Essas propriedades são altamente úteis para suavizar o design de caixas, botões e outros elementos, tornando-os visualmente mais agradáveis.

Vamos detalhar as seguintes propriedades:
- `border-top-left-radius`
- `border-top-right-radius`
- `border-bottom-right-radius`
- `border-bottom-left-radius`
- `border-radius`

---

### 1. **`border-top-left-radius`**: Raio do canto superior esquerdo

Esta propriedade define o raio de curvatura no canto **superior esquerdo** de um elemento.

### Sintaxe:

```css
elemento {
  border-top-left-radius: valor;
}
```

### Exemplo de `border-top-left-radius`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Top-Left-Radius</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      background-color: lightblue;
      border: 2px solid blue;
      border-top-left-radius: 30px; /* Arredonda o canto superior esquerdo */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com canto superior esquerdo arredondado.
  </div>

</body>
</html>
```

Neste exemplo, o **canto superior esquerdo** da caixa tem um raio de 30px, o que cria uma curvatura suave nesse canto.

---

### 2. **`border-top-right-radius`**: Raio do canto superior direito

A propriedade `border-top-right-radius` define o raio de curvatura no canto **superior direito** de um elemento.

### Sintaxe:

```css
elemento {
  border-top-right-radius: valor;
}
```

### Exemplo de `border-top-right-radius`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Top-Right-Radius</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      background-color: lightgreen;
      border: 2px solid green;
      border-top-right-radius: 40px; /* Arredonda o canto superior direito */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com canto superior direito arredondado.
  </div>

</body>
</html>
```

Aqui, o **canto superior direito** da caixa tem um raio de 40px, resultando em um arredondamento mais acentuado nesse canto.

---

### 3. **`border-bottom-right-radius`**: Raio do canto inferior direito

A propriedade `border-bottom-right-radius` define o raio de curvatura no canto **inferior direito** de um elemento.

### Sintaxe:

```css
elemento {
  border-bottom-right-radius: valor;
}
```

### Exemplo de `border-bottom-right-radius`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Bottom-Right-Radius</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      background-color: lightcoral;
      border: 2px solid red;
      border-bottom-right-radius: 20px; /* Arredonda o canto inferior direito */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com canto inferior direito arredondado.
  </div>

</body>
</html>
```

Neste exemplo, o **canto inferior direito** da caixa tem um raio de 20px, criando uma leve curvatura.

---

### 4. **`border-bottom-left-radius`**: Raio do canto inferior esquerdo

A propriedade `border-bottom-left-radius` define o raio de curvatura no canto **inferior esquerdo** de um elemento.

### Sintaxe:

```css
elemento {
  border-bottom-left-radius: valor;
}
```

### Exemplo de `border-bottom-left-radius`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Bottom-Left-Radius</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      background-color: lightyellow;
      border: 2px solid orange;
      border-bottom-left-radius: 50px; /* Arredonda o canto inferior esquerdo */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com canto inferior esquerdo arredondado.
  </div>

</body>
</html>
```

Neste exemplo, o **canto inferior esquerdo** da caixa tem um raio de 50px, criando uma curva bastante pronunciada nesse canto.

---

### 5. **`border-radius`**: Raio das bordas de todos os cantos

A propriedade `border-radius` é um atalho para definir o raio de **todos os cantos** de um elemento de uma só vez. Você pode usar um ou mais valores para aplicar diferentes graus de arredondamento a cada canto.

### Sintaxe:

```css
elemento {
  border-radius: valor;
}
```

- **Um valor**: Aplica o mesmo raio para todos os cantos.
- **Dois valores**: O primeiro valor aplica-se aos cantos superiores (esquerdo e direito), e o segundo valor aplica-se aos cantos inferiores (esquerdo e direito).
- **Três valores**: O primeiro valor aplica-se ao canto superior esquerdo, o segundo aos cantos superiores direito e inferior esquerdo, e o terceiro ao canto inferior direito.
- **Quatro valores**: Cada valor aplica-se a um canto, na seguinte ordem: superior esquerdo, superior direito, inferior direito e inferior esquerdo.

### Exemplo de `border-radius`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Radius</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      background-color: lightpink;
      border: 2px solid purple;
      border-radius: 20px 40px 60px 80px; /* Raio diferente para cada canto */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com raios diferentes em cada canto.
  </div>

</body>
</html>
```

Neste exemplo:
- O **canto superior esquerdo** tem um raio de 20px.
- O **canto superior direito** tem um raio de 40px.
- O **canto inferior direito** tem um raio de 60px.
- O **canto inferior esquerdo** tem um raio de 80px.

### Exemplo de `border-radius` igual para todos os cantos:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Radius</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      background-color: lightblue;
      border: 2px solid blue;
      border-radius: 20px; /* Arredonda todos os cantos igualmente */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com todos os cantos arredondados de 20px.
  </div>

</body>
</html>
```

Neste exemplo, **todos os cantos** da caixa têm um raio de 20px, resultando em uma curvatura uniforme.

---

## Resumo:

- **`border-top-left-radius`**: Define o raio do canto superior esquerdo.
- **`border-top-right-radius`**: Define o raio do canto superior direito.
- **`border-bottom-right-radius`**: Define o raio do canto inferior direito.
- **`border-bottom-left-radius`**: Define o raio do canto inferior esquerdo.
- **`border-radius`**: Atalho para definir o raio de todos os cantos de uma vez.

Essas propriedades são essenciais para suavizar os cantos dos elementos, proporcionando um design mais fluido e amigável em páginas web.