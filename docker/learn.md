** Iniciando o deamon do docker
# systemctl enbale docker
# systemctl start docker
# systemctl status docker

** versão do docker
# docker version

** visualizar todos os containers em execução
# docker container ls
# docker ps - comando legado
* container em excução e mortos
# docker container ls -a

** Visular todas as images instaladas
# docker container image ls

** Inicializar um novo conteiner
# docker container run <option> <name>
* option:
         -ti - roda container com I/O
         -d  - roda como deamon(segundo plano)

** Como criar um container sem execuntar
# docker container create <name>

** Terminar a execução de container
# docker container stop <name | container ID:q>

** Inializar um container ja existente
# docker container start <name | container ID>

** Reniciar um container
# docker container restart <name | container ID>

** Pausar e despausar um container
# docker container pause <name | container ID>
# docker container unpause <name | container ID>

** Remover um container
# docker container rm <container ID>
* Forçar
# docker container rm -f <container ID>
* Para remover todos que não estão em uso
# docker container prune

** Conectar a um conteiner
# docker container attach <name | container ID>

** Visualizar informações de um container
#docker container inspect <name | container ID>

** executar um comando no container
# docker container exec <option> <name | conteiner ID> <cmd>

** Capturar logs de um container
# docker container logs -f <name | container id>

