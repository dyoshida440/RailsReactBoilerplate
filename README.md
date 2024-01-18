# 環境構築

参考資料
- https://qiita.com/Yusuke_Hoirta/items/3a50d066af3bafbb8641
- https://zenn.dev/925rycki/articles/655462e9c76906

### 実行
1. docker-compose build<br>
2. docker-compose up -d<br>
（まとめて実行 docker compose up -d --build）<br>
3. docker compose exec api rails db:create

### backend
1. localhost:3001にアクセス

#### frontend
1. docker compose exec front bash(コンテナ内に入る)
2. npx create-react-app . --template typescript
3. npm start
4. localhost:3000にアクセス