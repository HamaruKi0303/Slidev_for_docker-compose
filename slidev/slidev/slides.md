---
# try also 'default' to start simple seriph
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: elliott-engelmann-DjlKxYFJlTc-unsplash.jpg
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: slide-left
# use UnoCSS
css: unocss

# フォントはGoogle Fontsから自動的にimportされます。
# 詳細: https://sli.dev/custom/fonts
fonts:
  sans: 'Shippori Mincho'
  serif: 'Shippori Mincho'
  mono: 'Fira Code'

---

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

# Slidev for docker-compose

---

# Index

- [Introduction](#introduction)
- [Environment](#environment)
- [Quick Start](#quick-start)
  - [start docker](#start-docker)
  - [create projects](#create-projects)
  - [run server](#run-server)
- [Reference site](#reference-site)

---



## Introduction

`Slidev`を`Docker for windows`＋`docker-compose`で構築していきます．

---

## Environment

- Windows 11
- Docker for windows

---

## Quick Start

```bash
docker-compose up
```

🌟URL:http://localhost:3030/9

---

### start docker

```bash
docker run --name slidev --rm -it \
    --user node \
    -v ./slidev:/slidev \
    -p 3030:3030 \
    tangramor/slidev:latest
```

---

### create projects

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

---

### run server

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

---

## Reference site

- [sli.dev](https://sli.dev/guide/install.html#install-globally)
- [slidev + docker環境構築メモ](https://zenn.dev/gakin/scraps/bf522ea07c848f)

