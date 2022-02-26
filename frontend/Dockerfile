# Node.js（17.5.0）は2022‑01‑18リリース
# vue createなどでエラーとなった場合は最新版に設定しなおす
FROM node:17.5.0-stretch-slim

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

WORKDIR /app

RUN yarn global add @vue/cli @vue/cli-init


# vueアプリが作成されいない状態（初期構築時）は手動で以下のコマンドを実行する
# docker exec -i -t frontend bash
# vue create .
# yarn add axios vue-axios

# vueサーバーの起動(vueアプリを作成した後、有効化する)。コンテナが起動してから30秒後くらいに起動。
CMD yarn serve