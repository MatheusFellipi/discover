# fonts

Tipográfica transmite mensagem

- negrito
- tamanho
- estilo

- basic Font Properties

  - font-family

    - tipo de font de um elemento
    - lista de fontes e ordem de prioridade
    - incluir `fallback` font

      ```css
      p {
        font-family: "Times new roman", Times, serif;
      }
      ```

      - serif
      - sans

  - font-weight

    - peso da fonte
      ```css
      p {
        font-weight: bold | normal | 100 a 900;
      }
      ```

  - font-styles

    - o estilo da fonte
      ```css
      p {
        font-style: italic;
      }
      ```

  - font-size
    - tamanho da fonte
      ```css
      p {
        font-size: 1rem;
      }
      ```

- Web Font
  - fontes do sistema x fontes da web
  - como usar fontes para web
    - @font-face
    - @import
    - link

# atribuir mais estilo as fontes

- font-variant

  ```css
  p {
    font-variant: small-caps;
  }
  ```

- font-stretch

  - alagamento ou encolhimento da fonte
  - aceita palavra-chaves com: expanded, condensed, normal
  - aceita porcentagens de 50% a 200%

    ```css
    p {
      font-stretch: 50%;
    }
    ```

- letter-spacing

  - Espaço entra caracteres

    ```css
    p {
      letter-spacing: 4px;
    }
    ```

- word-spacing

  - Espaço entra palavras

  ```css
  p {
    word-spacing: 4px;
  }
  ```

- line-height

  - Espaço entre linhas
  - pode ser com unidade ou sem unidade de medidas
  - Comuns: 1.5 ou 2

    ```css
    p {
      line-height: 1.5px;
    }
    ```

- text-transform

  - Transformação do texto

    ```css
    p {
      text-transform: uppercase | capitalize | lowercase | none;
    }
    ```

- text-decoration

  - Aparência decorativa de um texto
  - line: underline | overline | line-though
    - podemos aplicar mais de 1 valor
  - style: wavy | dotted | double | dashed | solid
  - color: `<color>` values

    ```css
    p {
      text-decoration: underline;
    }
    ```

- text-align

  - Alinhamento de texto

  ```css
  p {
    text-align: center | left | right | center | justify;
  }
  ```

- text-shadow

  - Sombra aplicada a um texto
  - permite múltiplos valores

    ```css
    p {
      text-shadow: 1px 1px 1px red, 2px 2px 1px green;
      /*offset-x | offset-y | blur-radius | color*/
    }
    ```

- Shorthand
  - font-style | font-variant | font-weight | font-size | line-height | font-family

````css
   p {
     font: italic normal bold normal 3em/1.5 Helvetica, Arial, sans-serif;
     /* style variant weight stretch size line-height e family*/
   }
   ```
````
