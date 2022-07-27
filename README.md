# 使用 docker-compose 一键启动

```shell

请先安装 docker-compose 程序！！！

例如在 debian 11 系统中:

apt update && apt install docker-compose

```

- 现已支持 docker 容器内调用宿主机 docker 来启动 `应用实例`

    - 注意：如果要 `修改挂载目录` 只需要修改 `.env` 文件中的 `INSTALL_PATH`, 目录结尾不要有斜线!!！

- 若不修改任何配置 则您的所有数据将会保存在宿主机的 `/opt/docker-mcsm` 下

- 若您使用 unraid 搭建 docker-mcsm, 那么根据 unraid 的机制, 您的数据必须保存到 /mnt/user/appdata 下才能重启服务器不丢失数据。所以请修改 `.env` 文件中 `INSTALL_PATH=/mnt/user/appdata`。

    - 此时 docker-mcsm 的所有数据会保存到 `/mnt/user/appdata/docker-mcsm` 目录下

<br>

# docker-mcsm_发布版

## Usage

```shell

运行:

git clone https://github.com/zijiren233/docker-mcsm

cd ./docker-mcsm/releases

docker-compose up -d

更新:

cd ./docker-mcsm/releases

docker-compose down

docker-compose build --no-cache

docker-compose up -d

```

- 发布版 web(前端): http://ip:23333

- 发布版 daemon(后端): http://ip:24444

- 发布版中不携带 java,如需运行 java 程序请在 `mcsm面板->环境镜像->环境镜像管理->新建镜像` 中自行构建

    - 实例设置中的 `进程启动方式` 选择 `虚拟化容器`

- 关闭服务器请进入到 docker-compose.yml 文件目录运行 `docker-compose stop`

    - 运行 `docker-compose down` 来移除容器

<br>

# docker-mcsm_开发版

## Usage

```shell

git clone https://github.com/zijiren233/docker-mcsm

cd ./docker-mcsm/dev

docker-compose up -d

```

- 开发版 UI(网页前端): http://ip:8080

- 开发版 MCSManager(控制面板端): http://ip:23333

- 开发版 Daemon(守护进程): http://ip:24444