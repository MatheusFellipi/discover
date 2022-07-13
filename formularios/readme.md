# Formularios

## para que serve

- capturar dados de entrada ( input)
- Interação
- Controle

## Pre Requisitos

- Basicos HTML

## Domnar

- estilização
- validação
- controles
- javascript

# Primeiro passo

- Elementos que definira um formularios
- E um container estilo <section> <footer>

## Atributos básicos

- action
- method

```html
<form action="" method=""></form>
```

# Agrupando campos form

- fieldset

  - agrupamento de campos
  - mesmo propósito
  - semântico
  - acessibilidade

- atributos especiais

  - disabled

    - desabilita todos os elementos internos
    - nao serão enviados ao submetam o formulário

  - form

    - o id de um formulário ao qual esse fieldset pertence
    - nao precisa esta dentro do formulário

  - name

    - nome do grupo

  - legend
    - nome do agrupamento
    - primeiro elemento dentro do fieldset

```html
<form action="" method="">
  <fieldset>
    <label for="">Nome</label>
    <input type="text" />
  </fieldset>
</form>
```

### label

- associa e identificar uma ou mais tag de entradas de dados
- acessibilidade
- voce poderar clicar para mudar o foco da entrada de dados

- atributos
  - for
    - para fazer conexao entre esta label e a tag de entrada de dados
    - feita via id do inout
    - so funciona em elemendo especificos
      - button,input (not hidden),meter, output, progress,select,textarea

```html
<label>
  Nome:
  <input type="text" />
</label>
```

### button

- representa um button
- usando para enviar formularios
- e estilizado pelo user agent

- Atributos comuns

  - type
    - submit
    - reset
    - button
  - autofocus
  - disabled
  - name
  - value
  - form

  ### dataList

  - lista de valores como sugestão a uma tag `<input>`
  - valores sugestivos e nao obrigatorios
  - usuario poderao selecios um dos valores ou coloca um valor defirente da sugestao

  ```html
  <datalist>
    <option value="">option 01</option>
    <option value="">option 02</option>
    <option value="">option 03</option>
    <option value="">option 04</option>
    <option value="">option 05</option>
  </datalist>
  ```

#### list

-recebe com valor o id de um datalist nresidente no mesmo documento

- tipos de valores
- text,search, utl,tel ,email ...

* valor de datales que nao sao compativel com o tipo do input nao serao apresentados

* Tipos de input nao suportados

- hidden, password,checkbox, radio,file,ou qualquer tipo de button

### tag de input

- um dos mais usando em formularios
- aceita os mais deverso tipos de dados um dos mais poderoso e complexos
- elevado numero de ombinacoes

- atributos

  - type
    - text, date,...
  - name
  - id

  - autocomplete

    - completa um dados que usa com frequência

  - autofocus: boolean
  - value
  - disabled
  - readonly (quase todos)
  - form -> caso o input esta em outra area da pagina (quase todos)
  - name
  - required (quase todos)
  - placeholder 

```html
<input type="text" />
<input type="date" />
<input type="password" />
```

* `<input type="password" />`

- atributos 
  - min/max
    - limitar o numero de caracteres do campo.

#### difinir um formularios

- pensa nos requisitos
- ajuda a definir as necessidades

- dicas:
  - simples e focados
  - somente dados necessários
  - verifique o que te agrada