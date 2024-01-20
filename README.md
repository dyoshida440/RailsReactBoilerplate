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
2. gem追加
3. docker-compose exec api bundle install
4. docker attach コンテナid

```
gem 'pry-rails'
gem 'pry-byebug'
gem 'rack-cors'
```

#### frontend
1. docker compose exec front bash(コンテナ内に入る)
2. npx create-react-app . --template typescript
3. npm install react-router-dom@6
4. npm install axios --save
5. npm start
6. localhost:3000にアクセス
