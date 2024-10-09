A propriedade **`flex-shrink`** é usada em layouts Flexbox para definir se e como um item flexível pode **encolher** caso o espaço no contêiner flexível seja insuficiente para acomodar todos os itens no seu tamanho ideal.

### Sintaxe:

```css
.item {
  flex-shrink: <valor>;
}
```

- **Valor padrão:** `1` (os itens podem encolher se necessário).
- **Valores:** Um número inteiro ou decimal que determina a **proporção** de encolhimento em relação aos outros itens.

### Como Funciona:

- **`flex-shrink: 0`**: O item **não encolhe** quando o contêiner tem menos espaço do que o necessário para exibir todos os itens no seu tamanho ideal.
- **`flex-shrink: 1`**: O item encolhe proporcionalmente aos outros itens flexíveis se houver menos espaço disponível.
- **Números maiores que 1** indicam que o item encolherá mais rapidamente do que os itens que têm um valor de `flex-shrink` menor.

Ou seja, a propriedade **`flex-shrink`** determina **a proporção em que um item pode encolher** em relação aos outros, quando o espaço dentro do contêiner é menor do que o necessário.

### Exemplo de Código Explicado:

O código que você forneceu demonstra diferentes cenários de uso da propriedade **`flex-shrink`**.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/flexshrink.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>flex-shrink</code></h2>

    <!-- Cenário 1: Todos os itens podem encolher igualmente (flex-shrink: 1) -->
    <p>Default: <code>flex-shrink: 1</code> (flex items are allowed to shrink to some degree)</p>
    <div class="container">
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 1</div>
    </div>

    <!-- Cenário 2: Alguns itens não podem encolher (flex-shrink: 0) -->
    <p>3, 4, and 5 are no longer allowed to shrink (<code>flex-shrink: 0</code>)</p>
    <div class="shrink1 container">
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 0</div>
      <div>flex-<br>shrink: 0</div>
      <div>flex-<br>shrink: 0</div>
      <div>flex-<br>shrink: 1</div>
    </div>

    <!-- Cenário 3: Um item encolhe mais rápido que os outros (flex-shrink: 5) -->
    <p>3 and 4 are allowed to shrink more compared to other flex items</p>
    <div class="shrink2 container">
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 5</div>
      <div>flex-<br>shrink: 1</div>
      <div>flex-<br>shrink: 1</div>
    </div>

  </body>
</html>
```

### Explicação de Cada Cenário:

#### Cenário 1: Todos os itens podem encolher igualmente (`flex-shrink: 1`)
```html
<div class="container">
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 1</div>
</div>
```
- Aqui, todos os itens têm **`flex-shrink: 1`**, o que significa que eles podem encolher igualmente se o contêiner for menor que o espaço necessário para o layout. Se não houver espaço suficiente, todos os itens encolherão na mesma proporção.

#### Cenário 2: Alguns itens não podem encolher (`flex-shrink: 0` para os itens 3, 4 e 5)
```html
<div class="shrink1 container">
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 0</div>
  <div>flex-<br>shrink: 0</div>
  <div>flex-<br>shrink: 0</div>
  <div>flex-<br>shrink: 1</div>
</div>
```
- Aqui, os itens 3, 4 e 5 têm **`flex-shrink: 0`**, ou seja, eles **não encolherão** quando o espaço for insuficiente. Os outros itens, com **`flex-shrink: 1`**, poderão encolher conforme necessário.
- O resultado é que os itens 3, 4 e 5 manterão seu tamanho fixo, enquanto os itens 1, 2 e 6 encolherão para ajustar-se ao espaço restante.

#### Cenário 3: Um item encolhe mais rápido (`flex-shrink: 5` para o item 3)
```html
<div class="shrink2 container">
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 5</div>
  <div>flex-<br>shrink: 1</div>
  <div>flex-<br>shrink: 1</div>
</div>
```
- Neste caso, o item 3 tem **`flex-shrink: 5`**, o que significa que ele **encolherá cinco vezes mais** do que os outros itens que têm **`flex-shrink: 1`**.
- Quando o espaço se torna insuficiente, o item 3 encolherá significativamente mais rápido que os outros, permitindo que os itens 1, 2, 4 e 5 mantenham mais de seu tamanho original.

### Código CSS:

```css
.container {
  flex-wrap: nowrap; /* Os itens não podem quebrar para uma nova linha */
  border: 1px solid #fff;
  border-radius: 2px;
}

.container div {
  flex-basis: 200px; /* Define o tamanho base inicial dos itens */
}

.shrink1 div:nth-child(3),
.shrink1 div:nth-child(4),
.shrink1 div:nth-child(5) {
  flex-shrink: 0; /* Impede o encolhimento dos itens 3, 4 e 5 */
}

.shrink2 div:nth-child(3) {
  flex-shrink: 5; /* O item 3 encolhe 5 vezes mais rápido do que os outros */
}
```

### Explicação Detalhada:

1. **`flex-wrap: nowrap`**: Especifica que os itens dentro do contêiner não podem quebrar para uma nova linha, mesmo que não haja espaço suficiente.
2. **`flex-basis: 200px`**: Define um tamanho base de 200px para cada item. Esse é o tamanho que o item teria se não houvesse encolhimento ou crescimento aplicado.
3. **`flex-shrink: 0`**: No cenário 2, esta regra é aplicada aos itens 3, 4 e 5, impedindo-os de encolher. Isso garante que esses itens mantenham seu tamanho original.
4. **`flex-shrink: 5`**: No cenário 3, esta regra faz com que o item 3 encolha 5 vezes mais rápido que os outros itens (que têm `flex-shrink: 1`).

---

### Resumo:

- **`flex-shrink`** controla como um item flexível pode encolher quando não há espaço suficiente no contêiner.
- O valor padrão é `1`, o que significa que os itens podem encolher igualmente.
- Valores maiores fazem o item encolher mais rápido, enquanto **`flex-shrink: 0`** impede o item de encolher.
- A propriedade é útil para layouts responsivos, especialmente quando você precisa priorizar quais itens devem encolher mais ou menos em espaços restritos.