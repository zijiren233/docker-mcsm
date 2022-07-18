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

- 发布版 web 端: http://ip:23333

- 发布版中自带 java8 java11 java16 java17, 运行不同版本java服务器直接输入 `java(版本号即可)`
    - `java17 -jar server.jar`
    - `java8 -jar server.jar`

<br>

# docker-mcsm_开发版

## Usage

```shell

git clone https://github.com/zijiren233/docker-mcsm

cd ./docker-mcsm/dev

docker-compose up -d --build

```

- 开发版 web 端: http://ip:8080

- 开发版中只包含 java17, java程序已在环境变量中
    - `java -jar server.jar`