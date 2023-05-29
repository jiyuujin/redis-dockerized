# redis-dockerized

## Installation

Install Docker (docker-compose).

https://docs.docker.com/compose/install/linux/#install-the-plugin-manually

```bash
brew install docker docker-compose
docker -v

# docker compose インストール
mkdir -p ~/.docker/cli-plugins
ln -sfn $(brew --prefix docker-compose)/bin/docker-compose $DOCKER_CONFIG/cli-plugins/docker-compose
echo -e "\nexport DOCKER_CONFIG=\${DOCKER_CONFIG:-\$HOME/.docker}" >> ~/.zshrc
docker compose version
```

Use docker compose.

```bash
# コンテナ作成
docker compose up -d

# 作成済コンテナのターミナルへ接続
docker exec -it <作成したコンテナID> bash
```

### Container Operation

Operate containers.

```bash
redis-cli
```
