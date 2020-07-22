<h1 align="center">
    Banco de Dados MySQL
</h1>

Mysql é um sistema de gerenciamento de dados(SGBD) que utiliza a linguagem SQL. Atualmente o MySQL é desenvolvida pela Oracle

<h2 align="center">
    Arquitetura de Software
</h2>

## Padrão MVC

O Padrão MVC pode ser dividida em 3 camadas, que são:

**Model** : É onde fica localizado as Classes modelo, sao classes que representam objetos e esses objetos ficam localizados no banco de dados.

**View** : São as telas do sistema, onde o usuário pode interagir com o sistema e assim enviar informações para serem verificadas pelo banco de dados. Aqui é onde se trabalham com as tecnologias de Front-end.

**Controller** : Nessa camada, fica localizado as regras de negócio e qualquer processamento do sistema fica localizado aqui. Aqui é onde se trabalham com as tecnologias de Back-end.

<h2 align="center">
    Modelagens de Banco de Dados
</h2>

**Modelagem Conceitual** : Rascuho básico sobre as informações que serão inseridas no banco de dados. Pode ser feita em uma simples folha de papel.

**Modelagem Lógica** : É utilizado um programa para que seja criado um banco de dados de forma visual utilizando ferramentas de modelagem, como: BrModelo, DBDesigner, Mysql WorkBench e etc.

**Modelagem Física** : São onde são inseridos os Scripts do banco de dados.

<h2 align="center">
    Iniciando na Modelagem Física
</h2>

**Criando o Banco de Dados**
{

    CREATE DATABASE NOMEDOBANCO;
}

**Conectando ao Banco**
{

    USE NOMEDOBANCO;
}

**Criando a tabela Cliente**
{

    CREATE TABLE NOMEDATABELA(
        NOME VARCHAR(30),
        TELEFONE CHAR(11)
    );
}

**Verificando a tabela**
{

    SHOW DATABASES;
    SHOW TABLES;
}

**Descobrindo os dados de uma tabela**
{

    DESC nomedatabela;
}

<h2 align="center">
    Tipos de dados
</h2>

Para caracteres do tipo texto, temos o **CHAR** e o **VARCHAR**.

**CHAR** : A cara caractere equivale a 1 byte, se a gente for definir um espaço de 30 caracteres(bytes) disponiveis para o usuário preencher, mas por ventura, o usuário preencher 10 caracteres(bytes). O espaço que o dado irá ocupar vai continuar com 30 bytes de memória. CHAR é mais perfomatico que o VARCHAR, porém ele é menos dinâmico; CHAR é um tipo de dado que pode ser utilizado quando já sabemos o que o usuário vai preencher. Ex: Telefone.

**VARCHAR** : VARCHAR é um tipo de dado dinâmico, ou seja, se a gente for definir um espaço de 30 caracteres(bytes) disponiveis para o usuário preencher, mas por ventura, o usuário preencher 10 carcateres(bytes). O espaço de 30 bytes será redimensionado para 10 bytes. Ela é muito útil quando o tipo de informação que o usuário irá inserir é relativa, porém, ela deixa o processo de banco de dados mais lento devido a sua redimensionação de espaço.

**ENUM** : ENUM é tipo de dado, que funciona como um combo-box, limitando ao usuário selecionar uma informação a ser inserida ao banco de dados. Esse tipo de dado só existe no MySQL, em outros bancos de dados é chamada de "constrait".

Para números temos o **INT** e o **FLOAT**

**FLOAT** : São números reais.

**INT** : São números inteiros.

Para objetos como fotos e documentos, temos o **BLOB**

E para textos extensos temos o **TEXT**

<h2 align="center">
    Inserindo Clientes
</h2>

#### Método para inserir dados #1

Este método ele não é muito utilizado, pois, não define a ordem clara de como os dados serão inseridos no banco.

{

    INSERT INTO NOMEDATABELA VALUES('NAME','TELEFONE');
}

#### Método para inserir dados #2

Este método é o mais confiavél, pois, é definida a ordem de como será inseridos os dados no banco.

{

    INSERT INTO NOMEDATABELA('NOME','TELEFONE') VALUES ('WASLEY','1232154');
}

<h2 align="center">
    Seleções, Projeções e filtros
</h2>

Para projetar todos os registros da tabela

{

    SELECT * FROM NOMEDATABELA;
}

Para projetar todos os registro, definindo a ordem de como são apresentadas

{

    SELECT EMAIL, CPF, NOME, SEXO FROM CLIENTE;
}

Também é possível apresentar as informações, criando tabelas 'fictícias'

{

    SELECT EMAIL AS EMAIL_DOS_CLIENTE, CPF, NOME AS CLIENTES, SEXO FROM CLINTE;
}

Pode-se projetar um tabela, com o horário em que ela foi imprimida

{

    SELECT EMAIL, CPF, NOME AS CLIENTE, SEXO, NOW() AS HORARIO FROM CLIENTE;
}

#### Filtros de Seleção

Com os filtros, podemos projetar tabelas apenas com os registros necessários

{

    SELECT NOME, SEXO, EMAIL FROM CLIENTE
    WHERE SEXO = 'F';
}

Podemos filtrar registros através de um dado especifíco

{

    SELECT NOME, SEXO, CPF FROM CLIENTE
    WHERE EMAIL LIKE = '%gmail';
}

<h2 align="center">
    Operadores Lógicos
</h2>

Com os operadores lógicos, é possível criar expressões mais com filtros mais específicos.

OR - Operdador OU.

AND - Opereador E.

NOT - Operador de Negação.

#### Deixando o banco de dados mais rápido, através de expressões lógica.

Vamos imaginar que temos o levantamento dos seguinte dados no banco:

**Utilizando OR**: Coloque a Expressão com mais chance de ser verdadeira na primeira condição.

**Utilizando AND**: Coloque a Expressão com menos chance de ser verdadeira na primeira condição.

#### Filtrando Valores Nulos

{

    SELECT * FROM NOMEDATABELA
    WHERE EMAIL IS NULL;
}

<h2 align="center">
    Delete & Update
</h2>

**Delete**: Serve para deletar registros, caso não seja indicado um registro específico, ele irá deletar todos os registros.


{

    DELETE FROM NOMEDATABELA
    WHERE NOME = 'Wasley'; :(
}
**Update**: Serve para atualizar valores que são indicados na query, caso não seja utilizado um expressão Where, ele irá atualizar todos registro com o valor indicado.

{

    UPDATE NOMEDATABELA
    SET EMAIL = 'conteudo@gmail.com'
    WHERE NOME = 'Wasley';
}

<h2 align="center">
    Primeira Formal Normal - Modelagem
</h2>

#### Regras

**1**: Todo campo vetorizado se tornará outra tabela, campos vetorizados são campos contém o mesmo tipo de informação, ex: telefone.

**2** : Todo campo multivalorado se tornará outra tabela, campos multivaloras são campos que contém várias tipos de informações para o mesmo dado, ex: Endereço.

**3** : Toda tabela necessita de pelo menos um Identificador, tornando assim o registro como único. Não é recomendado colocar como identificador processos de négocios de outros négocios, como: CPF que é da Receita Federal.

<h2 align="center">
    Cardinalidade & Obrigatoriedade
</h2>

A Cardinalidade e a Obrigatoriedade, ou mais conhecido como: (Obrigatoriedade, Cardinalidade) servem para criar relações entre as tabelas.

**Obrigatoriedade**: Serve para definir se um determinado dado seja obrigatório o preenchimento, sendo que para *1(true)*, o preenchimento desse dado é obrigatório, enquanto *0(false)* o preenchimento não é obrigatório.

**Cardinalidade**: Serve para definir se o dado precisa de apenas uma informação, ou pode ser colocada várias informações, ex: telefone,celular, comercial e etc. Sendo *1*, é necessário apenas um registro, não necessitando adionar novos dados, equanto *n*, é necessário para adicionar varios dados no mesmo registro, ex: Posso add 1 ou mais telefones.

#### Como se definir um Cardinalidade e Obrigatoriedade

Pega o primeiro indice da tabela mãe *(X,y)*, e termina com a da tabela filha*(x,Y)*.