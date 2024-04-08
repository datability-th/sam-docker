# sam-docker

Docker for people using SAM

```bash
docker build -t sam-docker:node14.17.0 ./node14.17.0
docker build -t sam-docker:node18.19.1 ./node18.19.1
docker build -t sam-docker:node20.12.1 ./node20.12.1
```

```bash
docker run -it -d --name sam -v /var/run/docker.sock:/var/run/docker.sock -p 11030:3000 -p 11031:3001 -v $(pwd):/workdir -w /workdir sam-docker

docker run -it -d --name sam -v /var/run/docker.sock:/var/run/docker.sock -p 11130:3000 -p 11131:3001 -v $(pwd):/workdir -w /workdir sam-docker:node18.19.1

docker run -it -d --name sam -v /var/run/docker.sock:/var/run/docker.sock -p 11130:3000 -p 11131:3001 -v $(pwd):/workdir -w /workdir sam-docker:node20.12.1
```
