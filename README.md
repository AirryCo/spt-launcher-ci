[![SPT.Launcher Build Nightly](https://github.com/AirryCo/spt-launcher-ci/actions/workflows/cron-nightly-build.yaml/badge.svg)](https://github.com/AirryCo/spt-launcher-ci/actions/workflows/cron-nightly-build.yaml)

[![SPT.Launcher Release Build](https://github.com/AirryCo/spt-launcher-ci/actions/workflows/cron-release-build.yaml/badge.svg)](https://github.com/AirryCo/spt-launcher-ci/actions/workflows/cron-release-build.yaml)

# spt-launcher-ci

Scripts to automate building [SPT/Modules](https://github.com/sp-tarkov/modules) and [SPT/Launcher](https://github.com/sp-tarkov/launcher)

The compilation steps can be found under [.github/workflows](.github/workflows).

Starting from midnight each day, the code from the remote repository will be automatically pulled and compared with the commit hash of the already compiled version defined in the local triggers, the build process will then proceed. (The nightly build trigger is `trigger.nightly`, while the stable version trigger is `trigger`.)

The server is located at: [AirryCo/spt-server-ci](https://github.com/AirryCo/spt-server-ci.git)

You can use `Docker` to run the server.

- DockerHub: https://hub.docker.com/r/stblog/spt-server

- GHCR: https://github.com/AirryCo/spt-server-ci/pkgs/container/spt-server

- Aliyun: registry.cn-shenzhen.aliyuncs.com/spt-server/spt-server

```bash
# Stable version
docker pull stblog/spt-server:latest

# nightly/development version
docker pull stblog/spt-server:nightly

# nightly verison with Fika-Server built-in
docker pull stblog/spt-server:nightly-fika
```

If you find that the server has been updated but the launcher has not, you can still use the old version of the launcher, as there are no differences in the code.

> [!WARNING]
> After downloading, please use extraction software like WinRAR or [7-Zip](https://www.7-zip.org/) to unzip the files, then copy them to the Tarkov root directory. Do not use Windows File Explorer to directly open and copy the files.

---

本仓库主要用来自动化编译 [SPT/Modules](https://github.com/sp-tarkov/modules) 和 [SPT/Launcher](https://github.com/sp-tarkov/launcher)

编译步骤可以在`.gitea/workflows`下查看

每天0点会自动拉取远程仓库的代码与本地文件中定义的，已编译完成的哈希值进行比对，然后进行编译。（每夜版本定义位于为`trigger.nightly`，稳定版的定义为`trigger.release`）

服务端位于： [AirryCo/spt-server-ci](https://github.com/AirryCo/spt-server-ci.git)

你可以选择docker来运行服务端：

- DockerHub: https://hub.docker.com/r/stblog/spt-server

- GHCR: https://github.com/AirryCo/spt-server-ci/pkgs/container/spt-server

- 阿里云：registry.cn-shenzhen.aliyuncs.com/spt-server/spt-server

```bash
# 稳定版
docker pull registry.cn-shenzhen.aliyuncs.com/spt-server/spt-server:latest

# 每夜版/开发板
docker pull registry.cn-shenzhen.aliyuncs.com/spt-server/spt-server:nightly

# 每夜版内置Fika-Server
docker pull sregistry.cn-shenzhen.aliyuncs.com/spt-server/spt-server:nightly-fika
```

如果您发现服务端更新了，而启动器没有更新，那么您依然可以使用旧标签的启动器，因为他们在代码上没有任何区别。

> [!WARNING]
> 下载之后，请使用WinRAR、[7-Zip](https://www.7-zip.org/)等解压缩软件进行解压，再复制到塔科夫根目录，请勿使用windows资源管理器直接打开并复制!!!

