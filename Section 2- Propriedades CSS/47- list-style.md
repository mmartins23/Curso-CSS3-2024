As propriedades `list-style-type`, `list-style-position`, `list-style-image`, e `list-style` no CSS são usadas para controlar a aparência e a posição dos marcadores (bullets ou números) em listas (`<ul>`, `<ol>`, e `<li>`).

Aqui estão os detalhes e exemplos de cada uma dessas propriedades:

---

## 1. `list-style-type`
Define o tipo de marcador (ou bullet) usado para itens de lista.

### Valores comuns:
- **`disc`**: Um círculo sólido (padrão para listas não ordenadas `<ul>`).
- **`circle`**: Um círculo oco.
- **`square`**: Um quadrado sólido.
- **`decimal`**: Números (padrão para listas ordenadas `<ol>`).
- **`none`**: Sem marcador.

### Exemplo:

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List Style Type Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>List with Different list-style-type</h2>
    <ul class="disc-list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <ul class="circle-list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <ul class="square-list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <ul class="none-list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

#### CSS (styles.css):
```css
/* Lista padrão com marcadores de disco */
.disc-list {
    list-style-type: disc;
}

/* Lista com círculos ocos */
.circle-list {
    list-style-type: circle;
}

/* Lista com quadrados */
.square-list {
    list-style-type: square;
}

/* Lista sem marcadores */
.none-list {
    list-style-type: none;
}
```

---

## 2. `list-style-position`
Define a posição do marcador em relação ao texto do item da lista.

### Valores:
- **`outside`**: O marcador é exibido fora da caixa de conteúdo do item da lista (padrão).
- **`inside`**: O marcador é exibido dentro da caixa de conteúdo do item da lista, fazendo parte do recuo do texto.

### Exemplo:

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List Style Position Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>List with list-style-position: outside</h2>
    <ul class="outside-list">
        <li>Item 1 com marcador fora da caixa de conteúdo</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <h2>List with list-style-position: inside</h2>
    <ul class="inside-list">
        <li>Item 1 com marcador dentro da caixa de conteúdo</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

#### CSS (styles.css):
```css
/* Marcador fora da caixa de conteúdo */
.outside-list {
    list-style-position: outside;
}

/* Marcador dentro da caixa de conteúdo */
.inside-list {
    list-style-position: inside;
}
```

---

## 3. `list-style-image`
Define uma imagem como marcador para os itens da lista.

### Valores:
- **`url(path-to-image)`**: Define a URL da imagem a ser usada como marcador.
- **`none`**: Nenhuma imagem é usada (padrão).

### Exemplo:

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List Style Image Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>List with Custom Image Marker</h2>
    <ul class="image-list">
        <li>Item 1 com marcador de imagem</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

#### CSS (styles.css):
```css
/* Usando uma imagem personalizada como marcador */
.image-list {
    list-style-image: url('https://via.placeholder.com/15');
}
```

---

## 4. `list-style`
A propriedade `list-style` é um atalho que permite definir várias propriedades de estilo de lista em uma única declaração, incluindo `list-style-type`, `list-style-position`, e `list-style-image`.

### Sintaxe:
```css
list-style: <list-style-type> <list-style-position> <list-style-image>;
```

### Exemplo:

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List Style Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>List with Multiple Style Properties</h2>
    <ul class="custom-list">
        <li>Item 1 com list-style combinado</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

#### CSS (styles.css):
```css
/* Usando o atalho list-style para combinar propriedades */
.custom-list {
    list-style: square inside url('https://via.placeholder.com/15');
}
```

---

## Explicação Detalhada:

1. **`list-style-type`**: Define o tipo de marcador da lista. Pode ser um círculo, quadrado, número, ou nenhum marcador.
2. **`list-style-position`**: Define se o marcador será colocado dentro ou fora da caixa de conteúdo do item da lista.
3. **`list-style-image`**: Permite substituir o marcador padrão por uma imagem personalizada.
4. **`list-style`**: É um atalho que combina as três propriedades anteriores, permitindo definir o tipo de marcador, a posição e a imagem em uma única linha de código.

---

### Código Completo:

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List Style Examples</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>Exemplos de Estilos de Lista</h2>

    <h3>list-style-type</h3>
    <ul class="disc-list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <h3>list-style-position</h3>
    <ul class="outside-list">
        <li>Item 1 com marcador fora</li>
        <li>Item 2</li>
    </ul>
    <ul class="inside-list">
        <li>Item 1 com marcador dentro</li>
        <li>Item 2</li>
    </ul>

    <h3>list-style-image</h3>
    <ul class="image-list">
        <li>Item 1 com marcador de imagem</li>
        <li>Item 2</li>
    </ul>

    <h3>list-style</h3>
    <ul class="custom-list">
        <li>Item 1 com list-style combinado</li>
        <li>Item 2</li>
    </ul>

</body>
</html>
```

#### CSS (styles.css):
```css
/* list-style-type */
.disc-list {
    list-style-type: disc;
}

/* list-style-position */
.outside-list {
    list-style-position: outside;
}

.inside-list {
    list-style-position: inside;
}

/* list-style-image */
.image-list {
    list-style-image: url('https://via.placeholder.com/15');
}

/* list-style */
.custom-list {
    list-style: square inside url('https://via.placeholder.com/15');
}
```

---

Esses exemplos mostram como personalizar listas em HTML com CSS, usando diferentes propriedades para definir o estilo do marcador, sua posição e até usar imagens no lugar dos marcadores tradicionais.