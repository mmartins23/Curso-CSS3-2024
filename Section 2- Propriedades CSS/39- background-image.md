A propriedade `background-image` em CSS 3 permite inserir imagens como plano de fundo de elementos HTML. Ela oferece um grande controle sobre a aparência e o comportamento dessas imagens, permitindo criar designs visuais ricos e interessantes.

**Sintaxe básica:**

```css
background-image: url('caminho/para/a/imagem.jpg');
```

Onde `url('caminho/para/a/imagem.jpg')` especifica o caminho para o arquivo de imagem que você deseja usar.

**Exemplo completo em HTML:**

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo background-image</title>
  <style>
    body {
      background-image: url('https://via.placeholder.com/1500x1000'); /* Imagem de fundo */
      background-repeat: no-repeat; /* Não repetir a imagem */
      background-size: cover; /* Cobrir toda a área do elemento */
    }
  </style>
</head>
<body>

  <h1>Exemplo de background-image</h1>
  <p>Esta página usa uma imagem de fundo.</p>

</body>
</html>
```

Neste exemplo, a imagem `https://via.placeholder.com/1500x1000` é definida como plano de fundo do elemento `body`. As propriedades `background-repeat` e `background-size` são usadas para controlar o comportamento da imagem.

**Propriedades relacionadas:**

Além de `background-image`, existem outras propriedades CSS que permitem controlar a aparência e o comportamento das imagens de fundo:

* **`background-repeat`:** Controla a repetição da imagem (e.g., `repeat`, `repeat-x`, `repeat-y`, `no-repeat`).
* **`background-size`:** Define o tamanho da imagem de fundo (e.g., `cover`, `contain`, `100px`, `50%`).
* **`background-position`:** Define a posição da imagem de fundo (e.g., `center`, `top left`, `20px 50px`).
* **`background-attachment`:** Determina se a imagem de fundo é fixa ou rola com o conteúdo (e.g., `fixed`, `scroll`).
* **`background-origin`:** Define a origem da imagem de fundo (e.g., `padding-box`, `border-box`, `content-box`).
* **`background-clip`:** Define a área onde a imagem de fundo é exibida (e.g., `padding-box`, `border-box`, `content-box`).

**Exemplo com múltiplas propriedades:**

```css
body {
  background-image: url('https://via.placeholder.com/1500x1000');
  background-repeat: repeat-x; /* Repete a imagem horizontalmente */
  background-size: 200px; /* Define a largura da imagem para 200px */
  background-position: top right; /* Posiciona a imagem no canto superior direito */
}
```

**Outras considerações:**

* **Múltiplas imagens:** É possível usar múltiplas imagens de fundo em um único elemento, separando as URLs por vírgula.
* **Gradientes:** A propriedade `background-image` também aceita gradientes lineares e radiais como valores.
* **Acessibilidade:** Certifique-se de que o contraste entre o texto e a imagem de fundo seja suficiente para garantir a legibilidade.

Com a propriedade `background-image` e suas propriedades relacionadas, você pode criar designs de fundo complexos e visualmente atraentes em seus sites. Explore as diferentes opções e experimente para obter os resultados desejados.
