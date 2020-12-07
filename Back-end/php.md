## O que é PHP

PHP é uma linguagem de script, adequada ao desenvolvimento web e que pode ser embutida dentro do HTML. PHP é um linguagem de programação Server Side, ou seja, trabalha apenas do lado do servidor. Também é possível a criação de páginas dinâmicas. 

## Diferença entre páginas estáticas e dinâmicas

#### Páginas Estáticas

Páginas estáticas são vistas da mesma forma por todos os usuários.

#### Páginas Dinâmicas

Páginas dinâmicas podem ser personalizadas de forma diferente para usuários distintos. Páginas de Redes Socias são um belo exemplo e se encaixam perfeitamente neste tipo de página.

## Classes

#### Atributos

Recomendação de sempre serem privados.

#### Métodos

Recomendação de sempre serem públicos.

## Variáveis 

As váriaveis do PHP devem começar com $. Os nomes das váriaveis são Case-sensitite, ou seja, nome é diferente de NOME.

**$nomedavariavel**

Tambem é possível referenciar as variáveis com o (&), antes da variável que vc deseja referenciar.

**$teste = "nome"**

**$novo_teste = &$teste** 

##### Nota: Não é possível criar um variável com a palavra this, pois, ela é uma palavra chave da linguagem

O escopo das variáveis funciona de maneira semelhante as demais linguagens existente, com o escopo local e global.

Existe uma palavra chave chamada **$GLOBALS**, onde é possível referenciar variáveis de escopo locais.

## Trabalhando com Strings

Para concatenar strings com variáveis é utilizado:

**"Seu texto: "" . $nomedavariavel**

#### Algumas funções para trabalhar com Strings

**srtlen(param);** Verifica quantos caracteres tem na string, também conta os espaços entre os textos

**stripos(param,param);** retorna o indice da primeira ocorrência

**SUBSTR_COUNT(param,param);** Funciona de maneira semelhante a função stripos, porém, ele diferencia entre maiúsculas e minuscúlas

**strripos(param,param);** retorna o indice da última ocorrência

**strtolower(param);** Todo o texto irá ficar minúsculo

**strtoupper(param);** Todo o texto irá ficar maiúsculo

## Trabalhando com Números

Existem dois tipos de números 'principais', que são os inteiros(int) e os flutuantes(float).

#### Algumas funções para trabalhar com Números

**pow(param,param);** Essa função serve para calcular exponentes.

**rand();** Gera um número aleatório

**rand(param,param);** Gera um número aleatório dentre os parametros passados;

**abs(param);** Converter para um valor absoluto

**is_numeric(param);** Verifica se o parametro passado é um número.(Mesmo se o parametro for do tipo String e for um número, ele irá retornar como true. Wtf, mas vou rever isso)

**is_integer(param);** Verifica se o parametro é um número inteiro

**is_float(param);** Verifica se o parametro é um número flutuante

**round(param);** Arredonda o valor (float)

**floor(param);** Arredonda o valor para baixo (float)

**ceil(param);** Arredonda o valor para cima (float)

## Trabalhando com Array

Array é um variável onde é possível armazenar diversos dados de um mesmo tipo, para criar um array:

**$nomedavariavel = array("Maça","Banana","Jaca");**

Para coletar dados dentro da array é passado o valor como indice, ou seja:

**echo $nomedavariavel[1];** Irá retornar Banana

#### Funções para Array

**count(param);** Conta quantos indices tem no array

**print_r(param);** Verifica os dados do array, porém é apresentado apenas ao dev

## Trabalhando com function

As functions, funcionam de maneira semelhante ao das demais linguagens.

Para uma function retornar múltiplos valores, basta retornar estes valores dentro de um array

function teste($a, $b) { 
     
    $soma = $a + $b;    // soma os parametros
    $sub = $a - $b;     // subtrai os parametros
    return array($soma,$sub); //retorna um array com o valor das variaveis 
}

    $chamada = teste(2,2);  //Variavel para passar os parametros

    echo $chamada[0] . "\n"; 

    echo $chamada[1];

## Trabalhando com Dates

No PHP existe diversas funções referentes a datas, que você pode configurar em poucas linhas

$hora = getdate();
            
            $ano = $hora["year"];
            $mes = $hora["mon"];
            $dia = $hora["mday"];

            $horas = $hora["hours"];
            $minutos = $hora["minutes"];
            $segundos = $hora["seconds"];

            echo $dia . "/" . $mes . "/" . $ano . "\n" . $horas . ":" . $minutos . ":" . $segundos;

## Links

Com o PHP é possível passar links com parametros

## Formulários

#### Métodos de Requisições

#### GET

Requisita um representação do recurso especificado (O mesmo recurso pode ter várias representações, ao exemplo de serviços que retornam XML e JSON).

#### POST

Envia um recurso e solicita que o servidor aceite o recurso como subordinada

#### DELETE

O método DELETE, remove um tipo de dados ou recurso
