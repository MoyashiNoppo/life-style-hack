FROM openjdk:17-jdk-alpine

# Maven インストール
RUN apk update && apk add --no-cache maven

WORKDIR /app

# pom.xml のみを先にコピーして依存関係を取得
COPY pom.xml .
RUN mvn dependency:go-offline -B

# ソースコードをコピー
COPY . .

# ビルド（テストはスキップ）
RUN mvn clean package -DskipTests

# devtools リロード有効化（Spring Boot DevTools使用前提）
ENV JAVA_OPTS="-Dspring.devtools.restart.enabled=true -Dspring.devtools.livereload.enabled=true"

# アプリ実行
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar target/*.jar"]