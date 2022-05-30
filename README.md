# como trabalha com maven no Spring boot #

## primeramente temos que instalar o ** Maven ** para rodamos a aplição ##

>> Maven é uma ferramenta de automação de compilação utilizada primariamente em projetos Java. Ela é similar à ferramenta Ant, mas é baseada em conceitos e trabalhos diferentes em um modo diferente

>> com o Maven instalado daremos inicio a aplicão

## como executar a Aplicaçao ##

*** Primeiramente baixar as dependencies do arquivo de configuraçao do .pom do Spring boot ***

>> mvn install

## Para roda o Spring boot ##

>> mvn spring-boot:run

## Importante a aplicação precisar do banco de dados ativo na sua maquina ##

*** comando para criar o database no banco de dado ***

>> create database db_gerenciamento

*** Agora como está tudo ok, podemos roda a aplicação do spring-boot ***

>> note que quando você roda a aplicação e olhar dentro do Banco de dados as tables estará la dentro com o comado, primariamente entre no database com o comando __use db_gerenciamento__

>> em seguinda rode com o comando show tables;

# Rotas da Api #

>> O JSON é o que você esta recebendo e enviando para aplicação Backend.

## Sobre as rotas ##
*** rotas usar o prefixo de htpp://127.0.0.1:8080/api ***

# Rota user e Tarefa #

>> Rota get sera o retorno dos dados em JSON.
>> Rota Post será onde você frontend enviara os dados em formato JSON.
>> Rota Delete você passará o id via URL.
>> Rota Update você passará o id via URL e no corpo do body enviara os dados.

### Rota Get User com retorno de um e e muitos ###

>> htpp://127.0.0.1:8080/api/users/1 retorno o usuario esteja cadastrado no BD.
>> htpp://127.0.0.1:8080/api/users retorna todos o users

### Rota Post User ###
>> htpp://127.0.0.1:8080/api/users e envia o Json com seguinte dados
>> { "nome": "allyson", "email":"allyson@gmail.com", "password":123456 }

## Rota Delete User ### 
>> htpp://127.0.0.1:8080/api/users/1 excluir o usuario do bd, mas tem que existir!


## Rota Update User ### 
>> htpp://127.0.0.1:8080/api/users/1 tem que enviar o Id do User via URL, e manda o dados em JSON com esse sequinte perfil { "nome": "allyson bruno", "email":"allyson@gmail.com", "password":123456 }


### Rota Get Tarefa com retorno de um e e muitos ###

>> htpp://127.0.0.1:8080/api/tarefas/1/users/1 o primeiro 1 é referente o Id do user e o segundo 1 é referente a tarefa existente no BD.

>> htpp://127.0.0.1:8080/api/tarefas/1/users retorna todos a tarefas existente referente esse usuario, passado no URL somente o ID USER.

### Rota Post Tarefa ###
>> htpp://127.0.0.1:8080/api/tarefas/1/users e envia o Json com seguinte dados
>> { "nome": "estudo de casa", "descricao": "Api em Spring-boot" }.

## Rota Delete Tarefa do User ### 
>> htpp://127.0.0.1:8080/api/tarefas/1/users/1 delata a tarefa referente ao usuario, primeiro id do User e o ultimo parametro o a ID da tarefa.


## Rota Update Tarefa do User ### 
>> htpp://127.0.0.1:8080/api/tarefas/1/users/1 tem que repetir a mesma coisa das rotas anteriores passando um JSON com ID do USER e ID da Tarefa e em seguinda enviar os dados altualizado com a seguir { "nome": "estudo de casa atualizado", "descricao":" Api em Spring-boot" }





