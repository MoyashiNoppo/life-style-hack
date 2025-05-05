# Node.js公式イメージをベースにする
FROM node:18

# 作業ディレクトリを作成
WORKDIR /app

# package.json と lock ファイルをコピーして依存関係をインストール
COPY package*.json ./
RUN npm install

# ソースコード全体をコピー
COPY . .

# 開発サーバーを起動
CMD ["npm", "run", "dev"]
