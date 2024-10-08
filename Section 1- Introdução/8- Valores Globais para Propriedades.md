Os **valores globais** em CSS são valores especiais que podem ser aplicados a qualquer propriedade CSS, independentemente de qual seja, e influenciam diretamente o comportamento do elemento ao qual a propriedade é aplicada. Esses valores são usados para reinicializar, herdar ou fazer com que uma propriedade não tenha efeito.

### 1. **`inherit`**
O valor `inherit` força o elemento a herdar o valor da propriedade de seu elemento pai. Esse comportamento pode ser útil quando você quer garantir que um estilo de um determinado elemento seja idêntico ao de seu elemento pai, mesmo que a propriedade não tenha um comportamento de herança por padrão.

#### Exemplo:
```html
<div class="parent">
  Pai (cor: vermelho)
  <div class="child">
    Filho (cor herdada)
  </div>
</div>
```

```css
.parent {
  color: red;
}

.child {
  color: inherit; /* O filho herdará a cor do pai */
}
```

Neste exemplo, a cor do texto do elemento filho será vermelha, pois ele herda a cor do elemento pai (`.parent`).

### 2. **`initial`**
O valor `initial` define a propriedade para seu valor inicial padrão, ou seja, o valor que a propriedade teria por padrão se nenhum estilo tivesse sido aplicado a ela.

#### Exemplo:
```html
<div class="example">
  Texto com estilo aplicado
</div>
```

```css
.example {
  color: blue; /* A cor inicialmente será azul */
  color: initial; /* Reseta a cor para o valor inicial (normalmente preto) */
}
```

Neste caso, mesmo que a cor tenha sido definida como azul, o valor `initial` redefine a cor do texto para o valor padrão do navegador, que geralmente é preto.

### 3. **`unset`**
O valor `unset` atua de forma combinada:
- Para propriedades herdáveis (como `color` e `font-size`), o valor `unset` se comporta como `inherit`.
- Para propriedades não herdáveis (como `display` e `width`), ele age como `initial`.

#### Exemplo:
```html
<div class="parent">
  Pai (cor: vermelho)
  <div class="child">
    Filho com estilo redefinido
  </div>
</div>
```

```css
.parent {
  color: red;
  font-size: 20px;
}

.child {
  color: unset; /* Herdará a cor do pai (comportamento de inherit) */
  font-size: unset; /* Herdará o tamanho da fonte do pai */
  display: unset; /* Reseta o display para o valor inicial */
}
```

No exemplo acima, a cor do texto e o tamanho da fonte do filho serão herdados do pai (`.parent`), pois `color` e `font-size` são propriedades herdáveis. No entanto, a propriedade `display` será redefinida para o valor inicial (`block` ou `inline`, dependendo do elemento).

### 4. **`revert`**
O valor `revert` redefine a propriedade para o valor que ela teria com base no estilo aplicado pela folha de estilo do navegador ou pelo autor, ignorando estilos aplicados anteriormente (como os de um arquivo CSS personalizado).

#### Exemplo:
```html
<div class="example">
  Texto com estilo sobrescrito
</div>
```

```css
.example {
  color: green; /* Define a cor como verde */
  color: revert; /* Reverte para o valor de cor padrão do navegador ou da folha de estilo do autor */
}
```

Neste caso, se o navegador tiver definido o valor padrão da cor do texto como preto, o valor `revert` fará com que a cor verde seja ignorada, e o texto voltará a ser preto.

---

## Comparação de Comportamento

| Propriedade    | Valor Original (CSS) | `inherit`      | `initial`    | `unset`            | `revert` |
|----------------|----------------------|----------------|--------------|--------------------|----------|
| `color`        | `black` (padrão)      | Herda do pai   | `black`      | Herda ou `black`    | Depende do estilo padrão |
| `display`      | `block` (para `div`)  | Não é herdado  | `block`      | `block` (para `div`) | Depende do estilo padrão |
| `font-size`    | 16px (padrão)         | Herda do pai   | `16px`       | Herda ou `16px`     | Depende do estilo padrão |

---

### Exemplo de todos os valores globais juntos:

```html
<div class="parent" style="color: red; font-size: 24px;">
  Elemento Pai
  <div class="child" style="color: blue; display: inline;">
    Elemento Filho
    <div class="grandchild" style="color: green; font-size: 12px;">
      Elemento Neto
    </div>
  </div>
</div>
```

```css
.child {
  color: inherit; /* O filho herda a cor do pai (vermelho) */
  font-size: initial; /* O filho tem o tamanho de fonte padrão (geralmente 16px) */
  display: revert; /* O filho usa o valor padrão do navegador (block para div) */
}

.grandchild {
  color: unset; /* O neto herda a cor do filho (vermelho) */
  font-size: unset; /* O neto herda o tamanho de fonte do pai (16px) */
}
```

- O elemento `.child` herda a cor vermelha do pai, redefine o `font-size` para o valor inicial (geralmente 16px) e o `display` é revertido para o valor padrão do navegador (`block`).
- O elemento `.grandchild` herda tanto a cor quanto o tamanho da fonte do elemento pai após o `unset`.

Esses valores globais permitem um controle flexível dos estilos em um projeto, ajudando a herdar, redefinir ou restaurar os estilos de maneira eficiente.