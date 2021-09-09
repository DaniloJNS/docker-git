** Ver status de um container
# docker container stats <container ID>

** Inicializar container com uso de memoria e cpu definido
# docker container run --memory <bits> --cpus <%> <name>

- Example docker container run -m 128M --cpus 0.5 (50% da cpu) ubuntu
** Atualizar uso de recursos (pode ser usado com container em execução)
# docker container update <status> <name>
- Example docker container update --cpus 0.2 <container ID>


- bonus: ver informações da cpu $ cat /proc/cpuinfo

** Resumo de comandos 
# docker container stats [CONTAINER ID]
# docker container top [CONTAINER ID]
# docker container run -d -m 128M --cpus 0.5 nginx
# docker container update --memory 64M --cpus 0.4 nginx
# docker container inspect [CONTAINER ID]
# docker container stats [CONTAINER ID]
# docker container top [CONTAINER ID]

