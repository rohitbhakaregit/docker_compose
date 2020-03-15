# docker_compose

```
ref docker commands

docker run -d  --name=redis redis 
docker run -d  --name=db -e POSTGRES_HOST_AUTH_METHOD=trust  postgres:9.4
docker run -d --name=vote -p 3000:80 --link redis:redis eesprit/voting-app-vote
docker run -d --name=result -p 3001:80 --link db:db eesprit/voting-app-result
docker run -d --name=worker --link redis:redis --link db:db  eesprit/voting-app-worker

```
