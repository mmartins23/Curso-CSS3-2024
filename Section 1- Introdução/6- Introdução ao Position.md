# Introdução ao Position

No CSS, a propriedade **`position`** controla o método de posicionamento de um elemento na página. Ela determina como um elemento será inserido no fluxo do layout e sua relação com outros elementos.

Existem cinco valores principais para a propriedade `position`:

### 1. **`static`** (Padrão)
O valor padrão da propriedade `position`. O elemento é posicionado de acordo com o fluxo normal da página, sem alterações no layout. Ele ignora as propriedades de posicionamento como `top`, `left`, `right`, e `bottom`.

```css
div {
    position: static; /* Padrão, sem posicionamento especial */
}
```

### 2. **`relative`** (Relativo)
O elemento é posicionado de forma **relativa** à sua posição original no layout normal da página. Você pode ajustar sua posição usando `top`, `left`, `right` e `bottom`, mas o espaço original do elemento ainda será reservado no layout.

```css
div {
    position: relative;
    top: 10px; /* Move o elemento 10px para baixo */
    left: 20px; /* Move o elemento 20px para a direita */
}
```

> **Nota:** O elemento "muda" da sua posição original, mas o espaço original ainda é preservado, o que pode causar uma sobreposição visual.

### 3. **`absolute`** (Absoluto)
O elemento é posicionado de forma **absoluta** em relação ao seu parente mais próximo com `position: relative`, `absolute`, ou `fixed`. Caso não exista um elemento pai com essa propriedade, o elemento será posicionado em relação ao `<html>` (ou body). O elemento é retirado do fluxo normal da página, portanto, não ocupa mais espaço no layout.

```css
div {
    position: absolute;
    top: 50px; /* Posiciona 50px a partir do topo do elemento pai */
    right: 20px; /* Posiciona 20px a partir da direita do elemento pai */
}
```

> **Nota:** O uso de `absolute` remove o elemento do fluxo da página, podendo causar sobreposição com outros elementos.

### 4. **`fixed`** (Fixo)
O elemento é posicionado em relação à **janela de visualização** (viewport), ou seja, permanece fixo em um ponto da tela mesmo quando o usuário rola a página. Assim como `absolute`, ele é retirado do fluxo normal do documento.

```css
div {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: lightblue;
}
```

> **Uso comum:** Usado para criar cabeçalhos ou rodapés fixos que permanecem visíveis enquanto o usuário rola a página.

### 5. **`sticky`** (Adesivo)
O elemento alterna entre `relative` e `fixed`, dependendo da rolagem da página. Ele se comporta como `relative` até atingir um determinado ponto (definido com `top`, `left`, `right`, ou `bottom`), e a partir daí passa a se comportar como `fixed`, mantendo-se fixo enquanto o usuário rola a página.

```css
div {
    position: sticky;
    top: 0; /* O elemento ficará fixo no topo quando chegar a essa posição */
    background-color: yellow;
}
```

> **Uso comum:** Criação de elementos "pegajosos", como um cabeçalho que se fixa ao topo da tela quando rolado até ele.

---

### Exemplo Completo de Código

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Position no CSS</title>
    <style>
        /* Posição estática (padrão) */
        .static {
            position: static;
            background-color: lightgray;
            padding: 10px;
        }

        /* Posição relativa */
        .relative {
            position: relative;
            top: 20px; /* Move 20px para baixo da sua posição original */
            left: 30px; /* Move 30px para a direita da sua posição original */
            background-color: lightcoral;
            padding: 10px;
        }

        /* Posição absoluta */
        .absolute {
            position: absolute;
            top: 100px; /* Posiciona 100px a partir do topo do seu parente mais próximo */
            left: 50px; /* Posiciona 50px a partir da esquerda */
            background-color: lightgreen;
            padding: 10px;
        }

        /* Posição fixa */
        .fixed {
            position: fixed;
            bottom: 10px; /* Fixa 10px a partir da parte inferior da janela */
            right: 10px; /* Fixa 10px a partir da direita da janela */
            background-color: lightblue;
            padding: 10px;
        }

        /* Posição adesiva (sticky) */
        .sticky {
            position: sticky;
            top: 0; /* O elemento fica fixo no topo quando a rolagem chegar a esse ponto */
            background-color: yellow;
            padding: 10px;
        }

        /* Estilo básico para o conteúdo */
        .content {
            height: 1000px; /* Para demonstrar o efeito de rolagem */
        }
    </style>
</head>
<body>

    <h1>Exemplo de Position no CSS</h1>

    <div class="static">
        Este elemento está em posição estática (padrão).
    </div>

    <div class="relative">
        Este elemento está em posição relativa (move-se em relação à sua posição original).
    </div>

    <div class="absolute">
        Este elemento está em posição absoluta (posicionado em relação ao seu elemento pai).
    </div>

    <div class="fixed">
        Este elemento está em posição fixa (sempre visível na parte inferior direita).
    </div>

    <div class="sticky">
        Este elemento está em posição adesiva (fixa-se no topo quando você rola).
    </div>

    <div class="content">
        Role para testar o comportamento do elemento sticky.
    </div>

</body>
</html>
```

### Explicação do Código:

- **Elemento `.static`**: O comportamento padrão, sem ajuste de posicionamento.
- **Elemento `.relative`**: Movido 20px para baixo e 30px para a direita da sua posição original, mas o espaço original é mantido.
- **Elemento `.absolute`**: Posicionado 100px a partir do topo e 50px a partir da esquerda em relação ao seu elemento pai mais próximo.
- **Elemento `.fixed`**: Fica sempre visível, fixado 10px do rodapé e da direita da tela, independentemente da rolagem.
- **Elemento `.sticky`**: O elemento começa como `relative`, mas ao rolar a página e ele atingir o topo, ele "gruda" e se comporta como `fixed`.

### Como Testar

1. Copie o código acima e salve como um arquivo `.html`.
2. Abra-o no navegador e role a página para observar o comportamento dos elementos com diferentes valores de `position`.

---

### Resumo

- **`static`**: Posicionamento padrão, sem ajuste extra.
- **`relative`**: Movimenta o elemento em relação à sua posição original, mas mantém seu espaço reservado.
- **`absolute`**: Posiciona o elemento em relação ao seu parente mais próximo com `position` definido, retirando-o do fluxo normal.
- **`fixed`**: O elemento fica fixo em relação à janela de visualização, permanecendo visível durante a rolagem.
- **`sticky`**: O elemento alterna entre relativo e fixo, fixando-se quando atinge um ponto de rolagem.

Esses diferentes valores de `position` são fundamentais para criar layouts flexíveis e complexos em páginas web.