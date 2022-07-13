# Css

## valores

- cada propriedade possui valores `property: value`

- estudos constante a fim de entender as propriedade e seus valores

## Pratica

- como conhecer e estudar os valores na documentação
  `<color> <length>`

- os termos podem variar. `values` ou `data types`

* Tipos numéricos

  - `<integer>` Numeto inteiro com -10 ou 223
  - `<number>` Numero decimal como -2.4, 64 ou 0.234
  - `<dimension>` E um `<number>` com uma unidade junto: 90deg, 2s, 8px
  - `<percentagem> ` Representa a fração de outro numero: 50%

* Unidade comuns

  - `<length>` representa um valor:px, em, vw
  - `<angle>` representa um ângulo: deg,rad,turn
  - `<time>` representa um tempo:s,ms
  - `<resolution>` representa um resolucoes para dispositivos: dpi

* Distancia absolutas `<lengtht>`

Sao fixas e nao alteram seu valor.

Unidade nome Equivalência
cm Centímetros 1cm= 96px/2.54
in Inches (polegadas) 1in = 2.54cm = 96px
px Pixels 1px = 1/96th of 1in

- o mais comun e mais utilizado e o `px`
- nao recomendado usar cm

* Distancias relativas

Sao relativas a algum outro valor
tamanho da tela.

- Beneficio: Maior adaptação aos diferente tipos de telas

Unidade Relativo a
em Tamanho da font do pai.
rem Tamanho da font do elemento raiz (root/html).
vw 1% da viewport width.
vh 1% da viewport height.

- Porcentagens

  - em muitas caso e tratado da mesma maneira ques as distancia `<lengtht>`
  - sempre sera relativo a algum valor

- Posições `<posições>`

* Representa um conjuto de coordenadas 2D

  - top, right, bottom, left e center

* usando para alguns tipos de propriedade
* nao confundir com a propriedade `position`

- Funções

* Em programacao, funcoes sao reconhecidas por causa um reaproveitamento de código.

  - rpg()
  - hsl()
  - url()
  - calc()

- Strings e identificadores

* String: texto envolto em aspas
* Identificadores: red, black, gold;

# Uma caixa dentro da outra

- Box model

  - Fundamental para fazer layouts para a web
  - Maior facilidade para aplicar o CSS

- O que é?

Uma caixa retangular.
Essa caixa possui propriedade de um caixa 2D

- tamanho (largura \* altura) width | height
- Conteúdo content
- Bordas border
- Preenchimento interno padding
- Espaço fora da caixa margin

* cada elemento na sua pagina, sera considerado uma caixa

* Box-sizing

Como sera calculado o tamanho total da caixa

- content-box | border-box
  - content-box faz o tamanho baseado no conteúdo
  - border-box a caixa vai der o tamanho que voce desejar

* display: block vs display: inline

- como as caixas se comportam em relacao as outra caixas
- comportamentos externo das caixa

  - Block

    - ocupa toda a linha, colocando o preoximo elemento abaixo desse
    - width e height sao respeitados
    - pandding, margin, border, irão funcionar normalmente

  - inline
    - elemento ao lado da outra
    - width e height nao funciona
    - somente valores horizontes de margin pandding e border

* margin

Espacos entre os elementos

- margin-top | margin-right | margin-bottom | margin-left
- value `<length>` | `<percentage>` | auto

```css
div {
  /* shorthand */
  /* margin: top right bottom left;*/
  margin: 12px 19px 10px 4px;
  /* margin: top right/left bottom ;*/
  margin: 12px 19px 0;
  /* margin: top/bottom right/left  ;*/
  margin: 12px 19px;
  /* margin: all ;*/
  margin: 12px;
}
```

- Cuidado com margin collapsing (top se ajunte ao bottom)

* Padding

Preenchimento interno da caixa

- padding-top | padding-right | padding-bottom | padding-left
- value `<length>` | `<percentage>` | auto

```css
div {
  /* shorthand */
  /* padding: top right bottom left;*/
  padding: 12px 19px 10px 4px;
  /* padding: top right/left bottom ;*/
  padding: 12px 19px 0;
  /* padding: top/bottom right/left  ;*/
  padding: 12px 19px;
  /* padding: all ;*/
  padding: 12px;
}
```

- pandding ponderar causa diferença na largura de um elemento

* Border e outline

  - value `<border-style>` | `<border-width>`| `<border-color>`
    - style: solid| dotted| dashed | double| grove| ridge| insert| outset
    - width `<length>`
    - color: `<color>`

  ```css
  div {
    /* shorthand */
    border-top: solid 2px;
    /*style*/
    border: solid;
    /*width <length> | style */
    border: 2px dotted;
    /*style|color*/
    border: dotted #fff;
    /*width <length> | style | color */
    border: medium dashed green;
  }
  ```

  - outline
    - difere em 4 sentidos
      - nao modifica o tamanho da caixa, pois nao e parte do box
      - poderá ser diferente de retangular
      - nao permite ajuste individuais
      - mains e usando pelo user agent para acessibilidade
