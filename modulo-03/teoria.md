

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
-  