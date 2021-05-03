# どのイメージを基にするか
FROM ubuntu:latest

# RUN: docker buildするときに実行される
RUN apt update -y && apt upgrade -y
RUN apt install curl git vim -y
RUN curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh && bash nodesource_setup.sh
RUN apt install nodejs -y
RUN git clone https://github.com/Kei01234/portfolio.git

# ワーキングディレクトリの変更
WORKDIR /portfolio

# 依存関係のインストール
RUN npm install
# start.shに実行権限を付与する
RUN chmod 744 /portfolio/docker/start.sh

# docker runコマンドを実行した後、ビルドしてサーバをスタートする
ENTRYPOINT ["/portfolio/docker/start.sh"]

ENV HOST 0.0.0.0
EXPOSE 3000
