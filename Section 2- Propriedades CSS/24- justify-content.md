### Justify Content no CSS3

A propriedade `justify-content` é usada em um contêiner flexível (ou em um grid) para alinhar os itens flexíveis ao longo do eixo principal (horizontal, se `flex-direction` estiver definido como `row`, ou vertical, se estiver definido como `column`). Essa propriedade ajuda a distribuir o espaço extra entre os itens ou ao redor deles, proporcionando um controle mais refinado sobre o layout.

### Valores da Propriedade

A propriedade `justify-content` pode receber os seguintes valores:

1. **`flex-start`** (padrão): Os itens são alinhados no início do contêiner (à esquerda em `row` e ao topo em `column`).
   
2. **`flex-end`**: Os itens são alinhados no final do contêiner (à direita em `row` e na parte inferior em `column`).

3. **`center`**: Os itens são centralizados ao longo do eixo principal.

4. **`space-between`**: Os itens são distribuídos uniformemente, com o primeiro item alinhado ao início e o último item alinhado ao final do contêiner, e o espaço restante é distribuído igualmente entre os itens.

5. **`space-around`**: Os itens são distribuídos com espaço igual ao redor de cada item. O espaço entre os itens será o dobro do espaço em cada extremidade.

6. **`space-evenly`**: Os itens são distribuídos de forma que o espaço entre qualquer dois itens adjacentes e o espaço entre os itens e as extremidades do contêiner sejam todos iguais.

### Exemplo com Código

Aqui está um exemplo que demonstra como a propriedade `justify-content` funciona:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Justify Content:</title>
    <style>
        .flex-start {
            display: flex;
            justify-content: flex-start;
            background-color: lightgray;
            padding: 10px;
            border: 1px solid #ccc;
        }

        .flex-end {
            display: flex;
            justify-content: flex-end;
            background-color: lightgray;
            padding: 10px;
            border: 1px solid #ccc;
        }
        .flex-center {
            display: flex;
            justify-content: center;
            background-color: lightgray;
            padding: 10px;
            border: 1px solid #ccc;
        }
        .flex-space-between {
            display: flex;
            justify-content: space-between;
            background-color: lightgray;
            padding: 10px;
            border: 1px solid #ccc;
        }
        .flex-space-around{
            display: flex;
            justify-content: space-around;
            background-color: lightgray;
            padding: 10px;
            border: 1px solid #ccc;
        }
        .flex-space-evenly {
            display: flex;
            justify-content: space-evenly;
            background-color: lightgray;
            padding: 10px;
            border: 1px solid #ccc;
        }
        .box {
            background-color: lightblue;
            padding: 20px;
            margin: 5px;
        }
    </style>
</head>

<body>
    <h2>Justify Content: flex-start</h2>
    <h3>flex-start: Os itens são alinhados no início do contêiner.</h3>
    <div class="flex-start">
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
    </div>

    <h2>Justify Content: flex-end</h2>
    <h3>flex-end: Os itens são alinhados no final do contêiner.</h3>
    <div class="flex-end">
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
    </div>

    <h2>Justify Content: center</h2>
    <h3>center: Os itens são centralizados no contêiner.</h3>
    <div class="flex-center">
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
    </div>

    <h2>Justify Content: space-between</h2>
    <h3>space-between: Os itens são distribuídos uniformemente com o primeiro item alinhado ao início e o último item alinhado ao final.</h3>
    <div class="flex-space-between">
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
    </div>

    <h2>Justify Content: space-around</h2>
    <h3>space-around: Os itens são distribuídos uniformemente, com espaço ao redor de cada item.
    </h3>
    <div class="flex-space-around">
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
    </div>

    <h2>Justify Content: space-evenly</h2>
    <h3>space-evenly: Os itens são distribuídos uniformemente, com o mesmo espaço ao redor e entre eles.
    </h3>
    <div class="flex-space-evenly">
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
    </div>
</body>

</html>
```

### Explicação dos Exemplos:

1. **`flex-start` (padrão)**:
   - Os itens são alinhados ao início do contêiner, ou seja, à esquerda. Isso é o comportamento padrão dos contêineres flexíveis.

2. **`flex-end`**:
   - Os itens são alinhados ao final do contêiner, ou seja, à direita.

3. **`center`**:
   - Os itens são centralizados no contêiner. Todos os itens aparecem no meio do contêiner.

4. **`space-between`**:
   - Os itens são distribuídos de modo que o primeiro item esteja no início do contêiner e o último no final. O espaço restante entre os itens é distribuído uniformemente.

5. **`space-around`**:
   - Os itens são distribuídos com espaço igual ao redor de cada item. O espaço em cada extremidade do contêiner é metade do espaço entre os itens.

6. **`space-evenly`**:
   - Os itens são distribuídos de modo que o espaço entre quaisquer dois itens adjacentes e o espaço em cada extremidade do contêiner sejam todos iguais.

### O que este código faz:
- Cada contêiner flexível (`flex-container`) apresenta três itens.
- O código demonstra como a propriedade `justify-content` altera o alinhamento e a distribuição dos itens no contêiner, mostrando claramente as diferenças entre os diferentes valores que podem ser utilizados.

A propriedade `justify-content` é essencial para criar layouts flexíveis e responsivos, permitindo um controle mais preciso sobre como os itens são dispostos dentro do contêiner.