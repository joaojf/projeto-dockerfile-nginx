# Projeto Dockerfile Nginx

Este projeto permite a criação e execução de um contêiner Docker do servidor Nginx. Ele inclui a cópia de um arquivo cep.html para o contêiner, a exposição da porta 80 e a execução do contêiner.

## Pré-requisitos

Antes de começar, certifique-se de que o seguinte software esteja instalado em seu sistema:

- [Docker](https://www.docker.com/)

## Configuração

1. Clone o repositório do projeto para o seu ambiente local:

   ```shell
   git clone https://github.com/joaojf/projeto-dockerfile-nginx.git

2. Acesse o diretório do projeto:
   ```shell
   cd projeto-dockerfile-nginx

3. Execute o comando Docker para fazer o build da imagem:
   ```shell
   docker image build -t nginx:1.0
   ```
4. Execute o comando docker para rodar o container:
   ```shell
   docker run -d --name nginx -p 80:80 nginx:1.0
   ```
5. Pode fazer um teste pela linha de comando usando o curl:
   ```shell
   curl localhost:80/cep.html
   ```
   - Pode fazer pelo navegador também acessando `htt://localhost:80/cep.html` para ver a página do html.

## Notas

- Certifique-se de ter privilégios de administrador para executar o Docker.
- Lembre-se de modificar as configurações do Dockerfile de acordo com suas necessidades.
- Verifique se possui uma conexão de rede adequada para acessar o Nginx no navegador.
- O arquivo cep.html está incluído no projeto para ser copiado para o contêiner. Caso deseje alterar o conteúdo do arquivo, basta modificá-lo antes de executar o build da imagem.
- Você pode modificar a configuração do Nginx editando o arquivo de configuração dentro do container.

## Contribuição
Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões para melhorar este projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.
