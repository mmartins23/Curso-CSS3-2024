As propriedades `break-before` e `break-after` em CSS são usadas para controlar as quebras de página e quebras de linha em elementos de bloco, especialmente quando se trabalha com impressão ou layouts que requerem quebras. Essas propriedades são parte das regras de controle de fluxo de layout e ajudam a gerenciar como e onde os elementos devem ser quebrados.

## 1. `break-before`
A propriedade `break-before` controla a quebra de linha ou de página que deve ocorrer antes do elemento.

### Valores comuns:
- **`auto`**: O comportamento padrão (sem quebra forçada).
- **`always`**: Sempre força uma quebra antes do elemento.
- **`avoid`**: Evita a quebra antes do elemento, se possível.
- **`left`**: Força a quebra para que o elemento comece em uma página ou coluna da esquerda (para impressão).
- **`right`**: Força a quebra para que o elemento comece em uma página ou coluna da direita.

## 2. `break-after`
A propriedade `break-after` controla a quebra de linha ou de página que deve ocorrer após o elemento.

### Valores comuns:
- **`auto`**: O comportamento padrão (sem quebra forçada).
- **`always`**: Sempre força uma quebra após o elemento.
- **`avoid`**: Evita a quebra após o elemento, se possível.
- **`left`**: Força a quebra para que o próximo elemento comece em uma página ou coluna da esquerda.
- **`right`**: Força a quebra para que o próximo elemento comece em uma página ou coluna da direita.

### Exemplo Completo

#### HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Break Before and After Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Exemplos de Break Before e Break After</h1>

    <div class="section-break-before">
        <h2>Seção com Break Before</h2>
        <p>Este parágrafo aparece antes da quebra de página.</p>
    </div>

    <div class="break-after">
        <h2>Seção com Break After</h2>
        <p>Este parágrafo força uma quebra após este elemento.</p>
    </div>

    <div class="next-section">
        <h2>Próxima Seção</h2>
        <p>Este parágrafo aparece na próxima seção.</p>
    </div>
</body>
</html>
```

#### CSS (styles.css):
```css
body {
    font-family: Arial, sans-serif;
    margin: 20px;
}

.section-break-before {
    background-color: #f0f0f0;
    padding: 15px;
    margin: 20px 0;
    break-before: always; /* Força quebra antes desta seção */
}

.break-after {
    background-color: #e0e0e0;
    padding: 15px;
    margin: 20px 0;
    break-after: always; /* Força quebra após este elemento */
}

.next-section {
    background-color: #d0d0d0;
    padding: 15px;
    margin: 20px 0;
}
```

### Explicação do Código

1. **HTML**: O HTML consiste em três seções:
   - **`section-break-before`**: Uma seção que contém um título e um parágrafo. A quebra será forçada antes desta seção devido à propriedade `break-before: always`.
   - **`break-after`**: Uma seção que contém um título e um parágrafo. A quebra será forçada após esta seção devido à propriedade `break-after: always`.
   - **`next-section`**: A próxima seção que aparecerá após a quebra forçada.

2. **CSS**: As regras de estilo aplicam um fundo, preenchimento e margem a cada uma das seções para torná-las visualmente distintas. As propriedades `break-before` e `break-after` são usadas nas respectivas seções para controlar onde as quebras devem ocorrer.

### Observações

- As propriedades `break-before` e `break-after` são particularmente úteis quando se lida com impressão, onde você pode querer garantir que certas seções comecem ou terminem em páginas específicas.
- O suporte para essas propriedades pode variar entre navegadores, especialmente em contextos de impressão, portanto, é uma boa prática testar em diferentes navegadores.

---

Esses exemplos demonstram como usar as propriedades `break-before` e `break-after` para controlar a estrutura e o fluxo de layout em HTML e CSS, permitindo um maior controle sobre como as seções se comportam em relação a quebras de página e linha.