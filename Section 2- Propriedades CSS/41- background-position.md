A propriedade `background-position` em CSS define a posição inicial da imagem de fundo dentro do elemento. Você pode posicionar a imagem usando palavras-chave, porcentagens ou valores de comprimento.

**Sintaxe básica:**

```css
background-position: valor_horizontal valor_vertical;
```

Onde:

* **`valor_horizontal`:** Define a posição horizontal da imagem (ex: `left`, `center`, `right`, `10px`, `50%`).
* **`valor_vertical`:** Define a posição vertical da imagem (ex: `top`, `center`, `bottom`, `20px`, `25%`).

**Exemplo completo em HTML com vários exemplos:**

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplos de background-position</title>
  <style>
    .container {
      width: 400px;
      height: 200px;
      margin: 20px auto;
      border: 1px solid #ccc;
      background-image: url('https://via.placeholder.com/100x100'); /* Imagem de fundo */
      background-repeat: no-repeat; /* Para não repetir a imagem */
    }

    /* Exemplo 1: Posição no canto superior esquerdo (padrão) */
    .exemplo-1 {
      background-position: top left; /* ou 0% 0% ou 0px 0px */
    }

    /* Exemplo 2: Posição centralizada */
    .exemplo-2 {
      background-position: center; /* ou 50% 50% */
    }

    /* Exemplo 3: Posição no canto inferior direito */
    .exemplo-3 {
      background-position: bottom right; /* ou 100% 100% */
    }

    /* Exemplo 4: Posição com valores em pixels */
    .exemplo-4 {
      background-position: 50px 100px; 
    }

    /* Exemplo 5: Posição com valores em porcentagem */
    .exemplo-5 {
      background-position: 25% 75%;
    }

    /* Exemplo 6: Posição com palavra-chave e valor */
    .exemplo-6 {
      background-position: right 20px; 
    }
  </style>
</head>
<body>

  <h1>Exemplos de background-position</h1>

  <div class="container exemplo-1">
    <h2>Exemplo 1: Top Left</h2>
  </div>

  <div class="container exemplo-2">
    <h2>Exemplo 2: Center</h2>
  </div>

  <div class="container exemplo-3">
    <h2>Exemplo 3: Bottom Right</h2>
  </div>

  <div class="container exemplo-4">
    <h2>Exemplo 4: Pixels</h2>
  </div>

  <div class="container exemplo-5">
    <h2>Exemplo 5: Porcentagem</h2>
  </div>

  <div class="container exemplo-6">
    <h2>Exemplo 6: Right 20px</h2>
  </div>

</body>
</html>
```

**Explicação do código:**

* **`.container`:** Define um contêiner para cada exemplo, com largura, altura, margem, borda, imagem de fundo e `no-repeat` para evitar repetições.
* **Exemplos 1 a 6:** Cada classe `.exemplo-N` demonstra um uso diferente de `background-position`:
    * **Exemplo 1:** Posiciona a imagem no canto superior esquerdo (comportamento padrão).
    * **Exemplo 2:** Centraliza a imagem horizontalmente e verticalmente.
    * **Exemplo 3:** Posiciona a imagem no canto inferior direito.
    * **Exemplo 4:** Define a posição da imagem usando valores em pixels.
    * **Exemplo 5:** Define a posição da imagem usando valores em porcentagem.
    * **Exemplo 6:** Combina uma palavra-chave (`right`) com um valor em pixels (`20px`).

**Observações:**

* A propriedade `background-position` permite um controle preciso sobre o posicionamento da imagem de fundo.
* Você pode combinar diferentes unidades de medida (pixels, porcentagens, palavras-chave) para definir a posição da imagem.
* Experimente combinar `background-position` com outras propriedades de fundo para criar layouts mais dinâmicos e interessantes.
