[![](https://images.microbadger.com/badges/image/ufirstgroup/alpine-node.svg)](https://microbadger.com/images/ufirstgroup/alpine-node "Get your own image badge on microbadger.com")

# docker-alpine-node

based on https://hub.docker.com/r/library/node/

node:

```bash
docker run -it --rm \
  -e USER_ID=`id -u` \
  -e GROUP_ID=`id -g` \
  -v $HOME:/homedir \
  -v `pwd -P`:/workdir  \
  ufirstgroup/alpine-node:8.1.3 node
```

yarn:

```bash
docker run -it --rm \
  -e USER_ID=`id -u` \
  -e GROUP_ID=`id -g` \
  -v $HOME:/homedir \
  -v `pwd -P`:/workdir  \
  ufirstgroup/alpine-node:8.1.3 yarn
```
