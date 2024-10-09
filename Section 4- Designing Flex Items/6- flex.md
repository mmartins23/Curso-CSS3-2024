### Propriedade `flex` em Detalhes:

A propriedade **`flex`** é uma abreviação para três subpropriedades: **`flex-grow`**, **`flex-shrink`**, e **`flex-basis`**. Juntas, elas determinam como os itens flexíveis se comportam dentro de um contêiner flex (normalmente um contêiner definido com `display: flex`).

#### Sintaxe da Propriedade `flex`:

```css
.item {
  flex: <grow> <shrink> <basis>;
}
```

1. **`flex-grow`**: Define a capacidade do item de crescer, ocupando o espaço extra disponível no contêiner.
   - Valor padrão: `0` (não cresce).
   - Valor típico: `1` (cresce proporcionalmente).
   
2. **`flex-shrink`**: Define a capacidade do item de encolher quando o espaço do contêiner é limitado.
   - Valor padrão: `1` (o item pode encolher se necessário).
   - Valor `0`: o item não encolherá.
   
3. **`flex-basis`**: Define o tamanho base inicial do item antes de qualquer crescimento ou encolhimento.
   - Valor padrão: `auto`.
   - Pode ser definido como um valor fixo (`100px`), percentual (`25%`), ou `auto`.

#### Valores Abreviados:

- **`flex: 1`** é uma forma curta de escrever `flex: 1 1 0%`. Isso significa que o item pode crescer para ocupar espaço extra, pode encolher se necessário, e seu tamanho base inicial é `0%`.

### Exemplo Explicado:

O código HTML abaixo demonstra diferentes usos da propriedade `flex` em layouts flexbox.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/growshrinkbasis.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>flex</code></h2>

    <!-- Cenário 1: Flex padrão (flex: 0 1 auto) -->
    <p>Default: <code>flex: 0 1 auto</code> (grow, shrink, basis)</p>
    <div class="container">
      <div>1 <br>flex: 0 1 auto</div>
      <div>2 <br>flex: 0 1 auto</div>
      <div>3 <br>flex: 0 1 auto</div>
      <div>4 <br>flex: 0 1 auto</div>
    </div>

    <!-- Cenário 2: Flex com valor abreviado (flex: 1) -->
    <p><code>flex: 1</code> is the same as <code>flex: 1 1 0%</code></p>
    <div class="gallery1 container">
      <div>1 <br>flex: 1</div>
      <div>2 <br>flex: 1</div>
      <div>3 <br>flex: 1</div>
      <div>4 <br>flex: 1</div>
      <div>5 <br>flex: 1</div>
      <div>6 <br>flex: 1</div>
      <div>7 <br>flex: 1</div>
      <div>8 <br>flex: 1</div>
    </div>

    <!-- Cenário 3: Flex com largura percentual fixa (25%) -->
    <p>Flex items stick to 25% width (works due to <code>flex-wrap: nowrap</code>, thus only for one row)</p>
    <div class="gallery2 container">
      <div>1 <br>flex: 1 1 25%</div>
      <div>2 <br>flex: 1 1 25%</div>
      <div>3 <br>flex: 1 1 25%</div>
      <div>4 <br>flex: 1 1 25%</div>
    </div>

    <!-- Cenário 4: Combinação de flex-grow, flex-shrink, e flex-basis -->
    <p>Example from <code>flex-basis</code> section, now combined with other properties</p>
    <div class="gallery3 container">
      <div>1 <br>flex: 0 1 25%</div>
      <div>2 <br>flex: 1 1 auto</div>
      <div>3 <br>flex: 1 1 auto</div>
      <div>4 <br>flex: 0 1 50%</div>
    </div>

  </body>
</html>
```

### Explicação de Cada Cenário:

#### Cenário 1: Itens com `flex: 0 1 auto`
```html
<div class="container">
  <div>1 <br>flex: 0 1 auto</div>
  <div>2 <br>flex: 0 1 auto</div>
  <div>3 <br>flex: 0 1 auto</div>
  <div>4 <br>flex: 0 1 auto</div>
</div>
```
- Neste cenário, cada item tem o comportamento padrão `flex: 0 1 auto`. Isso significa que:
  - **`flex-grow: 0`**: Os itens não crescerão, mesmo que haja espaço extra no contêiner.
  - **`flex-shrink: 1`**: Os itens podem encolher se necessário, se o espaço for limitado.
  - **`flex-basis: auto`**: O tamanho base de cada item é definido pelo seu conteúdo ou pelo valor de `width`/`height`.

#### Cenário 2: Itens com `flex: 1`
```html
<div class="gallery1 container">
  <div>1 <br>flex: 1</div>
  <div>2 <br>flex: 1</div>
  <div>3 <br>flex: 1</div>
  <div>4 <br>flex: 1</div>
  <div>5 <br>flex: 1</div>
  <div>6 <br>flex: 1</div>
  <div>7 <br>flex: 1</div>
  <div>8 <br>flex: 1</div>
</div>
```
- Aqui, todos os itens têm `flex: 1`, que é equivalente a `flex: 1 1 0%`. Isso significa que:
  - **`flex-grow: 1`**: Os itens crescerão proporcionalmente para ocupar o espaço extra.
  - **`flex-shrink: 1`**: Os itens encolherão se necessário.
  - **`flex-basis: 0%`**: O tamanho base inicial é `0`, ou seja, os itens começam com zero e depois crescem para ocupar o espaço.

#### Cenário 3: Itens com largura fixa de 25%
```html
<div class="gallery2 container">
  <div>1 <br>flex: 1 1 25%</div>
  <div>2 <br>flex: 1 1 25%</div>
  <div>3 <br>flex: 1 1 25%</div>
  <div>4 <br>flex: 1 1 25%</div>
</div>
```
- Neste cenário, cada item tem `flex: 1 1 25%`, o que significa que:
  - **`flex-grow: 1`**: Os itens podem crescer se houver espaço extra.
  - **`flex-shrink: 1`**: Os itens podem encolher se o espaço for limitado.
  - **`flex-basis: 25%`**: Cada item tem uma largura inicial de 25% do contêiner. Como o contêiner usa `flex-wrap: nowrap`, todos os itens são dispostos em uma única linha e ocupam 25% da largura.

#### Cenário 4: Combinação de diferentes valores de `flex-grow`, `flex-shrink` e `flex-basis`
```html
<div class="gallery3 container">
  <div>1 <br>flex: 0 1 25%</div>
  <div>2 <br>flex: 1 1 auto</div>
  <div>3 <br>flex: 1 1 auto</div>
  <div>4 <br>flex: 0 1 50%</div>
</div>
```
- Aqui, os itens têm diferentes combinações de `flex`:
  - O primeiro item tem `flex: 0 1 25%`, ou seja:
    - **`flex-grow: 0`**: O item não crescerá, mesmo que haja espaço extra.
    - **`flex-shrink: 1`**: O item pode encolher se necessário.
    - **`flex-basis: 25%`**: O tamanho base inicial é 25% da largura do contêiner.
  - O segundo e terceiro itens têm `flex: 1

 1 auto` (crescem, encolhem, e têm tamanho base `auto`).
  - O quarto item tem `flex: 0 1 50%`, o que significa que ele não crescerá, mas pode encolher, com um tamanho base inicial de 50%.

### Resumo:
- **`flex`** é uma poderosa propriedade CSS para controlar o tamanho, crescimento e encolhimento de itens dentro de um contêiner flexível.
- Valores de `flex-grow`, `flex-shrink` e `flex-basis` podem ser combinados para criar layouts flexíveis e responsivos.
- O comportamento dos itens flex pode ser ajustado para permitir que eles cresçam, encolham ou mantenham tamanhos fixos em diferentes situações.
