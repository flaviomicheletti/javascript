---
title:       Referência prática ao objeto literal em JavaScript
description: O objeto literal var foo = {} talvez seja a forma mais intuitiva de se aprender OOP em JavaScript
capitulo:    "javascript-referencia"
ordem:       11
---

Senhoras e senhores, com vocês a palavra de Stoyan Stefanov...

Se não estiver acostumado à notação literal, ela poderá lhe parecer um pouco estranha no início, mas quanto mais você a
utilizar, mais vai amá-la. Essencialmente, as regras de sintaxe são:

- Encapsule o objeto entre chaves `{}`.

```javascript
var obj = {}
```

- delimite as propriedades e métodos com vírgulas dentro do objeto. Uma vírgula final após o último par nome-valor é
permitido mas produz erros no IE (sempre o IE), então não faça isso.

- Separe nomes de propriedades e valores com um sinal de dois-pontos `:`.

```javascript
var obj = {
    a: "",
    b: "",
    c: "",
    funcao1: fucntion (){},
    funcao2: fucntion (){},
    funcao3: fucntion (){}
}
```

- Ao atribuir o objeto a uma variável, não se esqueça do ponto e vírgula após a chave de fechamento.

```javascript
var obj = {
    // seu código
    // seu código
    // seu código
};
```


- - -
Fonte: Padrões JavaScript, Stefanov, pág. 58]
