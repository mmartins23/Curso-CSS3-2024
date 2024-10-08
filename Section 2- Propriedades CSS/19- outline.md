No CSS3, a propriedade **`outline`** é usada para desenhar uma linha ao redor de um elemento, **fora da borda**, sem influenciar no layout. A linha de contorno é útil para destacar elementos, como botões ou campos de formulário, especialmente durante interações como foco (`focus`).

A propriedade `outline` é composta por várias subpropriedades que permitem o controle completo sobre o estilo, a cor, a largura e o deslocamento do contorno.

### 1. **`outline-style`**

A propriedade **`outline-style`** define o estilo da linha de contorno. Ela pode assumir os mesmos valores usados em `border-style`. Alguns valores comuns incluem:

- **`none`**: Nenhuma linha de contorno (padrão).
- **`solid`**: Linha contínua.
- **`dotted`**: Linha pontilhada.
- **`dashed`**: Linha tracejada.
- **`double`**: Linha dupla.
- **`groove`**, **`ridge`**, **`inset`**, **`outset`**: Estilos 3D.

### Exemplo de `outline-style`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de outline-style</title>
    <style>
        .solid-outline {
            outline-style: solid;
        }

        .dotted-outline {
            outline-style: dotted;
        }

        .double-outline {
            outline-style: double;
        }
    </style>
</head>
<body>

    <button class="solid-outline">Sólido</button>
    <button class="dotted-outline">Pontilhado</button>
    <button class="double-outline">Duplo</button>

</body>
</html>
```

### 2. **`outline-color`**

A propriedade **`outline-color`** define a cor da linha de contorno. Ela pode assumir valores como:

- Nome de cor (ex: `red`, `blue`)
- Cores hexadecimais (ex: `#ff0000`)
- Cores `rgb()` ou `rgba()`

### Exemplo de `outline-color`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de outline-color</title>
    <style>
        .red-outline {
            outline-style: solid;
            outline-color: red;
        }

        .blue-outline {
            outline-style: dashed;
            outline-color: blue;
        }

        .transparent-outline {
            outline-style: solid;
            outline-color: rgba(0, 0, 0, 0.5); /* Semi-transparente */
        }
    </style>
</head>
<body>

    <button class="red-outline">Vermelho</button>
    <button class="blue-outline">Azul</button>
    <button class="transparent-outline">Semi-transparente</button>

</body>
</html>
```

### 3. **`outline-width`**

A propriedade **`outline-width`** define a espessura (largura) da linha de contorno. Ela aceita os mesmos valores que `border-width`, incluindo:

- **Valores numéricos**: (ex: `1px`, `3px`)
- **Palavras-chave**: `thin`, `medium`, `thick`

### Exemplo de `outline-width`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de outline-width</title>
    <style>
        .thin-outline {
            outline-style: solid;
            outline-width: thin;
            outline-color: green;
        }

        .medium-outline {
            outline-style: solid;
            outline-width: medium;
            outline-color: purple;
        }

        .thick-outline {
            outline-style: solid;
            outline-width: thick;
            outline-color: orange;
        }
    </style>
</head>
<body>

    <button class="thin-outline">Fina</button>
    <button class="medium-outline">Média</button>
    <button class="thick-outline">Grossa</button>

</body>
</html>
```

### 4. **`outline-offset`**

A propriedade **`outline-offset`** especifica o **espaçamento entre a borda** do elemento e a linha de contorno. Esse valor pode ser positivo ou negativo, e é normalmente especificado em pixels.

- Um valor positivo desloca a linha de contorno **para fora** da borda.
- Um valor negativo desloca a linha de contorno **para dentro**.

### Exemplo de `outline-offset`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de outline-offset</title>
    <style>
        .no-offset {
            outline-style: solid;
            outline-color: black;
            outline-width: 3px;
            outline-offset: 0px;
        }

        .small-offset {
            outline-style: solid;
            outline-color: black;
            outline-width: 3px;
            outline-offset: 5px;
        }

        .large-offset {
            outline-style: solid;
            outline-color: black;
            outline-width: 3px;
            outline-offset: 15px;
        }
    </style>
</head>
<body>

    <button class="no-offset">Sem Offset</button>
    <button class="small-offset">Pequeno Offset</button>
    <button class="large-offset">Grande Offset</button>

</body>
</html>
```

### 5. **`outline`** (propriedade abreviada)

A propriedade **`outline`** é uma forma abreviada de definir o estilo, a cor e a largura do contorno em uma única declaração. Sua sintaxe é semelhante à da propriedade `border`, e sua ordem é:

```css
outline: [outline-width] [outline-style] [outline-color];
```

### Exemplo de `outline` (abreviado)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de outline abreviado</title>
    <style>
        .outline-shorthand {
            outline: 2px dashed red;
        }

        .outline-shorthand-thick {
            outline: thick solid blue;
        }
    </style>
</head>
<body>

    <button class="outline-shorthand">Contorno abreviado</button>
    <button class="outline-shorthand-thick">Contorno grosso</button>

</body>
</html>
```

### Conclusão

A propriedade **`outline`** e suas subpropriedades (`outline-style`, `outline-color`, `outline-width`, e `outline-offset`) oferecem controle detalhado sobre a aparência dos contornos de um elemento, sem afetar o layout. Ao contrário da borda, o contorno é desenhado **fora do elemento** e é especialmente útil para destacar elementos durante interações, como foco em campos de formulário ou botões.