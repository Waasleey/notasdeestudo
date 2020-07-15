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