# Cores

CSS3 introduz várias formas de definir cores, proporcionando flexibilidade e opções para estilizar elementos de forma criativa e eficiente. As cores podem ser aplicadas a propriedades como `background-color`, `color` (para texto), `border-color`, entre outras. Vamos explorar as diferentes maneiras de usar cores em CSS3 com exemplos.

### 1. **Cores Nomeadas**
CSS suporta uma lista de nomes de cores predefinidos como `red`, `blue`, `green`, entre outros. Esses nomes são simples e fáceis de usar, mas oferecem um número limitado de opções.

```css
h1 {
    color: red;
}
```

Neste exemplo, o texto do `h1` será exibido na cor vermelha.

### 2. **RGB (Red, Green, Blue)**
O sistema RGB define cores usando os valores de vermelho, verde e azul. Esses valores variam de 0 a 255.

```css
p {
    background-color: rgb(255, 0, 0); /* Vermelho puro */
    color: rgb(255, 255, 255); /* Branco */
}
```

Aqui, o parágrafo terá um fundo vermelho e o texto será branco.

### 3. **RGBA (Red, Green, Blue, Alpha)**
A variante RGBA permite definir a opacidade (transparência) da cor usando o valor Alpha, que vai de 0 (totalmente transparente) a 1 (totalmente opaco).

```css
div {
    background-color: rgba(0, 0, 255, 0.5); /* Azul semitransparente */
}
```

Nesse caso, o fundo do `div` será azul com 50% de opacidade.

### 4. **HEX (Hexadecimal)**
A representação hexadecimal é muito popular e compacta. Ela usa seis dígitos, onde os dois primeiros representam a quantidade de vermelho, os dois seguintes verde, e os dois últimos azul. Vai de `00` a `FF`.

```css
button {
    background-color: #e43c5c; /* Vermelho escuro */
    color: #ffffff; /* Branco */
}
```

Neste exemplo, o botão terá um fundo de cor vermelho-escuro e texto branco.

### 5. **HSL (Hue, Saturation, Lightness)**
O HSL usa o matiz (hue), saturação (saturation) e luminosidade (lightness) para definir cores. O matiz é o ângulo em uma roda de cores (0 a 360), a saturação e a luminosidade são porcentagens.

```css
a {
    color: hsl(120, 100%, 50%); /* Verde brilhante */
}
```

Aqui, o link será estilizado com um verde brilhante.

### 6. **HSLA (Hue, Saturation, Lightness, Alpha)**
Assim como o RGBA, o HSLA adiciona o valor de opacidade para as cores HSL.

```css
section {
    background-color: hsla(200, 100%, 50%, 0.3); /* Azul claro semitransparente */
}
```

Este `section` terá um fundo azul claro com 30% de opacidade.

### 7. **Gradientes de Cores**
CSS3 permite criar transições suaves entre duas ou mais cores usando gradientes. Existem dois tipos principais: **linear-gradient** e **radial-gradient**.

- **Linear Gradient**: Transição de cores de forma linear (de cima para baixo, da esquerda para direita, etc.).
  
  ```css
  header {
      background: linear-gradient(to right, red, yellow);
  }
  ```

  Neste exemplo, o fundo do `header` será uma transição de vermelho para amarelo da esquerda para a direita.

- **Radial Gradient**: Transição de cores em forma de círculo ou elipse.
  
  ```css
  footer {
      background: radial-gradient(circle, blue, green);
  }
  ```

  Aqui, o fundo do `footer` será um gradiente circular que começa com azul no centro e termina com verde nas bordas.

---