A propriedade **`flex-grow`** controla como os itens flexíveis dentro de um contêiner flexível crescem para preencher o espaço disponível, caso haja espaço restante após a alocação do espaço mínimo necessário para cada item.

### Sintaxe:

```css
.item {
  flex-grow: <valor>;
}
```

- **Valor padrão:** `0` (os itens não crescem).
- **Valores:** Um número inteiro ou decimal que determina a proporção de crescimento em relação aos outros itens. 

Quando há espaço disponível no contêiner flexível (por exemplo, quando o contêiner tem mais largura do que os itens dentro dele precisam), **`flex-grow`** define o quanto cada item deve crescer para ocupar esse espaço extra.

### Como Funciona:

- **`flex-grow: 0`**: O item não cresce, ou seja, permanece com seu tamanho inicial, mesmo que haja espaço extra disponível.
- **`flex-grow: 1`**: O item cresce para ocupar uma parte igual do espaço restante em relação a outros itens com o mesmo valor de `flex-grow`.
- **`flex-grow: 2`**: O item cresce para ocupar o dobro do espaço em comparação com itens que têm `flex-grow: 1`.

### Exemplo de Código Explicado:

O código que você forneceu ilustra diferentes cenários com a propriedade **`flex-grow`**.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/flexgrow.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>flex-grow</code></h2>

    <!-- Cenário 1: Nenhum item cresce (flex-grow: 0 para todos) -->
    <p>Default: <code>flex-grow: 0</code> (remaining space not filled)</p>
    <div class="container">
      <div>1 <br>flex-grow: 0</div>
      <div>2 <br>flex-grow: 0</div>
      <div>3 <br>flex-grow: 0</div>
      <div>4 <br>flex-grow: 0</div>
    </div>

    <!-- Cenário 2: Apenas o item 3 cresce (flex-grow: 1 para o item 3) -->
    <p>3 allowed to take remaining space (<code>flex-grow: 1</code>)</p>
    <div class="grow1 container">
      <div>1 <br>flex-grow: 0</div>
      <div>2 <br>flex-grow: 0</div>
      <div>3 <br>flex-grow: 1</div>
      <div>4 <br>flex-grow: 0</div>
    </div>

    <!-- Cenário 3: Todos os itens crescem igualmente (flex-grow: 1 para todos) -->
    <p>Remaining space distributed equally (all have same <code>flex-grow</code>)</p>
    <div class="grow2 container">
      <div>1 <br>flex-grow: 1</div>
      <div>2 <br>flex-grow: 1</div>
      <div>3 <br>flex-grow: 1</div>
      <div>4 <br>flex-grow: 1</div>
    </div>

    <!-- Cenário 4: O item 3 cresce o dobro do espaço (flex-grow: 2 para o item 3) -->
    <p>3 gets 2/5 (40%) of remaining space (does not mean that 3 will be twice as wide)</p>
    <div class="grow3 container">
      <div>1 <br>flex-grow: 1</div>
      <div>2 <br>flex-grow: 1</div>
      <div>3 <br>flex-grow: 2</div>
      <div>4 <br>flex-grow: 1</div>
    </div>

    <!-- Cenário 5: O item 3 cresce quatro vezes o espaço (flex-grow: 4 para o item 3) -->
    <p>3 gets 4/7 of remaining space</p>
    <div class="grow4 container">
      <div>1 <br>flex-grow: 1</div>
      <div>2 <br>flex-grow: 1</div>
      <div>3 <br>flex-grow: 4</div>
      <div>4 <br>flex-grow: 1</div>
    </div>

  </body>
</html>
```

### Explicação de Cada Cenário:

#### Cenário 1: `flex-grow: 0` (comportamento padrão)
```html
<div class="container">
  <div>1 <br>flex-grow: 0</div>
  <div>2 <br>flex-grow: 0</div>
  <div>3 <br>flex-grow: 0</div>
  <div>4 <br>flex-grow: 0</div>
</div>
```
- Todos os itens têm **`flex-grow: 0`**, então eles mantêm seu tamanho inicial, e nenhum deles cresce para preencher o espaço restante no contêiner.

#### Cenário 2: Um item cresce (`flex-grow: 1` para o item 3)
```html
<div class="grow1 container">
  <div>1 <br>flex-grow: 0</div>
  <div>2 <br>flex-grow: 0</div>
  <div>3 <br>flex-grow: 1</div>
  <div>4 <br>flex-grow: 0</div>
</div>
```
- Aqui, o item 3 tem **`flex-grow: 1`**, então ele vai ocupar todo o espaço restante, enquanto os outros itens (1, 2, 4) mantêm seu tamanho fixo.

#### Cenário 3: Todos os itens crescem igualmente (`flex-grow: 1` para todos)
```html
<div class="grow2 container">
  <div>1 <br>flex-grow: 1</div>
  <div>2 <br>flex-grow: 1</div>
  <div>3 <br>flex-grow: 1</div>
  <div>4 <br>flex-grow: 1</div>
</div>
```
- Todos os itens têm **`flex-grow: 1`**, portanto, o espaço restante é distribuído igualmente entre os quatro itens.

#### Cenário 4: Um item cresce mais do que os outros (`flex-grow: 2` para o item 3)
```html
<div class="grow3 container">
  <div>1 <br>flex-grow: 1</div>
  <div>2 <br>flex-grow: 1</div>
  <div>3 <br>flex-grow: 2</div>
  <div>4 <br>flex-grow: 1</div>
</div>
```
- O item 3 tem **`flex-grow: 2`**, o que significa que ele vai ocupar o **dobro** do espaço disponível comparado aos outros itens (que têm **`flex-grow: 1`**). 
- O espaço total será dividido em 5 partes: o item 3 ficará com 2/5 do espaço, e cada um dos outros itens ficará com 1/5.

#### Cenário 5: Um item cresce ainda mais (`flex-grow: 4` para o item 3)
```html
<div class="grow4 container">
  <div>1 <br>flex-grow: 1</div>
  <div>2 <br>flex-grow: 1</div>
  <div>3 <br>flex-grow: 4</div>
  <div>4 <br>flex-grow: 1</div>
</div>
```
- Aqui, o item 3 tem **`flex-grow: 4`**, ou seja, ele vai ocupar **quatro vezes** o espaço que os itens 1, 2 e 4 ocupam (que têm **`flex-grow: 1`**). 
- O espaço total será dividido em 7 partes: o item 3 ficará com 4/7 do espaço, e cada um dos outros itens ficará com 1/7.

---

### Resumo:

- **`flex-grow`** é uma poderosa propriedade no Flexbox para controlar o quanto cada item flexível vai crescer em relação aos outros, usando proporções.
- Quando configurado, ele distribui o espaço restante entre os itens com base nos valores numéricos atribuídos.
- Isso permite flexibilidade para ajustar o layout de uma maneira responsiva e adaptativa, especialmente quando você deseja que certos itens tenham prioridade em ocupar o espaço restante.