# Unidades e Medidas

No CSS3, unidades de medidas são usadas para definir o tamanho de elementos, margens, espaçamentos e outras propriedades que dependem de dimensões. Existem dois tipos principais de unidades: **absolutas** e **relativas**. Vamos explorar cada uma delas com exemplos.

### 1. **Unidades Absolutas**
As unidades absolutas são fixas, ou seja, têm o mesmo valor em todos os dispositivos. Elas são independentes do contexto, o que pode tornar difícil o design responsivo.

- **px (pixels)**: A unidade mais comum, representa um único ponto na tela do dispositivo.
  
  ```css
  h1 {
      font-size: 24px; /* Tamanho da fonte é 24 pixels */
  }
  ```

- **cm (centímetros)** e **mm (milímetros)**: Definem tamanhos físicos precisos, mas são raramente usadas em web design, já que o tamanho físico depende da tela e da resolução do dispositivo.

  ```css
  div {
      width: 10cm; /* Largura do div é 10 centímetros */
      height: 50mm; /* Altura do div é 50 milímetros */
  }
  ```

- **pt (pontos)**: Um ponto é 1/72 de polegada. Essa unidade é mais usada em documentos impressos.

  ```css
  p {
      font-size: 12pt; /* Tamanho da fonte é 12 pontos */
  }
  ```

- **in (polegadas)**: Define o tamanho baseado em polegadas (1 polegada = 2.54 cm).
  
  ```css
  img {
      width: 2in; /* A imagem terá uma largura de 2 polegadas */
  }
  ```

### 2. **Unidades Relativas**
As unidades relativas são mais flexíveis e geralmente usadas para criar layouts responsivos. Elas dependem do contexto e do elemento pai ou do tamanho da janela.

- **% (porcentagem)**: Define o tamanho relativo ao elemento pai.

  ```css
  div {
      width: 50%; /* A largura do div será 50% da largura do elemento pai */
  }
  ```

- **em**: Define o tamanho em relação ao tamanho da fonte do elemento pai. Se o pai tiver uma fonte de 16px, `1em` será igual a 16px.

  ```css
  p {
      font-size: 1.5em; /* Tamanho da fonte é 1.5 vezes o tamanho da fonte do pai */
  }
  ```

- **rem (root em)**: Semelhante ao `em`, mas o valor é baseado no tamanho da fonte do elemento raiz (`<html>`), em vez do elemento pai.

  ```css
  body {
      font-size: 16px; /* Define a fonte raiz como 16px */
  }
  h2 {
      font-size: 2rem; /* O tamanho da fonte será 2 vezes a fonte raiz, ou seja, 32px */
  }
  ```

- **vw (viewport width)** e **vh (viewport height)**: `vw` é baseado na largura da janela de visualização (viewport), onde `1vw` é igual a 1% da largura da tela, e `vh` é baseado na altura da janela.

  ```css
  section {
      width: 80vw; /* A largura da seção será 80% da largura da tela */
      height: 50vh; /* A altura da seção será 50% da altura da tela */
  }
  ```

- **vmin** e **vmax**: `vmin` é o menor valor entre `vw` e `vh`, enquanto `vmax` é o maior valor.

  ```css
  div {
      width: 50vmin; /* Largura será 50% da menor dimensão entre altura e largura da tela */
  }
  ```

---