A propriedade **`display`** no CSS é uma das mais importantes, pois controla como um elemento HTML é renderizado na página e como ele interage com os elementos ao seu redor. Ela determina se um elemento será exibido como um bloco, inline, flexível, grid ou até mesmo se ele será completamente removido da renderização visual.

### Tipos principais de `display`

1. **`block`**: Um elemento com `display: block` ocupa toda a largura disponível e começa em uma nova linha. Ele empurra os próximos elementos para baixo.
   
2. **`inline`**: Um elemento com `display: inline` ocupa apenas a largura necessária e não começa em uma nova linha. Ele permite que outros elementos fiquem na mesma linha.

3. **`inline-block`**: Combina características de `inline` e `block`. O elemento não quebra a linha, mas permite definir largura e altura como se fosse um bloco.

4. **`none`**: O elemento não é renderizado na página, ou seja, ele desaparece visualmente e do fluxo do documento.

5. **`flex`**: Transforma um elemento em um contêiner flexível, permitindo o controle sobre o layout dos seus elementos filhos.

6. **`grid`**: Transforma um elemento em um contêiner de grid, permitindo organizar elementos filhos em uma grade bidimensional.

---

### 1. **`display: block`**

- O elemento ocupa toda a largura disponível, empurrando os elementos adjacentes para baixo.
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display block</title>
    <style>
        div {
            background-color: lightblue;
            margin-bottom: 10px;
            width: 100%;
        }
    </style>
</head>
<body>

    <div>Elemento de Bloco 1</div>
    <div>Elemento de Bloco 2</div>

</body>
</html>
```

**Explicação**: Cada `div` ocupa 100% da largura e é renderizada em uma nova linha.

---

### 2. **`display: inline`**

- O elemento ocupa apenas o espaço necessário e permite que outros elementos fiquem na mesma linha.
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display inline</title>
    <style>
        span {
            background-color: lightcoral;
        }
    </style>
</head>
<body>

    <span>Elemento 1</span>
    <span>Elemento 2</span>
    <span>Elemento 3</span>

</body>
</html>
```

**Explicação**: Os `span` são elementos inline, logo, eles ficam na mesma linha.

---

### 3. **`display: inline-block`**

- O elemento é renderizado na mesma linha, mas pode ter largura e altura definidas como um elemento `block`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display inline-block</title>
    <style>
        div {
            display: inline-block;
            width: 150px;
            height: 100px;
            background-color: lightgreen;
            margin-right: 10px;
        }
    </style>
</head>
<body>

    <div>Elemento 1</div>
    <div>Elemento 2</div>
    <div>Elemento 3</div>

</body>
</html>
```

**Explicação**: Mesmo sendo renderizados lado a lado (como inline), os elementos `div` podem ter tamanho personalizado.

---

### 4. **`display: none`**

- O elemento não é exibido, e não ocupa espaço no layout.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display none</title>
    <style>
        p {
            display: none;
        }
    </style>
</head>
<body>

    <p>Este parágrafo não será exibido.</p>
    <p>Este parágrafo será exibido.</p>

</body>
</html>
```

**Explicação**: O primeiro parágrafo desaparece completamente da página.

---

### 5. **`display: flex`**

- O `display: flex` permite criar layouts mais dinâmicos, organizando os elementos filhos dentro de um contêiner flexível.
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display flex</title>
    <style>
        .flex-container {
            display: flex;
            justify-content: space-around;
            background-color: lightgrey;
        }

        .flex-container div {
            background-color: lightseagreen;
            width: 100px;
            height: 100px;
            margin: 10px;
        }
    </style>
</head>
<body>

    <div class="flex-container">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
    </div>

</body>
</html>
```

**Explicação**: O `display: flex` permite organizar os elementos filhos dentro do contêiner flexível, com espaçamento automático entre eles.

---

### 6. **`display: grid`**

- O `display: grid` cria um contêiner de grid, organizando os elementos filhos em uma grade bidimensional.
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display grid</title>
    <style>
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 10px;
            background-color: lightyellow;
        }

        .grid-container div {
            background-color: lightsalmon;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>

    <div class="grid-container">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
        <div>Item 4</div>
        <div>Item 5</div>
        <div>Item 6</div>
    </div>

</body>
</html>
```

**Explicação**: O `display: grid` organiza os elementos filhos em uma grade, com 3 colunas de tamanho igual e espaçamento entre elas.

---

### 7. **`display: inherit`**

- O elemento herda o valor de `display` do seu elemento pai.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de display inherit</title>
    <style>
        div {
            display: block;
        }

        span {
            display: inherit;
        }
    </style>
</head>
<body>

    <div>
        <span>Herda o display do pai (block).</span>
    </div>

</body>
</html>
```

---

### Resumo dos principais valores de `display`:

- **`block`**: Ocupa toda a largura disponível e começa em uma nova linha.
- **`inline`**: Ocupa apenas o espaço necessário e não quebra a linha.
- **`inline-block`**: Combina características de inline e block, mantendo-se na mesma linha, mas permitindo controle de largura e altura.
- **`none`**: Remove o elemento da página.
- **`flex`**: Organiza elementos filhos em um layout flexível.
- **`grid`**: Organiza elementos filhos em um layout de grade bidimensional.

Esses valores de `display` são fundamentais para construir layouts e controlar o comportamento dos elementos na página.