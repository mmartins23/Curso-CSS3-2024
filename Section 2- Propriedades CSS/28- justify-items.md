A propriedade `justify-items` em CSS é utilizada em containers de layout CSS Grid para definir como os itens são justificados dentro de suas células. Essa propriedade controla o alinhamento horizontal dos itens dentro de suas áreas de grid.

### Valores da Propriedade `justify-items`
- **start**: Os itens são alinhados no início da célula (à esquerda).
- **end**: Os itens são alinhados no final da célula (à direita).
- **center**: Os itens são alinhados no centro da célula.
- **stretch**: Os itens são esticados para preencher a célula. Este é o valor padrão.

### Exemplo Completo em HTML
Abaixo está um exemplo completo em um único arquivo HTML que demonstra o uso da propriedade `justify-items` em um layout CSS Grid:

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplos de justify-items</title>
  <style>
    .grid-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      border: 1px solid #ccc;
      padding: 10px;
      margin-bottom: 20px;
    }

    .grid-item {
      border: 1px solid #000;
      padding: 20px;
      text-align: center;
    }

    /* Exemplo 1: justify-items: start */
    .exemplo-1 {
      justify-items: start; 
    }

    /* Exemplo 2: justify-items: end */
    .exemplo-2 {
      justify-items: end;
    }

    /* Exemplo 3: justify-items: center */
    .exemplo-3 {
      justify-items: center;
    }

    /* Exemplo 4: justify-items: stretch (padrão) */
    .exemplo-4 {
      justify-items: stretch; 
    }
  </style>
</head>
<body>

  <h2>Exemplo 1: justify-items: start</h2>
  <div class="grid-container exemplo-1">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
  </div>

  <h2>Exemplo 2: justify-items: end</h2>
  <div class="grid-container exemplo-2">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
  </div>

  <h2>Exemplo 3: justify-items: center</h2>
  <div class="grid-container exemplo-3">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
  </div>

  <h2>Exemplo 4: justify-items: stretch</h2>
  <div class="grid-container exemplo-4">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
  </div>

</body>
</html>
```


### Explicação dos Exemplos:
- **justify-items: start**: Os itens são alinhados à esquerda da célula.
- **justify-items: end**: Os itens são alinhados à direita da célula.
- **justify-items: center**: Os itens são centralizados na célula.
- **justify-items: stretch**: Os itens são esticados para preencher toda a largura da célula.

Você pode modificar os valores e estilos conforme necessário para experimentar diferentes resultados!