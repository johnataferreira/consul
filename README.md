# Consul

Projeto criado para experimentar o Service Discovery com o Consul

# Comandos Úteis

-> Para iniciar o docker:

`docker-compose up -d` 

-> Para acessar o docker:

docker exec -it consul01 sh

-> Subindo o consul em modo dev:

consul agent -dev

-> Em outro terminal, veja o consul rodando:

consul members

-> Para consultar os nodes:

curl localhost:8500/v1/catalog/nodes

-> Para trabalhar com o servidor DNS:

Primeiro instalo o dig no linux alpine: apk -U add bind-tools

Depois faço a consulta: dig @localhost -p 8600

Se eu quiser buscar todos os nodes e os ips dos nodes do consul que estão registrados eu rodo:
dig @localhost -p 86000 consul01.node.consul