# docker-mcsm_releases

## Usage

```shell

git clone https://github.com/zijiren233/docker-mcsm

cd docker-mcsm/releases

docker-compose up -d --build

```

- 发布版中自带 java8 java11 java16 java17, 运行不同版本java服务器直接输入 `java(版本号即可)`
    - `java17 -jar server.jar`
    - `java8 -jar server.jar`

# docker-mcsm_dev

## Usage

```shell

git clone https://github.com/zijiren233/docker-mcsm

cd docker-mcsm/dev

docker-compose up -d --build

```

- 开发版中只包含 java17, java程序已在环境变量中
    - `java -jar server.jar`