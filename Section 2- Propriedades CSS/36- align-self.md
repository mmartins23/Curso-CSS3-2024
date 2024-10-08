A propriedade `align-self` no CSS é usada para ajustar o alinhamento de um item flexível em relação ao eixo transversal (perpendicular ao eixo principal) dentro de um contêiner flexível. Enquanto a propriedade `align-items` alinha todos os itens de um contêiner, `align-self` permite que você sobrescreva esse comportamento para um item específico.

### O que é `align-self`

- **Definição**: A propriedade `align-self` define como um item flexível deve ser alinhado em relação aos outros itens do contêiner. Você pode usar `align-self` para alinhar um único item de forma diferente do restante dos itens.

### Sintaxe

A sintaxe da propriedade `align-self` é:

```css
align-self: <value>;
```

#### Valores possíveis

- **`auto`**: O valor padrão. O item usará o valor da propriedade `align-items` do contêiner pai.
- **`flex-start`**: Alinha o item no início do contêiner.
- **`flex-end`**: Alinha o item no final do contêiner.
- **`center`**: Alinha o item no centro do contêiner.
- **`baseline`**: Alinha o item na linha de base do contêiner.
- **`stretch`**: O item ocupará o espaço disponível no eixo transversal (padrão para itens flexíveis).

### Exemplos de Código

#### Exemplo 1: Usando `align-self` para Alinhamento Personalizado

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de align-self</title>
    <style>
        .flex-container {
            display: flex;
            height: 200px;
            background-color: #f0f0f0;
            align-items: flex-start; /* Alinha todos os itens no início */
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
            align-self: flex-start; /* Alinha este item no início */
        }

        .item2 {
            align-self: center; /* Alinha este item no centro */
        }

        .item3 {
            align-self: flex-end; /* Alinha este item no final */
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
- Neste exemplo, o contêiner flex tem três itens, todos alinhados ao início por padrão (`align-items: flex-start`).
- O `item1` é alinhado no início, o `item2` é centralizado e o `item3` é alinhado ao final, demonstrando como `align-self` pode sobrescrever o alinhamento padrão.

#### Exemplo 2: Usando `align-self` com `stretch`

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de align-self com stretch</title>
    <style>
        .flex-container {
            display: flex;
            height: 200px;
            background-color: #f0f0f0;
            align-items: stretch; /* Faz todos os itens esticarem para ocupar o espaço disponível */
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
            height: 50px; /* Altura fixa */
            align-self: flex-start; /* Este item será alinhado no início */
        }

        .item2 {
            align-self: stretch; /* Este item se esticará para ocupar o espaço disponível */
        }

        .item3 {
            height: 30px; /* Altura fixa */
            align-self: flex-end; /* Este item será alinhado no final */
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
- Aqui, o contêiner flex está configurado para esticar todos os itens (`align-items: stretch`).
- O `item1` tem uma altura fixa e é alinhado ao início, o `item2` se estica para ocupar todo o espaço disponível, e o `item3` tem uma altura fixa e é alinhado ao final.

### Considerações Finais

- A propriedade `align-self` é útil quando você precisa de um alinhamento específico para itens individuais em um layout flexível.
- Com `align-self`, é possível criar layouts complexos e responsivos de maneira intuitiva.
- Essa propriedade é aplicada apenas a itens dentro de um contêiner com `display: flex` ou `display: inline-flex`.