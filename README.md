# registry
A SECURE DOCKER 2.0 REGISTRY WITH BASIC AUTHENTICATION

## Requirements
- letsencrypt
- docker and docker-compose

## Installation
1. create a valid letsencrypt certificate for your domain - check this [tutorial](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-16-04) 
2. split your certificate into a cert and a key (run `bin/generate-key-cert-from-pem <path/to/letsencrypt/live/>`)
3. generate a httpasswd file (run `bin/generate-htpasswd <username> <password>`)
4. install the expected directories (run `bin/install.sh`)
5. expose the domain to the container (export DOMAIN="my.domain.fr")
6. go to /containers/registry and run `docker-compose up -d`
