# hw2前端部分

[![Docker](https://github.com/ds-hw-fuuzen/hw2-frontend/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/ds-hw-fuuzen/hw2-frontend/actions/workflows/docker-publish.yml)

## 一键启用 docker + VSCode 开发环境

开发环境镜像在本仓库的 ghcr.io 注册表中，确保您的 docker 登录到 ghcr.io

克隆本仓库到您的电脑中，确保您的 VSCode 安装了 Dev-Containers 插件

请注意 `.devcontainer/devcontainer.json` 中这部分内容:
```json json
{
    "mounts": [
        "source=${HOME}/.ssh,target=/root/.ssh,type=bind"
    ]
}
```

如果你是 Windows 平台,请修改为硬编码正斜杠路径,例如我的用户名 `fuuzen`:

```json json
{
    "mounts": [
        "source=/c/Users/fuuzen/.ssh,target=/root/.ssh,type=bind"
    ]
}
```

VSCode 打开本仓库，ctrl + shift + p (command + shift + p for mac) 输入 Reopen with container 使用开发容器打开,若没有本地还镜像将自动拉取镜像,您也可以手动拉取:

```shell shell
docker pull ghcr.io/ds-hw-fuuzen/hw2-frontend:master
```
