---
title:       Como gerar números aleatórios em Javascript
description: Aprenda sobre a função Math.random() e como gerar um número randômico entre 0 e 1 entre outras receitas
capitulo:    "javascript-random"
ordem:       1
---

A função `random()` do objeto `Math` retorna um número pseudo-aleatório.
```javascript
Math.random();
```


> A função `Math.random()` retorna um ponto flutuante, número pseudo-aleatório no intervalo [0, 1), isto é, de 0 (inclusive)
> até 1, mas não incluindo 1 (exclusive) e que você pode, em seguida, dimensionar para o intervalo desejado.
>
> Fonte: [Mozilla Developer Network / Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)

Em outras palavras, a função retornará um número entre 0 e 1 (podendo incluir o 0 mas não o 1), veja os resultados:

    0.5824683890332182
    0.15599339785628574
    0.19135110741912686
    0.4996250046384343
    0.0008728340690463687


Para gerar números aleatórios na casa do inteiros, devemos multiplicar o método por um inteiro qualquer:
```javascript
Math.random() * 10
```


Agora devemos utilizar a função `Math.floor()` para retirar a parte flutuante (números decimais).

```javascript
Math.floor(Math.random() * 10)
```


O código acima irá gerar números aleatórios no seguinte "range" 0, 1, 2, 3, 4, 5, 6, 7, 8, e 9.

Agora que sabemos como gerar números randômicos, podemos ver algumas receitas...


### Como gerar um número randômico até um valor máximo qualquer!


Se nossa preocupação fosse apenas um teto máximo para o número aleatório, bastaria somar uma unidade ao valor desejado.

O código abaixo gera números aleatórios entre 1 e 10.

```javascript
Math.floor(Math.random() * 10 + 1)
```



Não pense que estamos somando 10 + 1 e multiplicando por `Math.random()`. Na verdade, multiplicamos 10 por `Math.random()`
e, somente depois, somamos uma unidade.

Podemos transformar nosso código em uma função onde recebemos como parâmetro o valor máximo aleatório.

```javascript
function getRandom(max) {
    return Math.floor(Math.random() * max + 1)
}
```



### Como gerar um número randômico booleano (entre 0 e 1):

```javascript
Math.floor(Math.random() * 2);
```


### Como gerar um número randômico tipo bytes ou octet (entre 0 e 256):

```javascript
Math.floor(Math.random() * 256);
```


### Como gerar um número randômico no "range" dos inteiros positivos (entre 0 e 65536):

```javascript
Math.floor(Math.random() * 65536);
```


### Como gerar um número randômico no "range" dos inteiros incluindo os negativos (entre -32768 e 65536):

```javascript
Math.floor(Math.random() * 65536) - 32768;
```