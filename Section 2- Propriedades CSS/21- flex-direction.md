### Flex Direction no CSS3

A propriedade `flex-direction` no CSS define a direção dos itens dentro de um contêiner flexível (`flex-container`). Ela especifica como os itens flexíveis são dispostos dentro do contêiner, seja horizontalmente (em linhas) ou verticalmente (em colunas).

Existem quatro valores principais para `flex-direction`:

1. **`row`**: Os itens são dispostos na direção da linha (da esquerda para a direita, ou da direita para a esquerda em layouts RTL).
2. **`row-reverse`**: Os itens são dispostos em linha, mas a ordem é inversa (da direita para a esquerda).
3. **`column`**: Os itens são dispostos em colunas (de cima para baixo).
4. **`column-reverse`**: Os itens são dispostos em colunas, mas com a ordem invertida (de baixo para cima).

### Exemplo com Código

Aqui está um exemplo de cada valor de `flex-direction` em ação:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Flex Direction</title>
    <style>
        /* Estilo base para os contêineres flexíveis */
        .flex-container {
            display: flex;
            width: 100%;
            height: 200px;
            margin-bottom: 20px;
            background-color: lightgray;
        }

        /* Estilo base para os itens flexíveis */
        .flex-container div {
            background-color: lightblue;
            padding: 20px;
            margin: 10px;
            text-align: center;
            font-weight: bold;
        }

        /* Flex Direction: row (padrão) */
        .row {
            flex-direction: row;
        }

        /* Flex Direction: row-reverse */
        .row-reverse {
            flex-direction: row-reverse;
        }

        /* Flex Direction: column */
        .column {
            flex-direction: column;
        }

        /* Flex Direction: column-reverse */
        .column-reverse {
            flex-direction: column-reverse;
        }
    </style>
</head>
<body>
    <h2>Exemplo de flex-direction: row (padrão)</h2>
    <div class="flex-container row">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
    </div>

    <h2>Exemplo de flex-direction: row-reverse</h2>
    <div class="flex-container row-reverse">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
    </div>

    <h2>Exemplo de flex-direction: column</h2>
    <div class="flex-container column">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
    </div>

    <h2>Exemplo de flex-direction: column-reverse</h2>
    <div class="flex-container column-reverse">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
    </div>

</body>
</html>
```

### Explicação dos Valores:

1. **`row` (padrão)**:
   - O comportamento padrão do `flex-direction` é organizar os itens na direção de linha, da esquerda para a direita. Isso faz com que os itens sejam exibidos lado a lado em uma linha horizontal.

2. **`row-reverse`**:
   - Inverte a ordem dos itens na linha, ou seja, os itens são exibidos da direita para a esquerda.

3. **`column`**:
   - Organiza os itens em uma coluna vertical, ou seja, os itens são exibidos um embaixo do outro, começando de cima para baixo.

4. **`column-reverse`**:
   - Organiza os itens em uma coluna vertical, mas com a ordem invertida, ou seja, os itens são exibidos de baixo para cima.

### O que este código faz:
- Cada contêiner flexível (`flex-container`) exibe três itens organizados conforme o valor da propriedade `flex-direction`.
- Você verá a diferença na disposição dos itens com cada valor de `flex-direction`. No primeiro exemplo (`row`), os itens são exibidos de forma padrão em uma linha. No exemplo com `row-reverse`, a ordem é invertida. Nos exemplos com `column` e `column-reverse`, os itens aparecem em uma coluna vertical, com a ordem alterada no caso de `column-reverse`.

Essa propriedade é fundamental para controlar como os itens dentro de um contêiner flexível são exibidos, seja horizontalmente ou verticalmente.