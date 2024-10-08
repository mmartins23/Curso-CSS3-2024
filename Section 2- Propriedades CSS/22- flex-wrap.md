### Flex Wrap no CSS3

A propriedade `flex-wrap` no CSS controla se os itens flexíveis dentro de um contêiner flexível devem ser mantidos em uma única linha ou se devem "quebrar" e se mover para a próxima linha quando não houver espaço suficiente. Essa propriedade é especialmente útil quando se trabalha com layouts responsivos, permitindo que os itens se ajustem de forma flexível conforme a largura do contêiner muda.

Existem três valores principais para a propriedade `flex-wrap`:

1. **`nowrap`**: Este é o valor padrão. Os itens flexíveis não vão quebrar e continuarão em uma única linha, mesmo que isso cause um estouro do contêiner.
2. **`wrap`**: Os itens flexíveis vão quebrar e se mover para a próxima linha quando não houver espaço suficiente na linha atual.
3. **`wrap-reverse`**: Os itens flexíveis vão quebrar e se mover para a próxima linha, mas a nova linha será exibida acima da linha anterior.

### Exemplo com Código

Aqui está um exemplo que demonstra como a propriedade `flex-wrap` funciona:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Flex Wrap</title>
    <style>
        /* Estilo base para os contêineres flexíveis */
        .flex-container {
            display: flex;
            width: 100%;
            height: 200px;
            margin-bottom: 20px;
            background-color: lightgray;
            flex-wrap: nowrap; /* Padrão */
            overflow: hidden; /* Esconder o conteúdo que não se ajusta */
        }

        /* Estilo base para os itens flexíveis */
        .flex-container div {
            background-color: lightblue;
            padding: 20px;
            margin: 10px;
            text-align: center;
            font-weight: bold;
            flex: 0 0 150px; /* Define a largura base dos itens */
        }

        /* Estilos para diferentes valores de flex-wrap */
        .wrap {
            flex-wrap: wrap;
        }

        .wrap-reverse {
            flex-wrap: wrap-reverse;
        }
    </style>
</head>
<body>

    <h2>Exemplo de flex-wrap: nowrap (padrão)</h2>
    <div class="flex-container">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
        <div>Item 4</div>
        <div>Item 5</div>
    </div>

    <h2>Exemplo de flex-wrap: wrap</h2>
    <div class="flex-container wrap">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
        <div>Item 4</div>
        <div>Item 5</div>
    </div>

    <h2>Exemplo de flex-wrap: wrap-reverse</h2>
    <div class="flex-container wrap-reverse">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
        <div>Item 4</div>
        <div>Item 5</div>
    </div>

</body>
</html>
```

### Explicação dos Valores:

1. **`nowrap` (padrão)**:
   - Os itens flexíveis não quebram. Eles são exibidos em uma única linha, e se houver mais itens do que o espaço disponível, eles podem sair do contêiner. No exemplo, o contêiner é definido com largura total e não permite que os itens se movam para a linha seguinte. 

2. **`wrap`**:
   - Os itens flexíveis quebram e se movem para a próxima linha quando não há espaço suficiente. Nesse exemplo, você verá que quando a largura do contêiner é insuficiente para acomodar todos os itens, eles se reorganizam em linhas subsequentes.

3. **`wrap-reverse`**:
   - Os itens flexíveis também quebram para a próxima linha, mas a nova linha é exibida acima da linha anterior. Assim, no exemplo, você verá que a ordem dos itens muda, colocando os itens que normalmente estariam na linha inferior na linha superior.

### O que este código faz:
- Cada contêiner flexível (`flex-container`) apresenta cinco itens.
- Com `flex-wrap: nowrap`, todos os itens são mantidos em uma única linha e podem sair do contêiner se a largura não for suficiente.
- Com `flex-wrap: wrap`, os itens quebram e se movem para a linha seguinte quando não há espaço suficiente.
- Com `flex-wrap: wrap-reverse`, os itens também quebram, mas a nova linha é exibida acima, invertendo a ordem dos itens.

Essa propriedade é crucial para o design responsivo, pois permite que os itens se ajustem conforme o tamanho do contêiner, melhorando a usabilidade e a estética do layout.