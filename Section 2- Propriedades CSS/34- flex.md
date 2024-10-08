A propriedade `flex` é uma shorthand (abreviação) que combina as três propriedades fundamentais do Flexbox em CSS: `flex-grow`, `flex-shrink` e `flex-basis`. Essa propriedade permite que você configure o comportamento de itens flexíveis dentro de um contêiner de forma compacta e eficiente.

### O que é `flex`

- **Definição**: A propriedade `flex` permite que você especifique como um item flexível deve crescer, encolher e qual deve ser o tamanho base dele. É uma maneira conveniente de definir esses três comportamentos em uma única linha.

### Sintaxe

A sintaxe da propriedade `flex` é:

```css
flex: <flex-grow> <flex-shrink> <flex-basis>;
```

- **`flex-grow`**: Um número que indica quanto o item deve crescer em relação a outros itens flexíveis.
- **`flex-shrink`**: Um número que indica quanto o item deve encolher em relação a outros itens flexíveis.
- **`flex-basis`**: O tamanho inicial do item antes do espaço extra ser distribuído.

### Valores Padrão

- `flex: 0 1 auto;`
  - `flex-grow`: 0 (não cresce)
  - `flex-shrink`: 1 (pode encolher)
  - `flex-basis`: auto (tamanho automático baseado no conteúdo)

### Exemplos de Código

#### Exemplo 1: Usando `flex` em um Contêiner Flex

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de flex</title>
    <style>
        .flex-container {
            display: flex;
            background-color: #f0f0f0;
            padding: 10px;
            height: 100px;
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
            flex: 1; /* Cresce e encolhe igualmente */
        }

        .item2 {
            flex: 2; /* Cresce o dobro do item 1 */
        }

        .item3 {
            flex: 1; /* Cresce e encolhe igualmente */
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
- Neste exemplo, o contêiner flex tem três itens.
- O `item1` e o `item3` têm `flex: 1`, enquanto o `item2` tem `flex: 2`. Isso significa que o `item2` ocupará duas vezes mais espaço do que os outros dois itens quando o espaço estiver disponível.

#### Exemplo 2: Usando `flex` com Valores Específicos

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de flex com tamanhos específicos</title>
    <style>
        .flex-container {
            display: flex;
            background-color: #f0f0f0;
            padding: 10px;
            height: 100px;
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
            flex: 1 1 100px; /* Cresce, encolhe e tem um tamanho base de 100px */
        }

        .item2 {
            flex: 0 1 200px; /* Não cresce, encolhe e tem um tamanho base de 200px */
        }

        .item3 {
            flex: 1 1 150px; /* Cresce, encolhe e tem um tamanho base de 150px */
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
- Neste exemplo, cada item tem uma configuração de `flex` que especifica como eles devem se comportar em relação ao crescimento e encolhimento.
- O `item1` pode crescer e encolher com um tamanho base de 100px, o `item2` não cresce mas pode encolher com um tamanho base de 200px, e o `item3` pode crescer e encolher com um tamanho base de 150px.

### Considerações Finais

- A propriedade `flex` é uma maneira poderosa e compacta de controlar o layout flexível de itens dentro de um contêiner.
- O uso adequado de `flex` permite criar layouts responsivos e dinâmicos que se adaptam a diferentes tamanhos de tela.
- É importante testar seu layout em várias resoluções para garantir que os itens se comportem como desejado em diferentes dispositivos.