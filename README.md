![CI](https://dev.sp-tarkov.com/medusa/spt-build-ci/actions/workflows/cron-nightly-build.yaml/badge.svg)

![CI](https://dev.sp-tarkov.com/medusa/spt-build-ci/actions/workflows/cron-release-build.yaml/badge.svg)

# spt-build-ci

Scripts to automate building SPT `modules` and `launcher`

This repository is primarily used for automating the compilation of `spt/modules` and `spt/launcher`, The compilation steps can be found under `.gitea/workflows`.

Starting from midnight each day, every 3 hours, the code from the remote repository will be automatically pulled and compared with the commit hash of the already compiled version defined in the local triggers, the build process will then proceed. (The nightly build trigger is `trigger.nightly`, while the stable version trigger is `trigger`.)

The server that matches the `launcher` and `modules` compiled from this repository is located at: [medusa/spt-server](https://dev.sp-tarkov.com/medusa/spt-server.git)

Note: The `spt-server` is compiled only for Linux and does not support Windows. Therefore, you can use `Docker` to run the server.

https://dev.sp-tarkov.com/medusa/-/packages/container/spt-server/latest

```bash
# Stable version
docker pull dev.sp-tarkov.com/medusa/spt-server:latest

# nightly/development version
docker pull dev.sp-tarkov.com/medusa/spt-server:nightly
```

---

本仓库主要用来自动化编译`spt/modules`和`spt/launcher`

编译步骤可以在`.gitea/workflows`下查看

每天0点开始，每隔3个小时，会自动拉取远程仓库的代码与本地文件中定义的，已编译完成的哈希值进行比对，然后进行编译。（每夜版本定义位于为`trigger.nightly`，稳定版的定义为`trigger`）

与此仓库编译出来的`launcher`和`modules`相匹配的服务端位于： [medusa/spt-server](https://dev.sp-tarkov.com/medusa/spt-server.git)

注意：服务端只编译了Linux版本，不支持windows，因此，你可以选择docker来运行服务端：

https://dev.sp-tarkov.com/medusa/-/packages/container/spt-server/latest

```bash
# 稳定版
docker pull dev.sp-tarkov.com/medusa/spt-server:latest

# 每夜版/开发板
docker pull dev.sp-tarkov.com/medusa/spt-server:nightly
```

