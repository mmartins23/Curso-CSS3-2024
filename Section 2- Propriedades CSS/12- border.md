As propriedades `border-top`, `border-right`, `border-bottom`, e `border-left` no CSS3 permitem definir as bordas específicas de cada lado de um elemento HTML. A propriedade `border` é uma forma abreviada para definir todas as bordas ao mesmo tempo, englobando a largura, o estilo e a cor da borda.

### 1. **Propriedades Individuais:**

- **`border-top`**: Define a borda superior do elemento.
- **`border-right`**: Define a borda direita do elemento.
- **`border-bottom`**: Define a borda inferior do elemento.
- **`border-left`**: Define a borda esquerda do elemento.

### 2. **Propriedade Abreviada (`border`)**:

A propriedade `border` permite definir, de uma vez, o estilo, a largura e a cor da borda de todos os lados de um elemento.

---

### Sintaxe:

```css
/* Propriedades Individuais */
border-top: largura estilo cor;
border-right: largura estilo cor;
border-bottom: largura estilo cor;
border-left: largura estilo cor;

/* Propriedade Abreviada */
border: largura estilo cor;
```

- **largura**: Define a espessura da borda. Exemplo: `2px`, `medium`, `thin`.
- **estilo**: Define o estilo da borda. Exemplo: `solid`, `dashed`, `dotted`.
- **cor**: Define a cor da borda. Exemplo: `blue`, `#000`, `rgb(255, 0, 0)`.

---

### **Exemplo Prático de Bordas Individuais e Abreviadas:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Bordas em CSS</title>
  <style>
    /* Exemplo de bordas individuais */
    .caixa-bordas-individuais {
      width: 200px;
      height: 100px;
      border-top: 5px solid red;   /* Borda superior: 5px, sólida e vermelha */
      border-right: 10px dashed green; /* Borda direita: 10px, tracejada e verde */
      border-bottom: 3px dotted blue; /* Borda inferior: 3px, pontilhada e azul */
      border-left: 7px double purple;  /* Borda esquerda: 7px, dupla e roxa */
    }

    /* Exemplo de borda abreviada */
    .caixa-borda-abreviada {
      width: 200px;
      height: 100px;
      border: 4px solid orange; /* Todas as bordas com 4px, sólida e laranja */
    }
  </style>
</head>
<body>

  <h2>Caixa com Bordas Individuais</h2>
  <div class="caixa-bordas-individuais">
    Esta caixa tem bordas diferentes em cada lado.
  </div>

  <h2>Caixa com Borda Abreviada</h2>
  <div class="caixa-borda-abreviada">
    Esta caixa tem a mesma borda em todos os lados.
  </div>

</body>
</html>
```

---

### **Explicação do Exemplo:**

1. **Caixa com bordas individuais**:
   - **`border-top: 5px solid red`**: Define a borda superior com 5px de espessura, estilo sólido, e cor vermelha.
   - **`border-right: 10px dashed green`**: Define a borda direita com 10px de espessura, estilo tracejado, e cor verde.
   - **`border-bottom: 3px dotted blue`**: Define a borda inferior com 3px de espessura, estilo pontilhado, e cor azul.
   - **`border-left: 7px double purple`**: Define a borda esquerda com 7px de espessura, estilo duplo, e cor roxa.

2. **Caixa com borda abreviada**:
   - **`border: 4px solid orange`**: Define uma borda de 4px, sólida, e laranja para todos os lados do elemento.

---

### **Propriedades Relacionadas:**

1. **Definir apenas o estilo da borda**:
   - As propriedades **`border-top-style`**, **`border-right-style`**, **`border-bottom-style`**, e **`border-left-style`** permitem definir o **estilo** da borda (sem afetar a largura ou a cor).

   ```css
   border-top-style: solid;
   border-right-style: dashed;
   ```

2. **Definir apenas a largura da borda**:
   - As propriedades **`border-top-width`**, **`border-right-width`**, **`border-bottom-width`**, e **`border-left-width`** permitem definir a **largura** da borda.

   ```css
   border-top-width: 5px;
   border-right-width: 10px;
   ```

3. **Definir apenas a cor da borda**:
   - As propriedades **`border-top-color`**, **`border-right-color`**, **`border-bottom-color`**, e **`border-left-color`** permitem definir a **cor** da borda.

   ```css
   border-top-color: red;
   border-right-color: green;
   ```

---

### **Mais Exemplos:**

#### Exemplo com estilos diferentes de borda em cada lado:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bordas com Estilos Diferentes</title>
  <style>
    .caixa {
      width: 200px;
      height: 100px;
      border-top: 3px solid red;   /* Borda sólida no topo */
      border-right: 4px dashed blue; /* Borda tracejada à direita */
      border-bottom: 5px dotted green; /* Borda pontilhada em baixo */
      border-left: 6px double purple; /* Borda dupla à esquerda */
    }
  </style>
</head>
<body>

  <h2>Caixa com Estilos Diferentes de Bordas</h2>
  <div class="caixa">
    Esta caixa tem bordas com diferentes estilos.
  </div>

</body>
</html>
```

### **Resumo:**

- **`border-top`**, **`border-right`**, **`border-bottom`**, e **`border-left`** permitem controlar as bordas de cada lado individualmente, com definições de largura, estilo e cor.
- **`border`** é a forma abreviada para definir todas as bordas ao mesmo tempo.
- Você pode misturar estilos e cores para obter diferentes efeitos visuais nas bordas de um elemento.

Essas propriedades são essenciais para criar interfaces visuais sofisticadas e precisas no design de páginas web.