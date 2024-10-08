A propriedade `border-collapse` no CSS3 é usada para controlar o comportamento das bordas das tabelas em HTML. Ela define se as bordas das células de uma tabela devem ser separadas ou colapsadas em uma única borda.

Existem dois valores principais para essa propriedade:

### 1. **`separate`** (padrão): 
As bordas de cada célula da tabela serão separadas, ou seja, cada célula terá sua própria borda individual.

### 2. **`collapse`**: 
As bordas de células adjacentes da tabela se **colapsam** (se fundem) em uma única borda compartilhada. Quando essa opção é usada, apenas uma borda será exibida entre as células adjacentes.

---

### Sintaxe:

```css
table {
  border-collapse: collapse | separate;
}
```

---

### **Exemplo Prático com `border-collapse`**

Aqui está um exemplo mostrando a diferença entre os dois valores de `border-collapse`.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Border-Collapse</title>
  <style>
    table {
      width: 50%;
      margin-bottom: 20px;
    }

    th, td {
      padding: 10px;
      text-align: center;
      border: 2px solid black;
    }

    /* Estilo para a tabela com bordas separadas */
    .separate-table {
      border-collapse: separate;
      border-spacing: 10px; /* Define o espaçamento entre as células no modo 'separate' */
    }

    /* Estilo para a tabela com bordas colapsadas */
    .collapse-table {
      border-collapse: collapse;
    }
  </style>
</head>
<body>

  <h2>Tabela com `border-collapse: separate`</h2>
  <table class="separate-table">
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

  <h2>Tabela com `border-collapse: collapse`</h2>
  <table class="collapse-table">
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

---

### **Explicação do Exemplo:**

1. **Tabela com `border-collapse: separate`**:
   - As bordas de cada célula estão **separadas**, e há um espaçamento entre elas, que pode ser controlado pela propriedade `border-spacing`.
   - No exemplo, foi aplicado `border-spacing: 10px`, o que adiciona 10px de espaço entre as bordas de cada célula.

2. **Tabela com `border-collapse: collapse`**:
   - As bordas das células adjacentes estão **colapsadas** em uma única borda compartilhada. O resultado é uma tabela mais compacta, com bordas contínuas entre as células.
   - O espaçamento entre células não pode ser ajustado quando as bordas estão colapsadas.

---

### Uso de `border-spacing` com `border-collapse: separate`

Quando o valor `separate` é utilizado, você pode usar a propriedade `border-spacing` para definir o **espaçamento entre as células**.

#### Exemplo:

```css
table {
  border-collapse: separate;
  border-spacing: 15px; /* Espaçamento entre as células */
}
```

Isso permite criar tabelas onde as bordas das células são separadas por uma determinada distância.

---

### Observações Adicionais:

- **Bordas colapsadas** (`collapse`) podem criar resultados mais limpos e compactos em tabelas, pois as bordas adjacentes de células e cabeçalhos são fundidas em uma só.
- **Bordas separadas** (`separate`) são úteis quando você quer um controle preciso sobre o **espaçamento** entre as células da tabela, por exemplo, para criar uma tabela com espaços visíveis entre as células.

---

### Resumo:

- **`border-collapse: separate`**: As bordas das células são separadas e podem ter espaçamento entre elas.
- **`border-collapse: collapse`**: As bordas das células são colapsadas em uma única borda contínua.
- Usar `border-collapse` adequadamente ajuda a controlar a aparência de tabelas e como suas bordas são exibidas em diferentes layouts.