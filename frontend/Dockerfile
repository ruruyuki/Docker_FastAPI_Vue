# Node.js（17.5.0）は2022-02-10リリース
# vue createなどでエラーとなった場合は最新版に設定しなおす
FROM node:17.5.0-stretch-slim

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

WORKDIR /app

RUN yarn global add @vue/cli @vue/cli-init

# axiosをインストールする
RUN yarn add axios vue-axios
# RUN if [ -f package.json ]; then \
#         yarn add axios vue-axios; \
#     fi

# vueサーバーの起動(vueアプリが作成されていた際に実行)。コンテナが起動してから30秒後くらいに起動。
CMD if [ -f package.json ]; then \
        yarn serve; \
    fi


# vueアプリが作成されいない状態（初期構築時）は手動で以下のコマンドを実行する
# docker exec -i -t frontend bash
# RUN vue create .
# yarn add axios vue-axios