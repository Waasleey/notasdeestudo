## Classes

Classes são a forma de "moldar" as instâncias que serão criadas a partir dela.

## Atributos

Atributos são indicados dentro das classes, e informam as caracteristicas de a classe irá receber.

## Objetos

Objetos são criados/instânciados a partir do "molde" de uma classe. Para criar uma instância em Java, segue abaixo o código.

{

    Tipodoobjeto nomedareferencia = new tipodaclasse();
}

## Referências

Referências é uma indicação do objeto na mémoria, ou seja, a cada objeto que é criado, ele recebe um idenficador de uma referência que indica o seu valor na mémoria.

## Atribuindo valores as instâncias

Para atribuir valores as instâncias, segue o código abaixo.

{

    nomedareferencia.nomedoatributo = valor;
}

## Criando métodos

Métodos são comportamentos que são utilizados para modificar os atributos de um objetos, como por exemplo, método **Sacar** é utilizado para sacar dinheiro de uma conta bancária. Para criar um método segue o código abaixo.

{

    void nomedometodo (argumento)
    {
        código do método;
    }
}

Para chamar o método, basta utilizar o seguinte código

{

    nomedareferencia.nomedometodo();
}