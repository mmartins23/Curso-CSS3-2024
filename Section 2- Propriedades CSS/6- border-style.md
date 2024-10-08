As propriedades de **borda** no CSS3 permitem controlar o estilo das bordas de um elemento. Especificamente, as propriedades `border-top-style`, `border-right-style`, `border-bottom-style`, `border-left-style`, e `border-style` são usadas para definir o **estilo visual** de cada lado da borda de um elemento HTML. Esses estilos incluem sólidos, tracejados, pontilhados, entre outros.

Vamos explorar cada uma dessas propriedades com exemplos.

---

## 1. **`border-top-style`**: Estilo da Borda Superior

A propriedade `border-top-style` define o estilo da **borda superior** de um elemento.

### Sintaxe:

```css
elemento {
  border-top-style: estilo;
}
```

### Exemplo de `border-top-style`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Top-Style</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-top-width: 5px; /* Largura da borda superior */
      border-top-style: dashed; /* Estilo da borda superior (tracejada) */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda superior tracejada.
  </div>

</body>
</html>
```

Neste exemplo, a borda **superior** da caixa será tracejada (`dashed`) com uma **largura de 5px**.

---

## 2. **`border-right-style`**: Estilo da Borda Direita

A propriedade `border-right-style` define o estilo da **borda direita** de um elemento.

### Sintaxe:

```css
elemento {
  border-right-style: estilo;
}
```

### Exemplo de `border-right-style`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Right-Style</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-right-width: 5px; /* Largura da borda direita */
      border-right-style: dotted; /* Estilo da borda direita (pontilhada) */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda direita pontilhada.
  </div>

</body>
</html>
```

Neste exemplo, a borda **direita** da caixa será pontilhada (`dotted`) com uma **largura de 5px**.

---

## 3. **`border-bottom-style`**: Estilo da Borda Inferior

A propriedade `border-bottom-style` define o estilo da **borda inferior** de um elemento.

### Sintaxe:

```css
elemento {
  border-bottom-style: estilo;
}
```

### Exemplo de `border-bottom-style`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Bottom-Style</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-bottom-width: 5px; /* Largura da borda inferior */
      border-bottom-style: double; /* Estilo da borda inferior (dupla) */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda inferior dupla.
  </div>

</body>
</html>
```

Aqui, a borda **inferior** da caixa será **dupla** (`double`) com **5px de largura**.

---

## 4. **`border-left-style`**: Estilo da Borda Esquerda

A propriedade `border-left-style` define o estilo da **borda esquerda** de um elemento.

### Sintaxe:

```css
elemento {
  border-left-style: estilo;
}
```

### Exemplo de `border-left-style`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Left-Style</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-left-width: 5px; /* Largura da borda esquerda */
      border-left-style: groove; /* Estilo da borda esquerda (groove) */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com borda esquerda em estilo "groove".
  </div>

</body>
</html>
```

Neste exemplo, a borda **esquerda** da caixa será em estilo **groove**, que cria uma borda com aparência de relevo.

---

## 5. **`border-style`**: Definindo o Estilo de Todas as Bordas ao Mesmo Tempo

A propriedade `border-style` permite definir o estilo das bordas de **todos os lados** (superior, direita, inferior, esquerda) de uma só vez.

### Sintaxe:

```css
elemento {
  border-style: estilo;
}
```

### Valores para `border-style`:
- **Um valor**: Aplica o mesmo estilo a todas as bordas. Exemplo: `border-style: solid;`.
- **Dois valores**: O primeiro valor aplica-se às bordas **verticalmente** (superior e inferior), e o segundo valor aplica-se **horizontalmente** (direita e esquerda). Exemplo: `border-style: solid dashed;`.
- **Três valores**: O primeiro valor aplica-se à **borda superior**, o segundo valor às **bordas laterais** (direita e esquerda), e o terceiro valor à **borda inferior**. Exemplo: `border-style: solid dashed dotted;`.
- **Quatro valores**: Aplica estilos individualmente para **cada lado** (superior, direita, inferior, esquerda). Exemplo: `border-style: solid dashed dotted double;`.

### Exemplo de `border-style`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Style</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border-width: 5px; /* Largura da borda de 5px */
      border-style: solid dashed dotted double; /* Estilos diferentes para cada borda */
    }
  </style>
</head>
<body>

  <div class="box">
    Caixa com bordas de estilos variados.
  </div>

</body>
</html>
```

Neste exemplo:
- A **borda superior** será sólida (`solid`).
- A **borda direita** será tracejada (`dashed`).
- A **borda inferior** será pontilhada (`dotted`).
- A **borda esquerda** será dupla (`double`).

---

## Estilos Comuns de Bordas

Aqui estão alguns dos estilos de borda mais usados:

- **`solid`**: Borda sólida.
- **`dashed`**: Borda tracejada.
- **`dotted`**: Borda pontilhada.
- **`double`**: Borda dupla.
- **`groove`**: Borda com um relevo que cria um efeito 3D.
- **`ridge`**: Oposto do `groove`, parece com um relevo elevado.
- **`inset`**: Cria um efeito de borda embutida.
- **`outset`**: Oposto de `inset`, parece estar elevada.

### Exemplo com Todos os Estilos:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplos de Border-Style</title>
  <style>
    .solid {
      border: 5px solid black;
      margin-bottom: 10px;
    }

    .dashed {
      border: 5px dashed black;
      margin-bottom: 10px;
    }

    .dotted {
      border: 5px dotted black;
      margin-bottom: 10px;
    }

    .double {
      border: 5px double black;
      margin-bottom: 10px;
    }

    .groove {
      border: 5px groove black;
      margin-bottom: 10px;
    }

    .ridge {
      border: 5px ridge black;
      margin-bottom: 10px;
    }

    .inset {
      border: 5px inset black;
      margin-bottom: 10px;
    }

    .outset {
      border: 5px outset black;
      margin-bottom: 10px;
    }
  </style>
</head>
<body

>

  <div class="solid">Borda sólida</div>
  <div class="dashed">Borda tracejada</div>
  <div class="dotted">Borda pontilhada</div>
  <div class="double">Borda dupla</div>
  <div class="groove">Borda em relevo (groove)</div>
  <div class="ridge">Borda em relevo (ridge)</div>
  <div class="inset">Borda embutida (inset)</div>
  <div class="outset">Borda elevada (outset)</div>

</body>
</html>
```

Neste exemplo, diferentes estilos de bordas são aplicados para ilustrar como cada estilo visualmente afeta a borda do elemento.

---

Essas propriedades de **border-style** no CSS3 são extremamente úteis para dar definição e separação visual aos elementos em uma página web, além de ajudar no design e estruturação visual do layout.