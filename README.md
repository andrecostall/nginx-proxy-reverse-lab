# nginx-proxy-reverse-lab
Configuração de Balanceamento com Nginx Proxy Reverso
# nginx-proxy-reverse-lab
Configuração de Balanceamento com Nginx Proxy Reverso

Este repositório contém os arquivos de configuração necessários para montar um cenário com quatro contêineres Docker, onde dois contêineres exibirão uma página web azul e os outros dois exibirão uma página web vermelha. Esses contêineres serão balanceados utilizando o Nginx como Proxy Reverso.

## Pré-requisitos
Antes de iniciar, verifique se você possui os seguintes pré-requisitos instalados em sua máquina:

Docker: https://docs.docker.com/get-docker/
Docker Compose: https://docs.docker.com/compose/install/


## Como Executar
Siga os passos abaixo para montar o cenário com os contêineres Docker, após o download do repositório:
$ cd nginx-proxy-reverse-lab
$ sudo docker compose up -d

## Configurar hosts
Configure o arquivo /etc/hosts (ou C:\Windows\System32\drivers\etc\hosts no Windows) para apontar para o endereço IP 127.0.0.1 das URLs desejadas:
127.0.0.1 all.labs.com.br
127.0.0.1 red.labs.com.br
127.0.0.1 blue.labs.com.br


Agora, ao acessar all.labs.com.br em um navegador, você será balanceado entre as páginas web azul e vermelha. O mesmo acontecerá ao acessar red.labs.com.br e blue.labs.com.br.

## Considerações Finais
Este é apenas um exemplo simples de configuração de balanceamento de carga com Docker e Nginx Proxy Reverso.