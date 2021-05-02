# イメージの指定
FROM node:alpine

# コンテナ内で cd /app しているようなもの
WORKDIR /app

# コマンド実行
# linux 最新化,gitのインストール
RUN apk update && apk add git
RUN git clone https://github.com/Kei01234/portfolio.git
# ワーキングディレクトリの変更
WORKDIR /portfolio
# npm最新化、依存関係のインストール
RUN npm install -g npm && npm install

# docker runコマンドを実行した後、ビルドしてサーバをスタートする
ENTRYPOINT ["./docker/start.sh"]

ENV HOST 0.0.0.0
EXPOSE 3000
