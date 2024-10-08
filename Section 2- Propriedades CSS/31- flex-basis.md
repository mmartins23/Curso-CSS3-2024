A propriedade `flex-basis` é uma das três propriedades fundamentais que compõem o modelo de layout Flexbox em CSS, juntamente com `flex-grow` e `flex-shrink`. O `flex-basis` define a base inicial do tamanho de um item flexível antes que o espaço restante do contêiner seja distribuído. Isso significa que o `flex-basis` determina qual será o tamanho inicial de um item, independentemente de suas propriedades de crescimento e encolhimento.

### O que é `flex-basis`

- **Definição**: O `flex-basis` especifica o tamanho inicial de um item flexível. Ele pode ser definido em unidades de medida fixas (como pixels, em, rem) ou em unidades relativas (como porcentagem). O valor padrão é `auto`, o que significa que o tamanho inicial do item será determinado por seu conteúdo ou pelas propriedades de tamanho (como `width` ou `height`).

### Valores de `flex-basis`

- **`auto`**: O tamanho do item é baseado nas propriedades de tamanho do próprio item, como `width` ou `height`.
- **Um valor fixo (por exemplo, `200px`, `50%`)**: O item terá esse tamanho fixo como base antes de aplicar o crescimento ou encolhimento.

### Exemplo de Código

Aqui estão alguns exemplos práticos de como usar a propriedade `flex-basis`:

#### Exemplo 1: Usando `flex-basis` em um Contêiner Flex

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de flex-basis</title>
    <style>
        .flex-container {
            display: flex;
            justify-content: space-between;
            background-color: #f0f0f0;
            padding: 10px;
        }

        .flex-item {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 20px;
            margin: 5px;
            border: 1px solid #ccc;
        }

        .item1 {
            flex-basis: 200px; /* Tamanho inicial de 200px */
        }

        .item2 {
            flex-basis: 100px; /* Tamanho inicial de 100px */
        }

        .item3 {
            flex-basis: 150px; /* Tamanho inicial de 150px */
        }
    </style>
</head>
<body>

<div class="flex-container">
    <div class="flex-item item1">Item 1</div>
    <div class="flex-item item2">Item 2</div>
    <div class="flex-item item3">Item 3</div>
</div>

</body>
</html>
```

**Explicação do Exemplo:**
- Neste exemplo, criamos um contêiner flex com três itens.
- Cada item tem um `flex-basis` diferente, que determina seu tamanho inicial antes de qualquer espaço adicional ser distribuído.

#### Exemplo 2: Usando `flex-basis` com `flex-grow` e `flex-shrink`

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de flex-basis com crescimento e encolhimento</title>
    <style>
        .flex-container {
            display: flex;
            justify-content: space-around;
            background-color: #f0f0f0;
            padding: 10px;
            height: 200px;
        }

        .flex-item {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 20px;
            margin: 5px;
            border: 1px solid #ccc;
        }

        .item1 {
            flex-basis: 200px; /* Tamanho inicial de 200px */
            flex-grow: 1; /* Permite que o item cresça */
        }

        .item2 {
            flex-basis: 150px; /* Tamanho inicial de 150px */
            flex-grow: 2; /* Permite que o item cresça mais do que o item 1 */
        }

        .item3 {
            flex-basis: 100px; /* Tamanho inicial de 100px */
            flex-grow: 1; /* Permite que o item cresça */
        }
    </style>
</head>
<body>

<div class="flex-container">
    <div class="flex-item item1">Item 1</div>
    <div class="flex-item item2">Item 2</div>
    <div class="flex-item item3">Item 3</div>
</div>

</body>
</html>
```

**Explicação do Exemplo:**
- Neste exemplo, os itens flex têm um `flex-basis` definido, mas também têm valores de `flex-grow` diferentes.
- O `item2` com `flex-grow: 2` crescerá mais do que os outros itens, que têm `flex-grow: 1`, resultando em uma distribuição de espaço diferente, mesmo com bases iniciais diferentes.

### Considerações Finais

- O `flex-basis` é uma maneira poderosa de controlar o tamanho inicial de itens em um layout flexível.
- O uso de `flex-basis` combinado com `flex-grow` e `flex-shrink` permite criar layouts responsivos e dinâmicos que se adaptam bem ao espaço disponível.
- É importante testar e visualizar o resultado em diferentes tamanhos de tela para garantir que o layout se comporte como desejado em dispositivos variados.