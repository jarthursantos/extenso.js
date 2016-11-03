# Extenso.js

![Build Status](https://api.travis-ci.org/theuves/extenso.js.svg)
![NPM version](https://badge.fury.io/js/extenso.svg)

> Escrever números por extenso.

Instale-o com `npm i extenso` ou `bower i extenso.js`.

## Caracteristicas

* aceita número de até **66** digitos
* aceita números negativos e decimais

## Uso

Exija a dependência com:

```js
var extenso = require('extenso');
```

### extenso(*número*[, *opções*])

Onde `número` deve ser um número válido (*number* ou *string*).

E `opções` pode ser:

* `feminino` - para retornar números escritos no feminino
 * para *um* (*uma*) e *dois* (*duas*).

## Exemplos

Veja alguns exemplos abaixo:

```js
extenso(123); //=> 'cento e vinte e três'
extenso(-123); //=> 'menos cento e vinte e três'
```

```js
extenso(1000000); //=> 'um milhão'
extenso('1000000'); //=> 'um milhão'
extenso('1.000.000'); //=> 'um milhão'
```

```js
extenso('1,0'); //=> 'um'
extenso('0,5'); //=> 'cinco décimos'
extenso('1,5'); //=> 'um inteiro e cinco décimos'
```

```js
extenso(1, {feminino: true}); //=> 'uma'
extenso(2, {feminino: true}); //=> 'duas'
```

Números com mais de 15 dígitos **devem** ser passados como *string*:

```js
extenso('10000000000000001'); //=> 'dez quatrilhões e um'
```

## Observações

Use `,` para separar decimais e `.` para separar milhares.

## Licença

MIT ([veja o conteúdo](https://git.io/extenso))
