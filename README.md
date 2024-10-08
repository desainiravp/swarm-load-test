docker stack deploy -c docker-compose.yml my_stack
docker exec -it $(docker ps -q -f name=my_stack_cockroachdb) ./cockroach init --insecure
docker exec -it $(docker ps -q -f name=my_stack_cockroachdb) ./cockroach node status --insecure
docker exec -it $(docker ps -q -f name=my_stack_cockroachdb) ./cockroach node status --insecure
