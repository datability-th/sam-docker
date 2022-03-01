# sam-docker
Docker for people using SAM

```bash
docker build -t sam-docker ./node14.17.0
```

```bash
docker run -it -d --name sam -v /var/run/docker.sock:/var/run/docker.sock -p 11030:3000 -p 11031:3001 -v $(pwd):/workdir -w /workdir sam-docker
```
