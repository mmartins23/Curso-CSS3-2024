No CSS3, a propriedade `border-image` e suas subpropriedades permitem que você aplique uma **imagem** como borda de um elemento HTML, em vez de usar a borda sólida tradicional. A imagem é fatiada em partes e distribuída ao longo das bordas, oferecendo uma grande flexibilidade de design.

Aqui está um detalhamento das subpropriedades da `border-image` e exemplos de como usá-las.

---

### 1. **`border-image-source`**: Fonte da Imagem da Borda

A propriedade `border-image-source` define a **imagem** que será usada para criar a borda.

### Sintaxe:

```css
elemento {
  border-image-source: url('caminho/da/imagem.png');
}
```

### Exemplo de `border-image-source`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Image-Source</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 20px; /* Definir largura da borda para exibir a imagem */
      border-image-source: url('https://via.placeholder.com/150'); /* Fonte da imagem da borda */
      border-style: solid;
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com imagem de borda.
  </div>

</body>
</html>
```

Neste exemplo, a imagem de borda é carregada de um link externo e usada nas bordas da caixa.

---

### 2. **`border-image-width`**: Largura da Imagem da Borda

A propriedade `border-image-width` define a **largura** da área da borda que será preenchida pela imagem. Ela pode ser ajustada em valores numéricos, porcentagens ou como multiplicador da largura original da borda.

### Sintaxe:

```css
elemento {
  border-image-width: valor;
}
```

### Exemplo de `border-image-width`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Image-Width</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 20px;
      border-image-source: url('https://via.placeholder.com/150');
      border-image-width: 10px; /* Largura da imagem da borda */
      border-style: solid;
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com largura de imagem da borda de 10px.
  </div>

</body>
</html>
```

Aqui, a **largura da borda** preenchida pela imagem será ajustada para **10px**.

---

### 3. **`border-image-slice`**: Fatiamento da Imagem da Borda

A propriedade `border-image-slice` define como a imagem da borda será **fatiada** (dividida) em 9 partes: 4 para as bordas, 4 para os cantos e 1 para o conteúdo. Isso permite um melhor controle sobre como a imagem será aplicada às bordas.

### Sintaxe:

```css
elemento {
  border-image-slice: valor;
}
```

- **Um valor**: Aplica o mesmo fatiamento em todos os lados.
- **Dois valores**: O primeiro valor se aplica às bordas superior/inferior, e o segundo às bordas laterais.
- **Quatro valores**: Aplicam-se aos quatro lados, em ordem: superior, direita, inferior e esquerda.

### Exemplo de `border-image-slice`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Image-Slice</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 20px;
      border-image-source: url('https://via.placeholder.com/150');
      border-image-slice: 30; /* Fatiar a imagem em 30% */
      border-style: solid;
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com imagem da borda fatiada.
  </div>

</body>
</html>
```

Aqui, a imagem é **fatiada em 30%** de sua largura e altura original para ser distribuída nas bordas.

---

### 4. **`border-image-outset`**: Projeção da Imagem da Borda

A propriedade `border-image-outset` define o quanto a imagem da borda deve **se projetar para fora** da área do conteúdo do elemento.

### Sintaxe:

```css
elemento {
  border-image-outset: valor;
}
```

### Exemplo de `border-image-outset`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Image-Outset</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 20px;
      border-image-source: url('https://via.placeholder.com/150');
      border-image-slice: 30;
      border-image-outset: 10px; /* Projeta a imagem da borda para fora 10px */
      border-style: solid;
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com imagem da borda projetada para fora.
  </div>

</body>
</html>
```

Neste exemplo, a borda **se projeta 10px para fora** do elemento, criando um efeito de afastamento da área de conteúdo.

---

### 5. **`border-image-repeat`**: Repetição da Imagem da Borda

A propriedade `border-image-repeat` define como a imagem da borda será **repetida** ao longo das bordas.

### Valores possíveis:
- `stretch`: A imagem será **esticada** para preencher a borda.
- `repeat`: A imagem será **repetida** ao longo da borda.
- `round`: A imagem será **repetida** e ajustada (encurtada ou alongada) para se encaixar perfeitamente na borda.
- `space`: A imagem será repetida e o espaço extra será distribuído entre as repetições.

### Sintaxe:

```css
elemento {
  border-image-repeat: valor;
}
```

### Exemplo de `border-image-repeat`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Image-Repeat</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 20px;
      border-image-source: url('https://via.placeholder.com/150');
      border-image-slice: 30;
      border-image-repeat: repeat; /* Repetir a imagem da borda */
      border-style: solid;
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com imagem da borda repetida.
  </div>

</body>
</html>
```

Aqui, a imagem da borda será **repetida** ao longo das bordas do elemento.

---

### 6. **`border-image`**: Atalho para Definir Todas as Propriedades da Imagem da Borda

A propriedade `border-image` é um atalho para definir todas as subpropriedades de uma vez.

### Sintaxe:

```css
elemento {
  border-image: source slice width outset repeat;
}
```

### Exemplo de `border-image`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Image</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 20px;
      border-image: url('https://via.placeholder.com/150') 30 stretch; /* Usando o atalho */
      border-style: solid;
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com imagem de borda usando o atalho border-image.
  </div>

</body>
</html>
```

Neste exemplo, o atalho `border-image` define a imagem da borda, fatiamento em 30% e o método de repetição como `stretch` (esticar a imagem ao longo das bordas).

---

### Resumo:

- **`border-image-source`**: Define a imagem a ser usada como borda.
-

 **`border-image-width`**: Define a largura da área de borda preenchida pela imagem.
- **`border-image-slice`**: Fatia a imagem para ser aplicada nas bordas.
- **`border-image-outset`**: Define o quanto a imagem da borda se projeta para fora.
- **`border-image-repeat`**: Controla como a imagem da borda é repetida ou esticada.
- **`border-image`**: Atalho para definir todas essas propriedades de uma vez.