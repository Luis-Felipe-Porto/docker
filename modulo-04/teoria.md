
## Networks

O que são networks
uma forma iniciar a comunicaçõa do docker com outros containers

### tipos de conexões

- Externa -> conexão de uma api com um servidor remoto
- Com host(nossa maquina) -> comunicação com maquina que está executando o docker
- Entre container -> comunicação que utiliza o drive bridge(mesma rede)

### tipos de rede(Driver)

- Bridge -> default do docker  usado quando container prescisam se conectar
- Host -> permite a conexão de um container com a maquina que esta hosteando docker
- macvlan -> permite a conexão de um container para um MAC adress
- none -> remove todas as conexão de rede de um container isolado no espaco
- plugins -> permite extensões de terceiros para cirar outras redes


### Listando redes
- docker network ls **alguma redes já são criadas**

### Criando uma rede
- docker network create <nome>
- tipo default bridge quan não é inicializado


### Removendo redes

- docker network rm minharedeteste

removendo redes em massa
- que não estaão sendo utilizadas no momento

### conexão esternas

-  conexão com outra api web

## conexão com host

- podemos conectar um conatiner com o host do docker
- ip de host usamos <host.docker.internal>
  
### Conexão entre containers
 - Quando usamos uma rede em bridge podemos usar a rede de conexão
 - nos referindo apenas pelo nome do container

### Conectar um container a uma rede

 - docker network connect <rede> <container>
 - Serve para reconectar um container quando perde a conexão entre rede com um outro container

### Desconectando um conatiner de uma rede

 - docker network disconnect <rede> <container>

### inspecionar redes

 - docker network inspect <nome>
