

## volumes

- forma pratica de persistir dados em aplicações sem prescisar de container
- container são reiniciado e os dados somem
- pasta do computados são usado como link
  

### Tipos de volumes
 - Anonymous flag -v (nome aleatorio)
 - Named são registrado de forma definida
 - Bind mounts: são arquivo são salvos em uma host de responsabilidade do gerenciados

### Volumes Anonymous

- docker run -v /data
- onde o data será o diretorio que contém o volumen anonimmo
- docker ls (Verificamos todos os volumes do nosso ambente)

### Named Volumes

- docker run -v nomedovolume:/data

### Bind Mount Volume

-  Também é um volume porém ele fica em um  diretorio que nós especificamos
-  Sera necessario pemisão para acessar diretorios fora do docker
-  Atualização em tempo real  com o bind mount
    [x] Adicionando a pasta do projeto sincronizando com o volume do docker
    temos um hot reload
    [X] home/meu-diretorio/projeto:var/diretorio-container/projeto

### Criar um volume

- docker volume create <nome>
- docker listagem de volumes 'docker ls'
- bind moun não é considerado um volume para o docker

### Inpecionando Volumes

- docker volume inspect <nome>

### Remover um volume
- docker volume rm <nome>

## Remover volumes nao utilizados
- docker volume prune

## Volumes apenas de leitura
- docker run -v volume:/data:ro
- ro readonly -> somente de leitura