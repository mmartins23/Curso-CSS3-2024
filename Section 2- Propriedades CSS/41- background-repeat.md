A propriedade `background-repeat` em CSS controla a repetição da imagem de fundo de um elemento. Ela define como a imagem será exibida quando as dimensões do elemento forem maiores que a própria imagem.

**Sintaxe básica:**

```css
background-repeat: valor;
```

Onde `valor` pode ser:

* `repeat`: Repete a imagem horizontalmente e verticalmente (valor padrão).
* `repeat-x`: Repete a imagem somente na horizontal.
* `repeat-y`: Repete a imagem somente na vertical.
* `no-repeat`: Não repete a imagem.
* `space`: Repete a imagem o máximo possível sem cortar, distribuindo o espaço restante entre as repetições.
* `round`: Semelhante a `space`, mas ajusta o tamanho das imagens para evitar espaços em branco.

**Exemplo completo em HTML com vários exemplos:**

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplos de background-repeat</title>
  <style>
    .container {
      width: 400px;
      height: 200px;
      margin: 20px auto;
      border: 1px solid #ccc;
      background-image: url('https://via.placeholder.com/100x100'); /* Imagem de fundo */
    }

    /* Exemplo 1: Repeat (padrão) */
    .exemplo-1 {
      background-repeat: repeat; 
    }

    /* Exemplo 2: Repeat-x */
    .exemplo-2 {
      background-repeat: repeat-x;
    }

    /* Exemplo 3: Repeat-y */
    .exemplo-3 {
      background-repeat: repeat-y;
    }

    /* Exemplo 4: No-repeat */
    .exemplo-4 {
      background-repeat: no-repeat;
    }

    /* Exemplo 5: Space */
    .exemplo-5 {
      background-repeat: space;
    }

    /* Exemplo 6: Round */
    .exemplo-6 {
      background-repeat: round;
    }
  </style>
</head>
<body>

  <h1>Exemplos de background-repeat</h1>

  <div class="container exemplo-1">
    <h2>Exemplo 1: Repeat</h2>
  </div>

  <div class="container exemplo-2">
    <h2>Exemplo 2: Repeat-x</h2>
  </div>

  <div class="container exemplo-3">
    <h2>Exemplo 3: Repeat-y</h2>
  </div>

  <div class="container exemplo-4">
    <h2>Exemplo 4: No-repeat</h2>
  </div>

  <div class="container exemplo-5">
    <h2>Exemplo 5: Space</h2>
  </div>

  <div class="container exemplo-6">
    <h2>Exemplo 6: Round</h2>
  </div>

</body>
</html>
```

**Explicação do código:**

* **`.container`:** Define um contêiner para cada exemplo, com largura, altura, margem, borda e a imagem de fundo.
* **Exemplos 1 a 6:** Cada classe `.exemplo-N` demonstra um valor diferente de `background-repeat`:
    * **Exemplo 1:** Repete a imagem em ambas as direções.
    * **Exemplo 2:** Repete a imagem somente na horizontal.
    * **Exemplo 3:** Repete a imagem somente na vertical.
    * **Exemplo 4:** Exibe a imagem uma única vez, sem repetição.
    * **Exemplo 5:** Repete a imagem sem cortar, adicionando espaços entre as repetições.
    * **Exemplo 6:** Repete a imagem sem cortar, ajustando o tamanho para preencher o espaço.

**Observações:**

* A propriedade `background-repeat` é frequentemente usada em conjunto com `background-image` para controlar a aparência do fundo de um elemento.
* Experimente combinar `background-repeat` com outras propriedades de fundo, como `background-position` e `background-size`, para obter efeitos visuais mais complexos.
* Utilize imagens otimizadas para web para garantir um bom desempenho do site.
