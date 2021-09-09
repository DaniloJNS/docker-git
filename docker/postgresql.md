** Criando o container de dados
# docker container create -v /data --name dbdados centos

** Como criar um container postgresql
# docker run -d -p 5432:5432 --name pgsql1 --mount src=<name> dbdados -e
# POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker
# kamui/postgresql

* Explicando os comandos

 - Configurando a porta do postgresql
# -p 5432:5432
 - nome do container
# --name pgsql1
 - definido o volume
# -volumes-from dbdados
 - variaveis de ambiente do container
# -e POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker
 - nome da image
# kamui/postgresql

