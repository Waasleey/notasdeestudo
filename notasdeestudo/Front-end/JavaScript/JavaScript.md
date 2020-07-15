## O que é JavaScript?

Javascript cuida da parte de inteligência do documento web, tornado a página mais dinâmica. Junto com HTMl e CSS, Javascript é uma das principais tecnologias de front-end.

## Conceitos da Linguagem

#### Operadores Aritméticos

(=) =>  Atribui um valor a um determinado elemente

(==) => Compara se os valores são iguais

(===) => Compara se os tipos dos valores são iguais e se os valores são iguais

(!=) => Compara se os valores são diferentes

(!==) => Compara se os tipos dos valores são diferentes

#### Funções

São blocos de código de JavaScript, e que podem ser invocados usando **nomedafuncao()**

function nomedafuncao(){

    bloco de código...
}

As funções criam um método chamado escopo, caso seja criada uma variável no corpo de função, a variável será visível apenas para a função e não para o restante do código

Para executar funções que retornam um array ou um objeto, para array, basta utilizar:

**nomedafuncao()[indice]**

e para objetos,utilize:

**nomedafuncao().nomedapropriedade**

#### Operadores Lógicos 

(&&) => Operador lógico and

(||) => Operador lógico or

(!) => Operador lógico not

#### Condicionais

Para você verificar se um parametro recebeu determinado argumento, utilize:

if (param === undefined){

    bloco de código...
}


Condições ternárias de forma simples, servem para simplificar em apenas uma linha aquele bloco de código if else no js.

condicao ? true : false;

Switch é um comando para verificar múltiplos cases de condicionais.

**switch(condicao)**{

    case 1://
    case 2: //
    default: //
}

Lembre-se de utilizar o palavra-chave break, pois, caso você não utilize, o resultado do case 1, pode submeter o resultado do case 2.

#### Objetos

Objetos no Js funcionam de forma semelhante em relação a outras linguagens mais focadas a POO como C#, Java e etc.

para criar objetos basta utilizar:

var demo = { propriedade: "valor", propriedade1: 2};

caso eu queira adicionar mais propriedades ao meu objeto demo, utilizo:

demo.propriedade: "valor"

#### Estruturas de Repetição

Estruturas de repetição, são necessários para verificar que um condição que está falsa seja verdadeira.

**while(condicao < parametro)**{

    bloco de código
    condicao++
}

## DOM

**onclick = nomedafuncao()**


## Propriedades

**setInterval(parametro, intervalo)**

setInverval mostra o que está no parametro entre um espaço de tempo determinado pelo intervalo.

**setTimeout(parametro, invervalo)**

É similar a propriedade setInterval, porém, ele mostra algo apenas uma vez após o tempo determinado pelo intervalo.