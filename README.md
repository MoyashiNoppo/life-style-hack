# life-style-hack
生活サポートアプリケーション


## 概要
このプロジェクトは、Next.js（フロントエンド）、Spring(バックエンド)、MySQL(データベース)を使用したアプリケーション。


## プロジェクトのクローン方法
### ・mac
任意の作業ディレクトリにプロジェクトを配置する。
ex:home/$user/work/life-style-hack

### ・windows環境
WSL2 + Ubuntu 上でプロジェクトを配置する。
ex:home/$user/work/life-style-hack


## 起動方法
### ・階層の移動    
    ~work/life-style-hack/　に移動する。

### ・起動コマンド（全てのサービス起動）
    docker-compose up --build
    ※初回起動時はビルドに時間がかかる可能性がある。(10分程度)

### ・起動確認コマンド（起動中のサービス一覧表示）
    docker　ps

### ・停止コマンド（全てのサービス停止）
    docker-compose down

### ・個別のサービスだけを起動・停止したい場合
    ex:
        docker-compose up -d db
        docker-compose up -d frontend
        docker-compose stop frontend

## 各アプリケーションへのアクセス
    ・Next.js：http://localhost:3000
    ・spring:http://localhost:####
    ・DB:ポート 3307

# 注意
    docker起動時にmysql-data/というディレクトリが作成されるが、MySQL の永続化ディレクトリです。（git管理対象外済み）
    削除しないように。