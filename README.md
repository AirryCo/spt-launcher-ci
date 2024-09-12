![CI](https://dev.sp-tarkov.com/medusa/spt-launcher-ci/actions/workflows/cron-nightly-build.yaml/badge.svg)

![CI](https://dev.sp-tarkov.com/medusa/spt-launcher-ci/actions/workflows/cron-release-build.yaml/badge.svg)

# spt-build-ci

Scripts to automate building SPT `modules` and `launcher`

This repository is primarily used for automating the compilation of `spt/modules` and `spt/launcher`, The compilation steps can be found under `.gitea/workflows`.

Starting from midnight each day, the code from the remote repository will be automatically pulled and compared with the commit hash of the already compiled version defined in the local triggers, the build process will then proceed. (The nightly build trigger is `trigger.nightly`, while the stable version trigger is `trigger`.)

The server that matches the `launcher` and `modules` compiled from this repository is located at: [medusa/spt-server-ci](https://dev.sp-tarkov.com/medusa/spt-server-ci.git)

You can use `Docker` to run the server.

https://dev.sp-tarkov.com/medusa/-/packages/container/spt-server/latest

```bash
# Stable version
docker pull dev.sp-tarkov.com/medusa/spt-server:latest

# nightly/development version
docker pull dev.sp-tarkov.com/medusa/spt-server:nightly
```

> [!WARNING]
> After downloading, please use extraction software like WinRAR or [7-Zip](https://www.7-zip.org/) to unzip the files, then copy them to the Tarkov root directory. Do not use Windows File Explorer to directly open and copy the files.

---

本仓库主要用来自动化编译`spt/modules`和`spt/launcher`

编译步骤可以在`.gitea/workflows`下查看

每天0点会自动拉取远程仓库的代码与本地文件中定义的，已编译完成的哈希值进行比对，然后进行编译。（每夜版本定义位于为`trigger.nightly`，稳定版的定义为`trigger`）

与此仓库编译出来的`launcher`和`modules`相匹配的服务端位于： [medusa/spt-server-ci](https://dev.sp-tarkov.com/medusa/spt-server-ci.git)

你可以选择docker来运行服务端：

https://dev.sp-tarkov.com/medusa/-/packages/container/spt-server/latest

```bash
# 稳定版
docker pull dev.sp-tarkov.com/medusa/spt-server:latest

# 每夜版/开发板
docker pull dev.sp-tarkov.com/medusa/spt-server:nightly
```
> [!WARNING]
> 下载之后，请使用WinRAR、[7-Zip](https://www.7-zip.org/)等解压缩软件进行解压，再复制到塔科夫根目录，请勿使用windows资源管理器直接打开并复制!!!

