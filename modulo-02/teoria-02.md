## Container e Images

### Imagens
conjunto de scrips de arquivos que foi programado
reaproveita outras imagens como base
 - Para Criar uma imagem precisamos de um arquivos Dockerfile
  
### 

A porta deve esta expota não so na camada mas tabem na maquina com a aflag -p ao rodar o container

### alteração de imagem

- Sempre que alterar o codigo da imagem devem ser buildada novamente
- camadas em imagen podem ou nao receber o cahche depende a hierarquia

### cached de camada

- As ordanizações de cahe são executadas de ordem de cima para baixo
- onde ele acha alguma alteração em ingnogara o cache e passa a realizar tudo novamente

### baixando imagem
 - docker pull <nome da imagem desejada>

## informacao do comandos

- docker <comando> --help
- mostrar os detalhes dos subcomandos

## Multipla aplicações mesmo container

 - isso server como escalabilidade onde tem-se varios container apartir da mesma imagem rodando em portas distintas


## Alterando as imagens

- docker tag <id>:<tag>

## Iniciando imagem com um nome

 - flag -t

## Container em modo interativo

 - flag -it
 - flag -i no modo interativo

## Removendo imagens
- docker rmi
  
## removendo imagens e containre nao usados

- docker system prune

## removendo container apos utilizar

 -  um container pode ser deletado automaticamente apos sua parada
 -  flag --rm
 -  economia de espaço 

## Copiando Arquivos do container

- copiando arquivo para dentro de um container
 - rodando o comando 
 - docker run -d -p 3000:3000 --name node_para_copia minhaimage
 - docker cp node_para_copia:/app/app.js ./copia/

## verificar informações de processamento

- verificar as informações de processamento do container
- docker top <nome do container>

- verificar mais informações sobre o container
- docker inspect <container>

- verificar os processo que estão sendo executado
- docker stats
  
## Autenticacao para o terminal no dockerhub

 - criar conta no docker hub
 - docker login
 - docker logout

## versionando uma imagem

 - O versionamento é realizado por tags
 - docker build felipeporto/node_para_copia:tagnova .

