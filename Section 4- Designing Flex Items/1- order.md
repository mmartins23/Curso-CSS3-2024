A propriedade **`order`** no CSS Flexbox permite reordenar os itens dentro de um contêiner flexível. Embora a ordem visual dos itens no HTML seja de cima para baixo (ou da esquerda para a direita em layout horizontal), a propriedade **`order`** permite modificar essa sequência, sem alterar a ordem no HTML. Isso pode ser útil para reposicionar itens específicos sem reescrever o código HTML.

### Sintaxe de `order`:

```css
.item {
  order: <integer>;
}
```

- **`order`** aceita valores inteiros (positivos, negativos ou zero). Por padrão, todos os itens têm o valor de **`order: 0`**.
  - **Valores negativos** movem o item para o início da ordem.
  - **Valores positivos** movem o item para o final da ordem.

### Detalhes da Propriedade `order`:

1. **Padrão (`order: 0`)**:
   - Todos os itens começam com o valor `0`, ou seja, eles aparecem na mesma ordem em que estão no HTML.
   
2. **Valores Negativos**:
   - Se você atribuir um valor negativo ao `order`, o item será movido para antes dos itens com `order` zero ou positivo.
   
3. **Valores Positivos**:
   - Um valor positivo moverá o item para depois dos itens com `order` zero ou negativo.

---

### Exemplo de Código:

Aqui está o exemplo que você forneceu com explicação:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Flexbox Grids</title>
    <link rel="stylesheet" href="css/showcase.css">
    <link rel="stylesheet" href="css/order.css">
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:300" rel="stylesheet">
  </head>
  <body>

    <h2>Property: <code>order</code></h2>

    <!-- Padrão: Todos os itens com `order: 0` (sem reordenação) -->
    <p>Default order</p>
    <div class="container">
      <div>1 <br>order: 0</div>
      <div>2 <br>order: 0</div>
      <div>3 <br>order: 0</div>
      <div>4 <br>order: 0</div>
    </div>

    <!-- Customizando a ordem dos itens 2 e 3 -->
    <p>2 and 3 with custom order</p>
    <div class="order1 container">
      <div>1 <br>order: 0</div>
      <div>2 <br>order: -1</div> <!-- Este item vai aparecer antes do item 1 -->
      <div>3 <br>order: 1</div>  <!-- Este item vai aparecer após os outros -->
      <div>4 <br>order: 0</div>
    </div>

    <!-- Todos os itens com `order` diferente -->
    <p>All with custom order</p>
    <div class="order2 container">
      <div>1 <br>order: 3</div>  <!-- Este item vai aparecer por último -->
      <div>2 <br>order: 2</div>  <!-- Este item vai aparecer antes do item 1 -->
      <div>3 <br>order: 1</div>  <!-- Este item vai aparecer antes do item 2 -->
      <div>4 <br>order: 2</div>  <!-- Este item vai aparecer junto com o item 2, mas na ordem original -->
    </div>

  </body>
</html>
```

### Explicação do Código:

1. **Primeira Seção (Padrão)**:
   - Todos os itens dentro do contêiner têm o valor padrão de **`order: 0`**. Portanto, a ordem visual dos itens será a mesma que a ordem declarada no HTML:
     - Ordem visual: 1, 2, 3, 4.

2. **Segunda Seção (Customizando `order` para os itens 2 e 3)**:
   - Aqui, o **item 2** tem **`order: -1`**, o que faz com que ele apareça antes de todos os outros (antes do item 1).
   - O **item 3** tem **`order: 1`**, o que o faz aparecer após os itens 1 e 4.
   - Ordem visual: 2, 1, 4, 3.

   ```css
   .order1 div:nth-child(2) {
     order: -1;  /* Move o item 2 para o início */
   }

   .order1 div:nth-child(3) {
     order: 1;  /* Move o item 3 para o final */
   }
   ```

3. **Terceira Seção (Todos os itens com `order` personalizado)**:
   - Cada item tem um valor diferente de `order`, o que afeta a ordem visual:
     - **Item 1** tem **`order: 3`**, então ele será exibido por último.
     - **Item 2** e **item 4** têm **`order: 2`**, então eles aparecerão no meio, mas o **item 2** aparecerá primeiro porque vem antes no HTML.
     - **Item 3** tem **`order: 1`**, então ele aparecerá antes dos itens com `order: 2` ou `order: 3`.
   - Ordem visual: 3, 2, 4, 1.

   ```css
   .order2 div:nth-child(1) {
     order: 3;  /* Move o item 1 para o final */
   }

   .order2 div:nth-child(2) {
     order: 2;  /* Move o item 2 para o meio */
   }

   .order2 div:nth-child(3) {
     order: 1;  /* Move o item 3 para o início */
   }

   .order2 div:nth-child(4) {
     order: 2;  /* Item 4 tem a mesma ordem que o item 2 */
   }
   ```

---

### Uso Comum do `order`:
O `order` é útil quando você precisa alterar a disposição visual dos itens sem mudar a estrutura HTML. Isso pode ser particularmente importante em casos como:
- Reordenar itens em diferentes resoluções de tela (para layouts responsivos).
- Priorizar certos conteúdos visualmente, mas manter a ordem semântica no HTML.

---

### Resumo:
- **`order`** define a ordem visual dos itens flexíveis dentro de um contêiner.
- O valor padrão é **`0`**, e você pode usar valores negativos ou positivos para reordenar os itens.
- Usando **`order`**, você pode manipular a sequência visual sem alterar a ordem do HTML.