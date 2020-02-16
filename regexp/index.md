---
title:       RegExp()
description: Referência prática da função RegExp() em JavaScript
capitulo:    javascript-regex
ordem:       4
---


Utilizando-se do construtor `RegExp()` podemos compilar a expressão regular antes de usá-la.

Isso é uma vantagem? Não exatamente.

Caso sua expressão esteja sintaticamente errada o erro existirá como nos demais exemplos e seu código irá travar.

Uma vantagem seria o fato de ser possível criar a expressão regular a partir de uma string, isto quer dizer que
é possível __criar a expressão de forma dinâmica__.

Imagine que o usuário irá digitar a palavra "exemplo" e o sistema armazenará o valor na variável `regexp`.

Agora é só passar a variável para o construtor e executar a expressão regular.

Resumindo, a expressão regular criada a partir de uma string lhe derá __mais flexibilidade__.


```javascript
var string  = "Casa com a palavra exemplo",
    pattern = {},
    regexp  = /exemplo/;

// pattern.test
pattern = new RegExp(regexp);
console.log(pattern.test(string)); // true

// pattern.exec
pattern = new RegExp(regexp);
console.log(pattern.exec(string)); // ["exemplo", 19, "Casa com a palavra exemplo"]

// string.match
pattern = new RegExp(regexp);
console.log(string.match(pattern)); // ["exemplo", 19, "Casa com a palavra exemplo"]
```


Uma vez com a expressão regular compilada podemos executá-la em qualquer uma das três formas já discutidas:
[test()](/javascript/pattern-test/),
[exec()](/javascript/pattern-exec/) e
[match()](/javascript/string-match/).
