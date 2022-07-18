# 使用 docker-compose 一键启动

```shell

请先安装 docker-compose 程序！！！

例如在 debian 11 系统中:

apt update && apt install docker-compose

```

<br>

# docker-mcsm_发布版

## Usage

```shell

git clone https://github.com/zijiren233/docker-mcsm

cd ./docker-mcsm/releases

docker-compose up -d --build

```

- 发布版 web(前端): http://ip:23333

- 发布版 daemon(后端): http://ip:24444

- 发布版中自带 java8 java16 java17, 运行不同版本java服务器直接输入 `java(版本号即可)`
    - `java17 -jar server.jar`
    - `java8 -jar server.jar`

- 请勿尝试在 Docker 容器内安装 Docker, 后端可直接运行 Minecraft Bedrock Server

- 关闭服务器请进入到 docker-compose.yml 文件目录运行 `docker-compose stop`

    - 运行 `docker-compose down` 来移除容器

<br>

# docker-mcsm_开发版

## Usage

```shell

git clone https://github.com/zijiren233/docker-mcsm

cd ./docker-mcsm/dev

docker-compose up -d --build

```

- 开发版 UI(网页前端): http://ip:8080

- 开发版 MCSManager(控制面板端): http://ip:23333

- 开发版 Daemon(守护进程): http://ip:24444

- 开发版中只包含 java17, java程序已在环境变量中
    - `java -jar server.jar`