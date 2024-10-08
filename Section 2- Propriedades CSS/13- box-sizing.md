A propriedade `box-sizing` no CSS3 é usada para alterar a forma como o navegador calcula a largura e a altura de um elemento. Ela controla se a largura e a altura de um elemento devem incluir o **padding** e as **bordas** ou não. Dependendo do valor que você usar, o comportamento do dimensionamento do elemento será diferente.

### Valores de `box-sizing`:

1. **`content-box`** (valor padrão): A largura e altura aplicadas ao elemento consideram apenas o **conteúdo**. O **padding** e a **borda** são adicionados à largura e altura definidas, o que aumenta o tamanho total do elemento.
   
2. **`border-box`**: A largura e a altura incluem o **conteúdo**, o **padding** e a **borda**. Isso significa que o tamanho total do elemento permanece o mesmo, e o conteúdo será reduzido para acomodar o **padding** e a **borda** dentro das dimensões definidas.

---

### 1. **`box-sizing: content-box`** (Padrão)

Com o valor padrão `content-box`, a largura e altura que você define em um elemento não incluem o **padding** e as **bordas**. Ou seja, esses elementos são **adicionados** à largura e à altura.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Sizing - content-box</title>
  <style>
    .content-box {
      width: 300px; /* Define a largura apenas para o conteúdo */
      height: 150px; /* Define a altura apenas para o conteúdo */
      padding: 20px; /* Adiciona padding */
      border: 10px solid red; /* Adiciona borda */
      background-color: lightblue;
      box-sizing: content-box; /* Valor padrão */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `box-sizing: content-box` (valor padrão)</h2>
  <div class="content-box">
    Esta caixa tem 300px de largura de conteúdo, mas a largura total será maior.
  </div>

</body>
</html>
```

### Explicação:
- **Largura total do elemento**: Largura total = `width` (300px) + `padding` (40px = 20px de cada lado) + `border` (20px = 10px de cada lado) = **360px**.
- **Altura total do elemento**: Altura total = `height` (150px) + `padding` (40px = 20px de cada lado) + `border` (20px = 10px de cada lado) = **210px**.

---

### 2. **`box-sizing: border-box`**

Com `border-box`, o navegador calcula a largura e a altura de forma que **inclua o conteúdo, o padding e as bordas**. Isso significa que a largura e a altura aplicadas ao elemento são o **tamanho total**, sem precisar somar as bordas e o padding.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Sizing - border-box</title>
  <style>
    .border-box {
      width: 300px; /* A largura total do elemento será 300px */
      height: 150px; /* A altura total do elemento será 150px */
      padding: 20px; /* O padding é incluído dentro da largura e altura */
      border: 10px solid red; /* A borda também é incluída */
      background-color: lightgreen;
      box-sizing: border-box; /* Valor border-box */
    }
  </style>
</head>
<body>

  <h2>Exemplo de `box-sizing: border-box`</h2>
  <div class="border-box">
    Esta caixa tem 300px de largura total, incluindo o padding e a borda.
  </div>

</body>
</html>
```

### Explicação:
- **Largura total do elemento**: A largura definida (300px) já inclui o **conteúdo**, o **padding** e a **borda**.
- **Altura total do elemento**: A altura definida (150px) já inclui o **conteúdo**, o **padding** e a **borda**.

Neste exemplo, mesmo com padding e borda, a largura e altura do elemento permanecem **300px** e **150px**, respectivamente, pois o `box-sizing: border-box` ajusta o tamanho interno para que tudo caiba dentro dessas dimensões.

---

### Comparação entre `content-box` e `border-box`:

| Propriedade      | `content-box` (padrão)                               | `border-box`                                    |
|------------------|------------------------------------------------------|-------------------------------------------------|
| Largura definida | Afeta apenas o conteúdo                              | Inclui o conteúdo, padding e borda              |
| Altura definida  | Afeta apenas o conteúdo                              | Inclui o conteúdo, padding e borda              |
| Tamanho total    | Largura + padding + borda                            | Exatamente a largura e altura definidas         |
| Uso comum        | Padrão, mas pode ser problemático ao calcular layouts | Mais previsível para layouts complexos          |

---

### Aplicando `box-sizing: border-box` a todos os elementos:

É comum usar `box-sizing: border-box` globalmente em projetos web para simplificar o cálculo de largura e altura, especialmente quando se trabalha com layouts responsivos.

#### Exemplo de uso global:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box-Sizing Global</title>
  <style>
    /* Aplica box-sizing: border-box a todos os elementos */
    * {
      box-sizing: border-box;
    }

    .caixa {
      width: 200px;
      height: 100px;
      padding: 20px;
      border: 10px solid blue;
      background-color: lightcoral;
    }
  </style>
</head>
<body>

  <h2>Exemplo de `box-sizing: border-box` aplicado globalmente</h2>
  <div class="caixa">
    Esta caixa tem largura e altura totais de 200px por 100px, incluindo padding e bordas.
  </div>

</body>
</html>
```

### Explicação:
- Neste exemplo, o seletor universal `*` aplica o `box-sizing: border-box` a **todos os elementos**, garantindo que o cálculo de largura e altura inclua o padding e as bordas. Isso torna o layout mais previsível.

---

### Resumo:

- **`box-sizing: content-box`** (padrão) faz com que a largura e altura definidas sejam aplicadas apenas ao conteúdo, adicionando bordas e padding ao valor final.
- **`box-sizing: border-box`** inclui o conteúdo, o padding e as bordas dentro da largura e altura definidas, facilitando o controle de layout.
- **Uso global de `border-box`** é uma prática comum para garantir que o layout de elementos seja previsível e fácil de controlar, especialmente em designs responsivos.

Essa propriedade é especialmente útil ao trabalhar com layouts modernos, como Flexbox e Grid, onde o controle preciso das dimensões de elementos é importante.