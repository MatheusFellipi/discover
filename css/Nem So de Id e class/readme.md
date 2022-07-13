# Seletores

- Conectar um elementos HTML com o CSS

* Tipos

  - Element selector
    - todo os elementos HTML (p,h1,span,div ...)
  - ID Selector
    - Um elemento que tenha um atributo `id`
    - ID e único
  - Class Selector
    - Os elementos que contenha um atributo `class`
    - podem ter uma ou mais classes.
  - Attribute Selector

    - Um elemento de que tenha um atributo especifico

      ```css
      [title] {
        color: blue;
      }
      ```

      ```html
      <h1 title="oi">oi</h1>
      ```

  - Pseudo-class selector

    - Elementos em um estado especifico.

      ```css
      p:houve {
        color: blue;
      }
      ```

* Múltiplos

  - voce poderá selecionar múltiplos elementos e aplicar alguma regras css para todos.

  - Usando uma Separação por virgula para isso

    ```css
    p,
    h1,
    a,
    .red {
      color: blue;
    }
    ```

# Combinators

- Combinadores, pois eles trabalah para busca e combinar seletores a fim de aplica um estilização.

- Descendant combinator

  - Identificado por um espaço entre os seletores
  - Busca um elemento dentro de outro

    ```css
    body article h2
    ```

- Child combinator

  - identificado pelo sinal `>` entre dois selectors
  - selecionar somente o elemento que e filhos direto do pai
  - Elementos depois do filho direto

    ```css
      body > article > h2
    ```

- Adjacent sibling combinator

  - Identificado pelo sinal `+` entre dois seletores
  - Selecionar somente o elemento do lado direto que e irmão direito na hierarquia.

    ```css
      h1 + p
    ```

- General sibling combinator

  - Identificado pelo sinal `~` entre dois seletores.
  - Selecionar todos os elementos irmão.

    ```css
      h1 ~ p
    ```

- utilizando combinadores

  ```css
    ul> li[class="red"]
  ```

### Dicas

- Seletores muito especifico tende a causa dificuldade no recurso das regras de estilização dos elementos
- Muitas vezes, um simples uso de class, toma o trabalho muito mais eficiente

# Pseudo-Classes

e um tipo de seletor que irar selecionar um elemento que estiver em estado especifico

exemplo: E o primeiro elemento dentro de uma caixa, ou , o elemento esta com o ponteiro do mouse em cima dele

Pseudo-classes começa com 2 pontos seguindo da pseudo class
`:pseudo-clas-name`

```html
<ul>
  <li>item 1</li>
  <li>item 2</li>
</ul>
```

- selecionado elementos com pseudo-classe

  - :fist-child

    ```css
    ul li:fist-child {
      color: red; /* aplica a regra de estilo no primeiro filho do ul */
    }
    ```

  - :nth-of-type()

    ```css
    ul li:nth-of-type(1) {
      color: red; /* pega os tipo de li que tem no ul*/
    }
    ```

  - :nth-child()

    ```css
    ul li::nth-child() {
      color: red; /* conta os filho do ul*/
    }
    ```

* dicas

  ```html
  <ul>
    <li>item 1</li>
    <li>item 2</li>
    <li>item 3</li>
    <li>item 4</li>
  </ul>
  ```

  ```css
  ul li::nth-child(even) {
    color: red; /* item sim e item nao par*/
  }
  ul li::nth-child(odl) {
    color: blue; /* item sim e item nao impar*/
  }
  ```

- ações do usuário

  - `:houve`

    ```css
    a:houve {
      color: red;
    }
    ```

  - `:focus`

    ```css
    input:focus {
      color: red;
    }
    ```

- Atributos

  - disabled

    ```css
    input:disabled {
      color: red;
    }
    ```

  - required

    ```css
    input:required {
      color: red;
    }
    ```

- Pseudo-Elements

com pseudo-elements nos podemos adicionar elemento html pelo css
`::pseudo-element-name`

- Exemplos

  - ::before
  - ::after
  - ::first-line
