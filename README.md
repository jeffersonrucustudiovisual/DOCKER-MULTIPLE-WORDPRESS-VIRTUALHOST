# Multiple WordPress Docker containers with NGINX Proxy e LetsEncrypt

## Requisitos

* Docker
* Docker Compose


## NGINX Proxy and LetsEncrypt

_Esses contêineres lidarão com https._

Execute `docker-compose up -d` no diretório `nginx` para iniciar o NGINX Proxy e LetsEncrypt Proxy. 



## WordPress Setup

* Copie o diretório `wordpress_01` para cada site WordPress que você deseja hospedar. Eu criei uma cópia chamada `wordpress_02` como exemplo. Se você deseja hospedar apenas um site, você pode excluir `wordpress_02` e modificar `wordpress_01` ao seu gosto.



## Build and run containers. 

For each site navigate to its directory and:

``docker-compose up --build``



## Local Development

Para desenvolvimento local, defina os valores de `VIRTUAL_HOST`

No Linux e MacOS adicione esta linha `localhost my_domain_one.com` pelo terminal usando o seguinte comando


```
  $ sudo nano /etc/hosts
```

