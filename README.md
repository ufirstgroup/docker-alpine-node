[![](https://images.microbadger.com/badges/image/ufirstgroup/alpine-node.svg)](https://microbadger.com/images/ufirstgroup/alpine-node "Get your own image badge on microbadger.com")

# docker-alpine-node

```bash
docker run -it --rm \
  -e USER_ID=`id -u` \
  -e GROUP_ID=`id -g` \
  -v $HOME:/homedir \
  -v `pwd -P`:/workdir  \
  ufirstgroup/alpine-node:8.0.0 node
```
