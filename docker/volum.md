** ver todas as images instaladas
# docker image ls

** criar uma image a apartir de um dockerfile
# docker image build <option> <name>:<tag> <dockerfile>
- option:
         -t criar image com tag
* Example
# docker image build -t toskeira:1.0 toskeira

** Criando um container com um volume tipo bind
# docker container run <option> --mount type=bind,source=<path>(maquina fisica),destination=<path> <name image>
- example
# docker container run -ti --mount type=bind,src=/opt/storage,dst=/storage
ubuntu

** Criando um volume type volume
# docker volume create <name>

+ OBS: o mesmo volume pode ser usado em multiplos containers

** Inspersionar um volume
#docker volume inspect <name>

** Criando um container com um volume tipo volme
# docker container run <option> --mount type=volume,src=<name
volume>,dst=<path>,{ro} -> (somente leitura) <name>

** Example volume
# docker container run -ti --mount type=bind,src=/volume,dst=/volume ubuntu
# docker container run -ti --mount type=bind,src=/root/primeiro_container,dst=/volume ubuntu
# docker container run -ti --mount type=bind,src=/root/primeiro_container,dst=/volume,ro ubuntu
# docker volume create giropops
# docker volume rm giropops
# docker volume inspect giropops
# docker volume prune
# docker container run -d --mount type=volume,source=giropops,destination=/var/opa  nginx
# docker container create -v /data --name dbdados centos
# docker run -d -p 5432:5432 --name pgsql1 --volumes-from dbdados -e POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker kamui/postgresql
# docker run -d -p 5433:5432 --name pgsql2 --volumes-from dbdados -e  POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker kamui/postgresql
# docker run -ti --volumes-from dbdados -v $(pwd):/backup debian tar -cvf /backup/backup.tar /data


