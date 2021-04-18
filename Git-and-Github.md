## O que é Git e GitHub?

Git é um sistema de controle de versão, onde é possível gerenciar as versões do seu código, a cada versão do seu código é criado um repositório local no seu computador, criando assim uma espécie de "maquina do tempo" no seu código. Enquanto o GitHub pode ser comparada como uma "rede social para programadores", o GitHub também serve como um repositório Remoto, onde é possível hospedar o seu repositório local nele.

## Termos do Git e Github

#### Commit

Commit são todas as alterações feitas no repositório sendo salvas, por isso o termo: "commita esse código".

#### Branch

Branch seria técnicamente, a linha de desenvolvimento de uma feature.

#### Repositório

Repositório é a pasta do projeto, todo repositório contém uma pasta oculta chamada .git, onde fica localizada
todas as configurações do seu repositório.

## Comandos

Após instalar o git é recomendado configurar algumas opções dele

#### git config --global user.name "Seu nome"

Configura o nome de usuário do seu git, é recomendado que você utilize o seu próprio ou o seu algum nome que
você seja reconhecido.

#### git config --global user.email "seuemail@.com"

Configura o seu email no seu git.

#### git config --global code.editor nome do seu editor

Configura o seu editor padrão.

#### git config --list

Lista todas as configurações do seu git.

#### git clone linkdorepositorio

Efetua o download do repositório inicializando o repositório local.

#### git init

Inicializa o repositório local do seu projeto.

#### git status

Verificar o status dos seus arquivos do projeto.

#### git commit -m "Mensagem Descritiva"

Commita o seu código

#### git remote add origin linkdoseurepositório

Sincroniza o seu repositório local, com o seu repositório remoto.

#### git pull nomedorepositorio branch

Baixa todas as alteração que houve no repositório.

#### git push nomedorepositorio branch

Sobe para o servidor as atualizações que houve no repositório.

#### git branch

Verifica a branch atual.

#### git checkout nomedabranch

Realiza a alteração para a branch indicada.

#### git checkout -b nomedabrach

Cria uma nova branch, e realiza a alteração para a mesma.

#### git checkout

Desfaz as alterações realizadas no código, antes de adiciona-las para commit.

#### git reset

Desfaz as alterações realizadas, antes de commitá-las.

#### git revert

Desfaz as alterações realizadas em um commit específico.

#### git stash

Armazena temporáriamente as alterações realizadas.

#### git checkout códigodocommit

Volta na linha de desenvolvimento, para o commit informado.

#### git diff

Verifica as mudanças realizadas no código durante o desenvolvimento.

#### git tag -a nomedaversão

Cria uma realease para o código.