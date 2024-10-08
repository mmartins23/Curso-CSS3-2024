### 1. **`overflow-wrap` no CSS3**

A propriedade `overflow-wrap` no CSS3 controla como o navegador deve tratar palavras que ultrapassam os limites do contêiner. Ela é útil quando uma palavra muito longa, como uma URL ou uma string sem espaços, pode causar transbordo no layout.

#### Sintaxe:
```css
overflow-wrap: normal | break-word;
```

- **`normal`** (padrão): As palavras só quebram quando há espaços. Se uma palavra for longa o suficiente para causar transbordo, ela não será quebrada automaticamente.
- **`break-word`**: Quebra as palavras longas automaticamente, se necessário, para evitar o transbordo.

#### Exemplo:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-wrap</title>
  <style>
    .box {
      width: 150px;
      border: 1px solid black;
      padding: 10px;
      margin-bottom: 20px;
    }

    .normal {
      overflow-wrap: normal;
    }

    .break-word {
      overflow-wrap: break-word;
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-wrap`</h2>

  <h3>Overflow-wrap: normal</h3>
  <div class="box normal">
    Este é um exemplo de uma palavra muitolongaparaquebrarautomaticamente e não será quebrada.
  </div>

  <h3>Overflow-wrap: break-word</h3>
  <div class="box break-word">
    Este é um exemplo de uma palavra muitolongaparaquebrarautomaticamente que será quebrada, evitando transbordo.
  </div>

</body>
</html>
```

### 2. **`overflow-block` no CSS3**

A propriedade `overflow-block` controla o comportamento de transbordo no **eixo bloco** (vertical) de um elemento em diferentes contextos de formatação, como conteúdo paginado ou com scroll.

#### Sintaxe:
```css
overflow-block: visible | hidden | scroll | auto;
```

- **`visible`** (padrão): O conteúdo que excede os limites no eixo bloco é visível.
- **`hidden`**: O conteúdo é cortado no eixo bloco.
- **`scroll`**: Barra de rolagem vertical é sempre visível, independentemente do conteúdo.
- **`auto`**: Barra de rolagem aparece se o conteúdo transbordar verticalmente.

#### Exemplo:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-block</title>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border: 1px solid black;
      margin-bottom: 20px;
    }

    .visible {
      overflow-block: visible;
    }

    .scroll {
      overflow-block: scroll;
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-block`</h2>

  <h3>Overflow-block: visible</h3>
  <div class="box visible">
    Este conteúdo ultrapassa a altura da caixa, mas permanece visível. A barra de rolagem não é exibida.
    <p>Mais texto para transbordar...</p>
  </div>

  <h3>Overflow-block: scroll</h3>
  <div class="box scroll">
    Este conteúdo ultrapassa a altura da caixa, e uma barra de rolagem vertical é exibida.
    <p>Mais texto para transbordar...</p>
  </div>

</body>
</html>
```

### 3. **`overflow-inline` no CSS3**

A propriedade `overflow-inline` controla o comportamento de transbordo no **eixo inline** (horizontal). Assim como o `overflow-block`, pode ser aplicado em contextos como conteúdo paginado ou com scroll.

#### Sintaxe:
```css
overflow-inline: visible | hidden | scroll | auto;
```

- **`visible`** (padrão): O conteúdo que excede os limites no eixo inline (horizontal) é visível.
- **`hidden`**: O conteúdo é cortado no eixo inline.
- **`scroll`**: Barra de rolagem horizontal é sempre visível, independentemente do conteúdo.
- **`auto`**: Barra de rolagem aparece se o conteúdo transbordar horizontalmente.

#### Exemplo:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de overflow-inline</title>
  <style>
    .box {
      width: 200px;
      border: 1px solid black;
      white-space: nowrap;
      margin-bottom: 20px;
    }

    .visible {
      overflow-inline: visible;
    }

    .scroll {
      overflow-inline: scroll;
    }
  </style>
</head>
<body>

  <h2>Exemplo de `overflow-inline`</h2>

  <h3>Overflow-inline: visible</h3>
  <div class="box visible">
    Este é um exemplo de uma linha muito longa que ultrapassa o contêiner e continua visível sem rolagem.
  </div>

  <h3>Overflow-inline: scroll</h3>
  <div class="box scroll">
    Este é um exemplo de uma linha muito longa, e a barra de rolagem horizontal aparece.
  </div>

</body>
</html>
```

### Resumo das Propriedades:

1. **`overflow-wrap`**: Controla a quebra automática de palavras longas que podem causar transbordo.
2. **`overflow-block`**: Controla o comportamento de transbordo no eixo bloco (vertical).
3. **`overflow-inline`**: Controla o comportamento de transbordo no eixo inline (horizontal).

Essas propriedades são essenciais para manter o layout limpo e funcional, mesmo quando o conteúdo excede os limites de seus contêineres.