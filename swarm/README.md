# SWARM

## Check Swarm deployed services
docker service ls
docker service ps {id}{name}

## Docker stack deploy
docker stack deploy -c docker-stack.yml {name}

## Check stack deployed services
docker stack ps {name}
docker stack services {name}