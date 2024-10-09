### Explicação do `flex-basis` – Definindo o Tamanho Base:

A propriedade **`flex-basis`** define o **tamanho inicial** de um item flexível antes de o espaço extra disponível no contêiner ser distribuído ou de ocorrer encolhimento. Essencialmente, é o tamanho que o item flexível terá **antes de qualquer redimensionamento** ocorrer, e age como um valor de **largura** (no eixo principal) ou **altura** (no eixo transversal).

### Sintaxe:

```css
.item {
  flex-basis: <valor>;
}
```

- **Valor padrão:** `auto` (o item usa seu tamanho natural ou o valor de `width`/`height`).
- **Valores:** Pode ser um comprimento fixo (por exemplo, `100px`), uma porcentagem (`50%`), ou `auto` (ajusta ao conteúdo ou ao tamanho definido).

### Como Funciona:

- **`flex-basis: auto`**: O item utiliza seu conteúdo ou o valor de `width`/`height` especificado no CSS.
- **`flex-basis: <valor>`**: Define um tamanho base específico, como `200px` ou `50%`. Este valor serve como ponto de partida para qualquer ajuste que possa acontecer devido a outras propriedades flex (como `flex-grow` ou `flex-shrink`).
  
Se o valor for `auto`, o item tenta se ajustar de acordo com seu conteúdo ou qualquer valor de `width`/`height` aplicável. Quando um valor específico é definido, como `200px`, o item tenta começar com esse tamanho.

### Exemplo de Código Explicado:

Este exemplo demonstra diferentes usos da propriedade **`flex-basis`** em layouts Flexbox.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/flexbasis.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>flex-basis</code></h2>

    <!-- Cenário 1: Todos os itens têm flex-basis: auto (tamanho natural ou largura/altura) -->
    <p>Default: <code>flex-basis: auto</code></p>
    <div class="container">
      <div>1 <br>flex-basis: auto</div>
      <div>2 <br>flex-basis: auto</div>
      <div>3 <br>flex-basis: auto</div>
      <div>4 <br>flex-basis: auto</div>
    </div>

    <!-- Cenário 2: Itens com diferentes valores de flex-basis -->
    <p>Different <code>flex-basis</code> values (act like width on the main axis)</p>
    <div class="basis1 container">
      <div>1 <br>flex-basis: 200px</div>
      <div>2 <br>flex-basis: 300px</div>
      <div>3 <br>flex-basis: auto</div>
      <div>4 <br>flex-basis: 100px</div>
    </div>

    <!-- Cenário 3: Valores percentuais de flex-basis -->
    <p>Percent values (note that it's necessary to combine with <code>flex-shrink</code>)</p>
    <div class="basis2 container">
      <div>1 <br>flex-basis: 25%</div>
      <div>2 <br>flex-basis: auto</div>
      <div>3 <br>flex-basis: auto</div>
      <div>4 <br>flex-basis: 50%</div>
    </div>

  </body>
</html>
```

### Explicação de Cada Cenário:

#### Cenário 1: Itens com `flex-basis: auto`
```html
<div class="container">
  <div>1 <br>flex-basis: auto</div>
  <div>2 <br>flex-basis: auto</div>
  <div>3 <br>flex-basis: auto</div>
  <div>4 <br>flex-basis: auto</div>
</div>
```
- Neste caso, todos os itens têm **`flex-basis: auto`**, o que significa que cada item se ajustará ao seu conteúdo ou ao valor de `width` ou `height` definido no CSS. O navegador calcula o tamanho de cada item baseado em seu conteúdo natural.
  
#### Cenário 2: Itens com diferentes valores de `flex-basis`
```html
<div class="basis1 container">
  <div>1 <br>flex-basis: 200px</div>
  <div>2 <br>flex-basis: 300px</div>
  <div>3 <br>flex-basis: auto</div>
  <div>4 <br>flex-basis: 100px</div>
</div>
```
- Aqui, os itens têm diferentes valores de `flex-basis`, que atuam como a **largura base** no eixo principal (normalmente, a linha horizontal). Isso significa:
  - O primeiro item tem uma largura de **200px**.
  - O segundo item tem uma largura de **300px**.
  - O terceiro item tem **`auto`**, então ele ajustará sua largura conforme seu conteúdo.
  - O quarto item tem uma largura de **100px**.

#### Cenário 3: Itens com `flex-basis` em valores percentuais
```html
<div class="basis2 container">
  <div>1 <br>flex-basis: 25%</div>
  <div>2 <br>flex-basis: auto</div>
  <div>3 <br>flex-basis: auto</div>
  <div>4 <br>flex-basis: 50%</div>
</div>
```
- Aqui, o `flex-basis` é definido com valores percentuais, e o comportamento depende do espaço disponível no contêiner:
  - O primeiro item ocupa **25%** da largura total do contêiner.
  - O segundo e o terceiro itens têm **`auto`**, ajustando-se ao seu conteúdo.
  - O quarto item ocupa **50%** da largura do contêiner.
  
  Quando se utiliza valores percentuais para `flex-basis`, é importante que o **`flex-shrink`** seja combinado para evitar que o layout fique quebrado se o contêiner for muito pequeno para acomodar os itens em suas larguras percentuais.

### Código CSS:

```css
.basis1 div:nth-child(1) {
  flex-basis: 200px; /* Tamanho base do item 1 é 200px */
}

.basis1 div:nth-child(2) {
  flex-basis: 300px; /* Tamanho base do item 2 é 300px */
}

.basis1 div:nth-child(4) {
  flex-basis: 100px; /* Tamanho base do item 4 é 100px */
}

.basis2 div:nth-child(1) {
  flex-basis: 25%; /* O item 1 ocupa 25% do contêiner */
}

.basis2 div:nth-child(4) {
  flex-basis: 50%; /* O item 4 ocupa 50% do contêiner */
}
```

### Detalhes Importantes:

1. **`flex-basis: auto`**:
   - Neste caso, o valor de `flex-basis` é calculado automaticamente, geralmente com base no conteúdo do item ou em qualquer valor `width`/`height` especificado no CSS. Se não houver `width`/`height`, o conteúdo define o tamanho do item.

2. **Valores Fixos (como `200px`, `100px`)**:
   - Quando `flex-basis` é definido com um valor fixo, ele especifica o **tamanho inicial** do item antes de qualquer encolhimento ou crescimento. Se houver mais espaço disponível ou o contêiner for menor que a soma de todos os tamanhos `flex-basis`, o `flex-grow` e `flex-shrink` entram em ação para ajustar os itens.

3. **Valores Percentuais (como `25%`, `50%`)**:
   - Os valores percentuais de `flex-basis` são calculados em relação ao tamanho do contêiner. No exemplo, o primeiro item ocupa 25% da largura do contêiner, e o quarto item ocupa 50%. O restante do espaço é ocupado pelos itens com `auto` ou outros valores fixos.

4. **Combinação com `flex-shrink`**:
   - Quando se usa `flex-basis` com valores percentuais, pode ser necessário ajustar o `flex-shrink` para garantir que os itens encolham apropriadamente quando o espaço for limitado.

---

### Resumo:

- **`flex-basis`** define o **tamanho base inicial** de um item flexível, antes de qualquer redimensionamento.
- Pode ser um valor fixo (`200px`), percentual (`25%`), ou `auto` (tamanho natural).
- É fundamental para controlar o layout de itens flexíveis, especialmente em conjunto com `flex-grow` e `flex-shrink`, para criar designs dinâmicos e responsivos.
