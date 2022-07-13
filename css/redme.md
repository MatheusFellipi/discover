# comentários

os comentários começa com `/*` e termina com `*/`

```css
/* basico */

body {
}
. . . h1 {
}
```

# Anatomia

```css
h1 {
  color: blue;
  font-size: 60px;
  background: gray;
}
```

- selector -> h1, body ,class, id
- declaration
- properties -> color,font etc.
- property Value -> blue,60px etc.

# Selectors

conecta um elemento HTML com CSS

## tipos

- Global selector `*`
- element/Type selector `h1, h2, p, div`
- Id selector `#box #container`
- Class Selector `.red .m-4`
- Attribute selector, pseudo-class, Pseudo-element, e outros

# caixa

- Voce irar perceber que (quase ) tudo sao caisa do css.

- posicionamentos, tamanho, espacamentos,bordas cores.

- caixa pode fica ao lado de outra ou acima

- Elementos HTML sao caixa

```html
<h1>Evolua rápido</h1>
<p>Descrição</p>
<button>Embarca</button>
```

```css
h1 {
  h1 {
    border: 1px solid red;
    margin: 200px;
    padding: 60px;
  }
}
```

# Adicionar Css no Html

## inline

- atributo `style`

```html
<h1 style="color :red">Título</h1>
```

## <styles>

- tag html que irar conter o css

```html
<style>
  h1 {
    color: red;
  }
</style>
```

## link

- arquivo css externo

```html
<head>
  <link rel="stylesheet" href="style.css" />
</head>
```

## @import

- arquivo css externo

```css
@import "" nao indica;
```

# A cascata (cascading)

a escolha do browser de qual regra aplica, caso haja muita regra para o mesmo elemento.

- seu estilo e lido de cima para baixo.

E levando em consideração 3 fatores

1. Origen do estilo.
2. Especificidade.
3. Importância.

### Origen do estilo

inline > tag style > tag link

### Especificidade

E um calculo matemático, onde, cada tipo de seletor e origem do estilo , possuem a serem considerados.

0. universal selector, combinators e negation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
2. classes e attribute selector ([type="radio"])
3. Id selector
4. Inline

### A regra !important

- cuidado, evite o uso
- nao e considerado um boa pratica
- quebra o fluxo natura da cascata

# At-rules

- esta relacionado ao comportamento do css
- começa com o sinal de `@` seguido do identificador e valor.

## Exemplos Comuns

- @import -> incluir um css externo
- @media -> regras condicionais para dispositivos
- @font-face -> font externas
- @keyframes -> Animations

# Funcao

- nome seguido de abre e fecha parentesis

## exemplos

```css
{
  color: rgb(255,0,100)
  width:calc(100%-10px )
}
```
