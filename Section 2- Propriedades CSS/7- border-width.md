As propriedades de borda em CSS3 permitem definir a **largura** de cada lado de uma borda em torno de um elemento. Especificamente, as propriedades `border-top-width`, `border-right-width`, `border-bottom-width`, `border-left-width`, e `border-width` controlam a **espessura** das bordas em cada um dos lados (superior, direito, inferior e esquerdo) de um elemento HTML.

Vamos explorar essas propriedades em detalhes.

---

## 1. **`border-top-width`**: Largura da Borda Superior

A propriedade `border-top-width` define a **largura** da borda **superior** de um elemento.

### Sintaxe:

```css
elemento {
  border-top-width: valor;
}
```

### Exemplos de valores:
- **Tamanho fixo** (por exemplo, `5px`): Define uma largura de 5 pixels.
- **Palavras-chave** (`thin`, `medium`, `thick`): Usadas para definir larguras predefinidas.

### Exemplo de `border-top-width`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Top-Width</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-top-width: 10px; /* Largura da borda superior */
      border-top-style: solid; /* Estilo da borda superior */
      border-top-color: blue;  /* Cor da borda superior */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda superior de 10px.
  </div>

</body>
</html>
```

Neste exemplo, a **borda superior** terá uma largura de **10 pixels**, será sólida (`solid`), e de cor azul.

---

## 2. **`border-right-width`**: Largura da Borda Direita

A propriedade `border-right-width` define a **largura** da borda **direita** de um elemento.

### Sintaxe:

```css
elemento {
  border-right-width: valor;
}
```

### Exemplo de `border-right-width`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Right-Width</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-right-width: 15px; /* Largura da borda direita */
      border-right-style: solid; /* Estilo da borda direita */
      border-right-color: red;   /* Cor da borda direita */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda direita de 15px.
  </div>

</body>
</html>
```

Neste exemplo, a **borda direita** terá uma largura de **15 pixels**, será sólida e de cor vermelha.

---

## 3. **`border-bottom-width`**: Largura da Borda Inferior

A propriedade `border-bottom-width` define a **largura** da borda **inferior** de um elemento.

### Sintaxe:

```css
elemento {
  border-bottom-width: valor;
}
```

### Exemplo de `border-bottom-width`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Bottom-Width</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-bottom-width: 8px; /* Largura da borda inferior */
      border-bottom-style: solid; /* Estilo da borda inferior */
      border-bottom-color: green; /* Cor da borda inferior */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda inferior de 8px.
  </div>

</body>
</html>
```

Aqui, a **borda inferior** terá uma largura de **8 pixels**, será sólida e de cor verde.

---

## 4. **`border-left-width`**: Largura da Borda Esquerda

A propriedade `border-left-width` define a **largura** da borda **esquerda** de um elemento.

### Sintaxe:

```css
elemento {
  border-left-width: valor;
}
```

### Exemplo de `border-left-width`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Left-Width</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-left-width: 20px; /* Largura da borda esquerda */
      border-left-style: solid; /* Estilo da borda esquerda */
      border-left-color: purple; /* Cor da borda esquerda */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda esquerda de 20px.
  </div>

</body>
</html>
```

Neste exemplo, a **borda esquerda** terá uma largura de **20 pixels**, será sólida e de cor roxa.

---

## 5. **`border-width`**: Definindo a Largura de Todas as Bordas

A propriedade `border-width` permite definir as larguras das bordas de todos os lados (superior, direita, inferior e esquerda) de uma só vez.

### Sintaxe:

```css
elemento {
  border-width: valor;
}
```

### Valores para `border-width`:
- **Um valor**: Aplica a mesma largura a todas as bordas. Exemplo: `border-width: 5px;`.
- **Dois valores**: O primeiro valor aplica-se às bordas **verticalmente** (superior e inferior), e o segundo valor aplica-se **horizontalmente** (direita e esquerda). Exemplo: `border-width: 5px 10px;`.
- **Três valores**: O primeiro valor aplica-se à **borda superior**, o segundo valor às **bordas laterais** (direita e esquerda), e o terceiro valor à **borda inferior**. Exemplo: `border-width: 5px 10px 15px;`.
- **Quatro valores**: Aplica larguras individualmente para **cada lado** (superior, direita, inferior, esquerda). Exemplo: `border-width: 5px 10px 15px 20px;`.

### Exemplo de `border-width`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Width</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 5px 10px 15px 20px; /* Larguras para cada borda (superior, direita, inferior, esquerda) */
      border-style: solid; /* Estilo sólido para todas as bordas */
      border-color: black; /* Cor preta para todas as bordas */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com larguras de borda diferentes em cada lado.
  </div>

</body>
</html>
```

Neste exemplo:
- A **borda superior** terá 5px de largura.
- A **borda direita** terá 10px de largura.
- A **borda inferior** terá 15px de largura.
- A **borda esquerda** terá 20px de largura.

---

## Resumo:

As propriedades de largura de borda (`border-top-width`, `border-right-width`, `border-bottom-width`, `border-left-width`, e `border-width`) são usadas para definir a espessura de cada lado da borda de um elemento em uma página HTML. Você pode controlar cada lado individualmente ou todos os lados de uma vez usando a propriedade `border-width`. Essas propriedades são úteis para dar mais controle sobre o design e layout de uma página web, criando separações visuais claras entre os elementos.