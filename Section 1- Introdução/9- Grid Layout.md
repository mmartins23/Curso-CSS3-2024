O **CSS Grid Layout** é um sistema de layout em duas dimensões (linhas e colunas) que facilita a criação de layouts complexos de forma simples e intuitiva. Com o Grid, é possível definir a estrutura de um layout sem precisar usar `float`, `position`, ou `flexbox` para alinhar elementos.

## Conceitos Básicos do Grid Layout

- **Grid Container**: O elemento pai que define um grid e contém os itens de grid.
- **Grid Items**: Os elementos filhos do grid container, organizados em linhas e colunas.

### Propriedades do Grid Container

1. **`display: grid;`**  
   Ativa o comportamento de grid no container.

2. **`grid-template-columns` e `grid-template-rows`**  
   Define a quantidade e o tamanho das colunas e linhas no grid:
   - Exemplo: `grid-template-columns: 1fr 1fr 1fr;` cria três colunas com larguras iguais.

3. **`gap`**  
   Define o espaço (espaçamento) entre as linhas e colunas. Pode ser usado como:
   - `gap: 10px;` (define o espaçamento entre todas as linhas e colunas).
   - `row-gap` e `column-gap` podem ser usados separadamente para espaçamento específico.

4. **`grid-template-areas`**  
   Permite nomear áreas do grid para facilitar o posicionamento dos itens.

5. **`justify-items` e `align-items`**  
   Controlam o alinhamento dos itens no grid, respectivamente, horizontalmente e verticalmente.

### Propriedades dos Itens do Grid

1. **`grid-column` e `grid-row`**  
   Definem a posição e a extensão dos itens nas colunas e linhas.  
   - Exemplo: `grid-column: 1 / 3;` significa que o item começa na coluna 1 e termina antes da coluna 3 (abrange 2 colunas).

2. **`grid-area`**  
   Associa o item a uma área nomeada definida por `grid-template-areas`.

---

## Exemplo Simples de Grid Layout

### HTML

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Grid Layout</title>
  <style>
    /* Definindo o container como grid */
    .grid-container {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr; /* 3 colunas, sendo a do meio duas vezes maior */
      grid-template-rows: auto 200px auto; /* 3 linhas, sendo a do meio com 200px */
      gap: 10px; /* Espaçamento entre as células do grid */
      background-color: lightgray;
      padding: 10px;
    }

    /* Estilizando os itens do grid */
    .grid-item {
      background-color: #4CAF50;
      color: white;
      padding: 20px;
      text-align: center;
      font-size: 30px;
    }

    /* Estendendo o item 1 por 2 colunas */
    .item1 {
      grid-column: 1 / 3; /* O item 1 ocupa da coluna 1 até a coluna 3 (duas colunas) */
    }

    /* Definindo o item 3 para ocupar 2 linhas */
    .item3 {
      grid-row: 1 / 3; /* O item 3 ocupa duas linhas */
    }
  </style>
</head>
<body>

  <div class="grid-container">
    <div class="grid-item item1">Item 1</div>
    <div class="grid-item item2">Item 2</div>
    <div class="grid-item item3">Item 3</div>
    <div class="grid-item item4">Item 4</div>
    <div class="grid-item item5">Item 5</div>
    <div class="grid-item item6">Item 6</div>
  </div>

</body>
</html>
```

### Explicação do Código

- **`.grid-container`**: O container é definido como grid com três colunas e três linhas. A segunda coluna é o dobro do tamanho das outras, e a segunda linha tem uma altura fixa de 200px.
  
- **`.item1`**: O item 1 se estende por duas colunas (da 1ª à 3ª coluna).
  
- **`.item3`**: O item 3 ocupa duas linhas (da 1ª à 3ª linha).

### Resultado esperado:
Os itens serão dispostos em uma grade com a seguinte organização:

```
+----------------+----------------+----------------+
|     Item 1     |     Item 2      |     Item 3     |
|                |                 |                |
+----------------+----------------+----------------+
|     Item 4     |     Item 5      |                |
+----------------+----------------+     Item 6     |
|     Item 6     |                 |                |
+----------------+----------------+----------------+
```

---

## Exemplo Avançado com `grid-template-areas`

O `grid-template-areas` é útil para nomear as áreas de um grid e posicionar itens de forma semântica.

### HTML

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo Avançado de Grid</title>
  <style>
    /* Definindo o container como grid com áreas nomeadas */
    .grid-container {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      grid-template-rows: 100px 200px auto;
      grid-template-areas:
        "header header header"
        "menu main sidebar"
        "footer footer footer";
      gap: 10px;
      background-color: #ddd;
      padding: 10px;
    }

    /* Estilizando as áreas nomeadas */
    .header {
      grid-area: header;
      background-color: #4CAF50;
      color: white;
      text-align: center;
      padding: 20px;
    }

    .menu {
      grid-area: menu;
      background-color: #2196F3;
      color: white;
      padding: 20px;
    }

    .main {
      grid-area: main;
      background-color: #f44336;
      color: white;
      padding: 20px;
    }

    .sidebar {
      grid-area: sidebar;
      background-color: #FFC107;
      color: white;
      padding: 20px;
    }

    .footer {
      grid-area: footer;
      background-color: #9C27B0;
      color: white;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>

  <div class="grid-container">
    <div class="header">Cabeçalho</div>
    <div class="menu">Menu</div>
    <div class="main">Conteúdo Principal</div>
    <div class="sidebar">Barra Lateral</div>
    <div class="footer">Rodapé</div>
  </div>

</body>
</html>
```

### Explicação do Código

- **`.grid-template-areas`**: Este código cria um layout nomeado com `header`, `menu`, `main`, `sidebar`, e `footer`. A primeira linha é o cabeçalho que ocupa as três colunas. A segunda linha contém o menu à esquerda, o conteúdo principal no centro e a barra lateral à direita. A última linha é o rodapé, que também ocupa as três colunas.

### Resultado esperado:

```
+------------------+------------------+------------------+
|    Cabeçalho     |    Cabeçalho      |    Cabeçalho     |
+------------------+------------------+------------------+
|      Menu        | Conteúdo Principal|    Barra Lateral |
+------------------+------------------+------------------+
|      Rodapé      |      Rodapé       |      Rodapé      |
+------------------+------------------+------------------+
```

---

## Propriedades Úteis no Grid Layout

- **`fr` (fractional unit)**: Representa uma fração do espaço disponível no grid. Exemplo: `1fr` significa "uma fração" do espaço disponível, e `2fr` significa "duas frações".
  
- **`repeat()`**: Simplifica a criação de colunas/linhas repetitivas. Exemplo: `grid-template-columns: repeat(3, 1fr);` cria três colunas iguais.

- **`auto`**: O valor `auto` ajusta automaticamente o tamanho de uma linha ou coluna com base no conteúdo.

---

O **CSS Grid Layout** é uma ferramenta poderosa para construir layouts flexíveis e responsivos. Ele permite organizar o conteúdo em uma grade que pode ser facilmente manipulada, facilitando a criação de layouts modernos e acessíveis.