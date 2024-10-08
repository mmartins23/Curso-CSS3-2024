A propriedade `border-spacing` no CSS3 é utilizada para definir o **espaçamento entre as células de uma tabela** quando a propriedade `border-collapse` está configurada como `separate`. Ou seja, ela controla a distância entre as bordas adjacentes das células da tabela.

### Sintaxe:

```css
table {
  border-spacing: valor-horizontal valor-vertical;
}
```

- **Um valor**: Define tanto o espaçamento horizontal quanto o vertical.
- **Dois valores**: O primeiro valor define o espaçamento horizontal (entre as colunas) e o segundo define o espaçamento vertical (entre as linhas).

### Ponto Importante:
- **Funciona apenas** quando a propriedade `border-collapse` está definida como `separate` (que é o comportamento padrão). Se `border-collapse` estiver como `collapse`, o `border-spacing` não terá efeito.

---

### Exemplo Básico de `border-spacing`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Spacing</title>
  <style>
    table {
      border-collapse: separate; /* As bordas estão separadas */
      border-spacing: 20px; /* Espaçamento de 20px em ambos os eixos */
      border: 2px solid black; /* Borda ao redor da tabela */
    }

    th, td {
      border: 2px solid blue; /* Borda ao redor das células */
      padding: 10px;
    }
  </style>
</head>
<body>

  <h2>Tabela com `border-spacing: 20px`</h2>
  <table>
    <tr>
      <th>Coluna 1</th>
      <th>Coluna 2</th>
    </tr>
    <tr>
      <td>Celula 1</td>
      <td>Celula 2</td>
    </tr>
    <tr>
      <td>Celula 3</td>
      <td>Celula 4</td>
    </tr>
  </table>

</body>
</html>
```

### Explicação:
- Neste exemplo, a tabela tem um espaçamento de **20px** entre as células, tanto no eixo horizontal quanto no eixo vertical.
- As bordas de cada célula estão separadas e a tabela é exibida com **espaços visíveis** entre as células.

---

### Usando Dois Valores em `border-spacing`

Você também pode definir valores diferentes para os eixos horizontal e vertical, como mostrado a seguir.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Spacing com Dois Valores</title>
  <style>
    table {
      border-collapse: separate;
      border-spacing: 30px 10px; /* 30px horizontal, 10px vertical */
      border: 2px solid black;
    }

    th, td {
      border: 2px solid blue;
      padding: 10px;
    }
  </style>
</head>
<body>

  <h2>Tabela com `border-spacing: 30px 10px`</h2>
  <table>
    <tr>
      <th>Coluna 1</th>
      <th>Coluna 2</th>
    </tr>
    <tr>
      <td>Celula 1</td>
      <td>Celula 2</td>
    </tr>
    <tr>
      <td>Celula 3</td>
      <td>Celula 4</td>
    </tr>
  </table>

</body>
</html>
```

### Explicação:
- O valor **30px** aplica-se ao **espaçamento horizontal** entre as colunas.
- O valor **10px** aplica-se ao **espaçamento vertical** entre as linhas.
- As células têm mais espaço horizontal entre elas do que espaço vertical, criando uma aparência assimétrica.

---

### Combinando `border-spacing` com `border-collapse`

A propriedade `border-spacing` **não terá efeito** se a tabela estiver utilizando a propriedade `border-collapse: collapse`. Isso ocorre porque, quando as bordas estão colapsadas, não há espaçamento entre as células adjacentes.

### Exemplo de `border-collapse: collapse` (sem efeito de `border-spacing`):

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Border-Collapse com Border-Spacing (sem efeito)</title>
  <style>
    table {
      border-collapse: collapse; /* Bordas colapsadas */
      border-spacing: 20px; /* Não terá efeito neste caso */
      border: 2px solid black;
    }

    th, td {
      border: 2px solid blue;
      padding: 10px;
    }
  </style>
</head>
<body>

  <h2>Tabela com `border-collapse: collapse` (sem efeito de `border-spacing`)</h2>
  <table>
    <tr>
      <th>Coluna 1</th>
      <th>Coluna 2</th>
    </tr>
    <tr>
      <td>Celula 1</td>
      <td>Celula 2</td>
    </tr>
    <tr>
      <td>Celula 3</td>
      <td>Celula 4</td>
    </tr>
  </table>

</body>
</html>
```

### Explicação:
- Como o `border-collapse` está configurado para `collapse`, as bordas das células se colapsam, criando uma borda contínua entre elas, e o `border-spacing` não é aplicado.

---

### Resumo:

- **`border-spacing`** é usado para definir o espaçamento entre as células da tabela.
- Funciona apenas com **`border-collapse: separate`** (o valor padrão), onde as bordas de cada célula são separadas.
- Permite definir espaçamento **horizontal** e **vertical** independentes.
- **Não tem efeito** quando as bordas estão colapsadas com `border-collapse: collapse`.

Esses controles permitem criar tabelas com layouts mais espaçados e ajustados, de acordo com as necessidades de apresentação de dados e design visual.