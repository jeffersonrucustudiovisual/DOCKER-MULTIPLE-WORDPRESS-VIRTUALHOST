# Multiple WordPress Docker containers with NGINX Proxy e LetsEncrypt

## Requisitos

* Docker
* Docker Compose


## NGINX Proxy and LetsEncrypt

_Esses contêineres lidarão com https._

Execute `docker-compose up -d` no diretório `nginx` para iniciar o NGINX Proxy e LetsEncrypt Proxy. 



## WordPress Setup

* Copie o diretório `wordpress_01` para cada site WordPress que você deseja hospedar. Eu criei uma cópia chamada `wordpress_02` como exemplo. Se você deseja hospedar apenas um site, você pode excluir `wordpress_02` e modificar `wordpress_01` ao seu gosto.

* Dentro do wordpress_01 rode o comando `docker-compose up -d` para subir o docker do wordpress e isso vale para os outros wordpress

* Para acessar o php-my-admin adicione a seu dominiom + ${PHPMYADMIN_PORT}



## Build and run containers. 

For each site navigate to its directory and:

``docker-compose up --build``



## Local Development

Para desenvolvimento local, defina os valores de `VIRTUAL_HOST`

No Linux e MacOS adicione esta linha `localhost my_domain_one.com` pelo terminal usando o seguinte comando


```
  $ sudo nano /etc/hosts
```

No Windows Abra o Bloco de Notas ou qualquer outro editor de texto de sua escolha no Menu Iniciar com privilégios de administrador.
(Obs: Sem privilégios de administrador, não é possível salvar as alterações do arquivo hosts feitas no editor.)


- Agora abra o arquivo o seguinte arquivo ```C:\Windows\System32\Drivers\etc\hosts```
- Altere o arquivo com o endereço IP seguido por espaço e domínio/nome do host.
- Salve o arquivo e feche o Editor de Texto.
- Abra o prompt de comando no menu Iniciar e digite ```ping domain.tld```
- domain.tld aqui é o domínio/nome do host para o qual você deseja configurar um host virtual.
- A saída deve mostrar o IP que você adicionou em ' C:\Windows\System32\Drivers\etc\hosts'junto com o domínio/nome do host. Se não, então limpe o DNS. Siga o guia aqui e reinicie o sistema.

## Thema

Faça um git clone dentro da pasta de temas para trabalhar com o projeto que esta atuando
