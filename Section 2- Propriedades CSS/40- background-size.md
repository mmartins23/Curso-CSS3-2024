A propriedade `background-size` em CSS controla o tamanho das imagens de fundo. Com ela, você pode redimensionar, esticar, repetir ou cobrir um elemento com a imagem de fundo. 

**Sintaxe básica:**

```css
background-size: valor;
```

Onde `valor` pode ser:

* **Tamanho absoluto:** Define a largura e altura da imagem em pixels ou outras unidades de medida (ex: `100px`, `50%`).
* **Palavras-chave:**
    * `cover`: A imagem cobre toda a área do elemento, mantendo a proporção.
    * `contain`: A imagem é dimensionada para caber completamente dentro do elemento, mantendo a proporção.

**Exemplo completo em HTML com vários exemplos:**

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplos de background-size</title>
  <style>
    .container {
      width: 400px;
      height: 200px;
      margin: 20px auto;
      border: 1px solid #ccc;
      background-image: url('https://via.placeholder.com/300x200'); /* Imagem de fundo */
      background-repeat: no-repeat; /* Para não repetir a imagem */
    }

    /* Exemplo 1: Tamanho original */
    .exemplo-1 {
      background-size: auto; /* ou omitir a propriedade */
    }

    /* Exemplo 2: Tamanho definido em pixels */
    .exemplo-2 {
      background-size: 100px 50px; /* Largura 100px, altura 50px */
    }

    /* Exemplo 3: Tamanho definido em porcentagem */
    .exemplo-3 {
      background-size: 50% 100%; /* Largura 50%, altura 100% */
    }

    /* Exemplo 4: Cover */
    .exemplo-4 {
      background-size: cover;
    }

    /* Exemplo 5: Contain */
    .exemplo-5 {
      background-size: contain;
    }
  </style>
</head>
<body>

  <h1>Exemplos de background-size</h1>

  <div class="container exemplo-1">
    <h2>Exemplo 1: Tamanho original</h2>
  </div>

  <div class="container exemplo-2">
    <h2>Exemplo 2: Tamanho definido em pixels</h2>
  </div>

  <div class="container exemplo-3">
    <h2>Exemplo 3: Tamanho definido em porcentagem</h2>
  </div>

  <div class="container exemplo-4">
    <h2>Exemplo 4: Cover</h2>
  </div>

  <div class="container exemplo-5">
    <h2>Exemplo 5: Contain</h2>
  </div>

</body>
</html>
```

**Explicação do código:**

* **`.container`:** Define um contêiner para cada exemplo, com largura, altura, margem, borda e a imagem de fundo.
* **Exemplos 1 a 5:** Cada classe `.exemplo-N` demonstra um uso diferente de `background-size`:
    * **Exemplo 1:** Exibe a imagem no tamanho original.
    * **Exemplo 2:** Define o tamanho da imagem em pixels.
    * **Exemplo 3:** Define o tamanho da imagem em porcentagem em relação ao elemento.
    * **Exemplo 4:** A imagem cobre todo o elemento, mantendo a proporção e possivelmente cortando as bordas.
    * **Exemplo 5:** A imagem é totalmente contida no elemento, mantendo a proporção e possivelmente deixando espaços vazios.

**Observações:**

* Use imagens otimizadas para web para garantir um bom desempenho do site.
* Experimente diferentes valores e combinações de `background-size` com outras propriedades de fundo para obter o efeito desejado.
* A propriedade `background-size` oferece grande flexibilidade na manipulação de imagens de fundo, permitindo criar layouts mais dinâmicos e responsivos.
