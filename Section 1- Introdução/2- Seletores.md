# Seletores

Seletores em CSS são usados para definir quais elementos HTML serão estilizados. No CSS3, foram introduzidos novos seletores que tornam o processo mais poderoso e flexível. Aqui estão os principais tipos de seletores com exemplos:


### 1. **Seletor de ID**
   O seletor de ID é utilizado para estilizar um elemento HTML específico que possui um atributo `id`. No código, o ID `#header` está sendo usado para estilizar o elemento `<h1>`.
   ```css
   #header {
       font-size: 32px;
       color: darkblue;
       text-align: center;
   }
   ```
   Isso altera o tamanho da fonte para 32px, a cor do texto para azul escuro e alinha o título centralmente.

### 2. **Seletor de Classe**
   O seletor de classe é usado para aplicar estilos a todos os elementos que possuem uma classe específica. No código, a classe `.intro` estiliza um parágrafo específico.
   ```css
   .intro {
       font-size: 18px;
       font-style: italic;
   }
   ```
   Aqui, o parágrafo com a classe `intro` terá uma fonte de 18px e será exibido em itálico.

### 3. **Seletor de Tipo**
   O seletor de tipo (ou seletor de elemento) aplica estilos a todos os elementos de um determinado tipo. Neste caso, todos os parágrafos `<p>` são afetados.
   ```css
   p {
       color: darkgray;
   }
   ```
   Isso faz com que todos os textos dos parágrafos sejam exibidos na cor cinza escuro.

### 4. **Seletor de Atributo**
   O seletor de atributo aplica estilos aos elementos que possuem um determinado atributo ou valor de atributo. No exemplo, ele afeta links (`<a>`) que têm o atributo `target="_blank"`.
   ```css
   a[target="_blank"] {
       color: red;
       text-decoration: none;
   }
   ```
   Isso faz com que todos os links que abrem em uma nova aba fiquem vermelhos e sem sublinhado.

### 5. **Pseudo-classe `:hover`**
   A pseudo-classe `:hover` é usada para aplicar estilos quando o usuário passa o cursor sobre um elemento. No exemplo, afeta o botão.
   ```css
   button:hover {
       background-color: #e43c5c;
       color: white;
       cursor: pointer;
   }
   ```
   Quando o botão é "hovered", a cor de fundo muda para vermelho e a cor do texto para branco, além de mudar o cursor para "pointer".

### 6. **Pseudo-classe `:nth-child()`**
   A pseudo-classe `:nth-child()` seleciona o enésimo filho de um elemento pai. No exemplo, o segundo item da lista `<li>` é estilizado.
   ```css
   li:nth-child(2) {
       font-weight: bold;
       color: green;
   }
   ```
   Isso faz com que o segundo item da lista seja exibido em negrito e com cor verde.

### 7. **Pseudo-elemento `::before`**
   O pseudo-elemento `::before` insere conteúdo antes de um elemento. Aqui, é usado para adicionar uma estrela antes do texto do título `<h1>`.
   ```css
   h1::before {
       content: "⭐ ";
   }
   ```
   Isso faz com que uma estrela apareça antes do texto "Título Principal".

### 8. **Seletor Descendente**
   O seletor descendente estiliza elementos que são filhos de um determinado elemento pai. No exemplo, todos os parágrafos dentro de um `div` são estilizados.
   ```css
   div p {
       color: black;
       font-size: 16px;
   }
   ```
   Todos os parágrafos dentro de um `div` terão a cor preta e a fonte de 16px.

### 9. **Seletor de Negação (`:not()`)**
   O seletor de negação exclui elementos específicos de uma regra. No exemplo, todos os parágrafos que **não** têm a classe `.intro` são estilizados.
   ```css
   p:not(.intro) {
       font-size: 14px;
   }
   ```
   Todos os parágrafos que não são parte da classe `intro` terão o tamanho da fonte definido como 14px.

### 10. **Seletor de Classe + Pseudo-classe**
   O exemplo combina uma classe (`.highlight`) com a pseudo-classe `:hover`. Quando o parágrafo com a classe `highlight` é "hovered", ele muda o fundo.
   ```css
   .highlight:hover {
       background-color: yellow;
   }
   ```
   Quando o parágrafo com a classe `highlight` é "hovered", o fundo dele muda para amarelo.

### Resumo do Funcionamento:
- O código CSS define diferentes seletores que controlam o estilo dos elementos HTML, como parágrafos, botões e links, dependendo de suas classes, IDs, estados (`hover`) ou posições específicas (`nth-child()`).
- Isso permite que o desenvolvedor tenha um controle refinado sobre o design da página, aplicando estilos a elementos específicos ou com base em comportamentos dinâmicos, como a interação do usuário com o botão ou link.