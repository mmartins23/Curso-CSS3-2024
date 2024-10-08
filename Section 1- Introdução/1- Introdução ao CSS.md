CSS3 (Cascading Style Sheets, Level 3) é a mais recente evolução das folhas de estilo em cascata, usada para estilizar páginas da web. Com CSS3, os desenvolvedores têm maior controle sobre o layout e o design de páginas, além de novas funcionalidades que facilitam a criação de efeitos visuais sofisticados, sem depender de gráficos ou JavaScript.

Aqui estão alguns dos principais recursos do CSS3:

### 1. **Novos Seletores**
   CSS3 introduziu novos seletores que facilitam a seleção de elementos específicos no HTML, como:
   - `nth-child()`: Seleciona o enésimo filho de um elemento.
   - `:not()`: Seleciona todos os elementos que **não** correspondem a um determinado seletor.

### 2. **Modelo de Caixa Flexível (Flexbox)**
   O Flexbox torna mais fácil alinhar e distribuir espaço entre os itens de um contêiner, especialmente quando o tamanho é desconhecido ou dinâmico.

### 3. **Grid Layout**
   O CSS Grid é uma abordagem poderosa e fácil para criar layouts de duas dimensões (linhas e colunas) de forma flexível.

### 4. **Media Queries**
   Media Queries permitem a criação de designs responsivos, que se adaptam a diferentes tamanhos de tela, como para dispositivos móveis e desktops.
   ```css
   @media screen and (max-width: 768px) {
       /* Estilos para telas menores */
   }
   ```

### 5. **Animações e Transições**
   CSS3 permite a criação de animações sem o uso de JavaScript. Propriedades como `transition` e `animation` permitem criar efeitos visuais como mudanças suaves de cor, movimento, e transformações de elementos.
   ```css
   .box {
       transition: background-color 0.5s ease;
   }

   .box:hover {
       background-color: #e43c5c;
   }
   ```

### 6. **Cantos Arredondados e Sombras**
   - `border-radius`: Para criar cantos arredondados.
   - `box-shadow`: Para adicionar sombras às caixas.
   ```css
   .button {
       border-radius: 10px;
       box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
   }
   ```

### 7. **Transformações 2D e 3D**
   Com CSS3, você pode aplicar transformações 2D e 3D a elementos como rotação, escalonamento e translação.
   ```css
   .rotate {
       transform: rotate(45deg);
   }
   ```

### 8. **Novas Unidades**
   Além de unidades tradicionais como `px`, CSS3 introduziu unidades relativas como `rem` e `vh`/`vw`, que ajudam a criar designs mais flexíveis e responsivos.

Esses são alguns dos aspectos mais importantes do CSS3, que tornaram o design de websites mais eficiente, moderno e visualmente atraente.