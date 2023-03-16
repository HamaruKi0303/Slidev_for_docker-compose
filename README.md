# Slidev_for_docker-compose


# Index

- [Introduction](#introduction)
- [Environment](#environment)
- [Quick Start](#quick-start)
- [Reference site](#reference-site)

## Introduction

`Slidev`を`Docker for windows`＋`docker-compose`で構築していきます．


## Environment

- Windows 11
- Docker for windows

## Quick Start


```bash
docker run --name slidev --rm -it \
    --user node \
    -v ./slidev:/slidev \
    -p 3030:3030 \
    tangramor/slidev:latest
```

```bash
D:\Prj\Slidev_for_docker-compose>docker-compose exec slidev bash
root@33b4a3f91a99:~/slidev# ls
root@33b4a3f91a99:~/slidev# yarn create slidev
yarn create v1.22.19
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Building fresh packages...

success Installed "create-slidev@0.40.3" with binaries:
      - create-slidev

  ●■▲
  Slidev Creator  v0.40.3

✔ Project name: … slidev
  Scaffolding project in slidev ...
  Done.

✔ Install and start it now? … yes
✔ Choose the agent › npm
```

```bash
root@33b4a3f91a99:~/slidev# npx slidev --remote
  shortcuts           > restart | open | edit | qrcode


  ●■▲
  Slidev  v0.40.3

  theme   @slidev/theme-seriph
  entry   /root/slidev/slidev/slides.md

  public slide show   > http://localhost:3030/
  presenter mode      > http://localhost:3030/presenter/
  remote control      > http://172.22.0.2:3030/presenter/

  shortcuts           > restart | open | edit | qrcode


```


## Reference site

- [sli.dev](https://sli.dev/guide/install.html#install-globally)
- [slidev + docker環境構築メモ](https://zenn.dev/gakin/scraps/bf522ea07c848f)