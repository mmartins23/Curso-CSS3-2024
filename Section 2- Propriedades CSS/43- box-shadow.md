A propriedade `box-shadow` em CSS3 adiciona uma ou mais sombras a elementos, criando um efeito de profundidade. Com esta propriedade, você pode controlar a direção, tamanho, suavidade e cor da sombra. As sombras podem ser aplicadas tanto no interior quanto no exterior do elemento, e é possível usar múltiplas sombras ao mesmo tempo.

### Sintaxe da Propriedade `box-shadow`:
```css
element {
  box-shadow: [offset-x] [offset-y] [blur-radius] [spread-radius] [color];
}
```

#### Parâmetros:
1. **`offset-x`**: Define o deslocamento da sombra no eixo horizontal. Valores positivos movem a sombra para a direita, valores negativos para a esquerda.
2. **`offset-y`**: Define o deslocamento da sombra no eixo vertical. Valores positivos movem a sombra para baixo, valores negativos para cima.
3. **`blur-radius` (opcional)**: Define o quão borrada (desfocada) será a sombra. Quanto maior o valor, mais desfocada a sombra. O valor padrão é `0` (sombra nítida).
4. **`spread-radius` (opcional)**: Controla o tamanho da sombra. Valores positivos fazem a sombra crescer, valores negativos a diminuem. O valor padrão é `0`.
5. **`color` (opcional)**: Define a cor da sombra. O valor padrão é o preto (`black`). Pode-se usar qualquer valor de cor CSS, como `rgba` para sombras com transparência.

### Exemplo Completo com HTML e CSS:

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo Box-Shadow</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="shadow-basic">
        <h2>Sombra Básica</h2>
    </div>

    <div class="shadow-blur">
        <h2>Sombra com Blur (Desfoque)</h2>
    </div>

    <div class="shadow-spread">
        <h2>Sombra com Spread</h2>
    </div>

    <div class="shadow-inset">
        <h2>Sombra Interna (Inset)</h2>
    </div>

    <div class="shadow-multiple">
        <h2>Múltiplas Sombras</h2>
    </div>
</body>
</html>
```

#### CSS (styles.css):
```css
/* Estilos gerais */
body {
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 20px;
}

div {
    width: 300px;
    margin: 20px auto;
    padding: 20px;
    border-radius: 10px;
    background-color: #e43c5c;
    color: white;
}

/* Sombra básica */
.shadow-basic {
    box-shadow: 10px 10px 5px rgba(0, 0, 0, 0.5); /* 10px à direita, 10px para baixo, 5px de desfoque */
}

/* Sombra com blur */
.shadow-blur {
    box-shadow: 10px 10px 15px rgba(0, 0, 0, 0.3); /* Aumenta o raio de desfoque para 15px */
}

/* Sombra com spread */
.shadow-spread {
    box-shadow: 10px 10px 10px 5px rgba(0, 0, 0, 0.4); /* Spread positivo de 5px */
}

/* Sombra interna (inset) */
.shadow-inset {
    box-shadow: inset 10px 10px 10px rgba(0, 0, 0, 0.5); /* Sombra interna com inset */
}

/* Múltiplas sombras */
.shadow-multiple {
    box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.5), -5px -5px 5px rgba(255, 255, 255, 0.5); /* Duas sombras */
}
```

### Explicação dos Exemplos:

1. **Sombra Básica (`shadow-basic`)**:
   - A sombra tem um deslocamento de 10px no eixo X (direita) e 10px no eixo Y (para baixo), com um raio de desfoque de 5px.
   ```css
   box-shadow: 10px 10px 5px rgba(0, 0, 0, 0.5);
   ```

2. **Sombra com Blur (`shadow-blur`)**:
   - O raio de desfoque foi aumentado para 15px, criando uma sombra mais suave e dispersa.
   ```css
   box-shadow: 10px 10px 15px rgba(0, 0, 0, 0.3);
   ```

3. **Sombra com Spread (`shadow-spread`)**:
   - O spread-radius de 5px aumenta o tamanho da sombra, expandindo-a para fora do elemento.
   ```css
   box-shadow: 10px 10px 10px 5px rgba(0, 0, 0, 0.4);
   ```

4. **Sombra Interna (`shadow-inset`)**:
   - Com o valor `inset`, a sombra é aplicada dentro do elemento, criando um efeito de profundidade interna.
   ```css
   box-shadow: inset 10px 10px 10px rgba(0, 0, 0, 0.5);
   ```

5. **Múltiplas Sombras (`shadow-multiple`)**:
   - Duas sombras são aplicadas ao mesmo elemento. A primeira sombra é deslocada para a direita e para baixo, enquanto a segunda é deslocada para a esquerda e para cima, criando um efeito de luz dupla.
   ```css
   box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.5), -5px -5px 5px rgba(255, 255, 255, 0.5);
   ```

### Propriedades Adicionais e Considerações:

1. **Sombra Interna (`inset`)**:
   - Usar `inset` faz com que a sombra apareça dentro do elemento em vez de fora, criando um efeito de profundidade interna.

2. **Cores com Transparência (`rgba`)**:
   - Usar a notação `rgba` permite ajustar a opacidade da sombra, tornando-a mais sutil com transparência.
   
3. **Múltiplas Sombras**:
   - Para aplicar múltiplas sombras, basta separar as diferentes sombras por vírgulas. Cada uma pode ter seus próprios valores de deslocamento, cor, desfoque e spread.

### Exemplos Adicionais:

#### Sombra Difusa Leve:
```css
.box {
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

#### Efeito "Cartão Elevado":
```css
.card {
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2), 0 6px 6px rgba(0, 0, 0, 0.2);
}
```

Esses exemplos demonstram como a propriedade `box-shadow` pode ser usada para criar uma ampla variedade de efeitos visuais em interfaces, desde sombras sutis e leves até sombras profundas e dramáticas.