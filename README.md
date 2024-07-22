# ソーシャルメディアアプリケーション

ソーシャルメディアアプリケーションへようこそ！このアプリは、ユーザーが投稿を作成し、他のユーザーをフォローし、投稿にいいねやコメントをすることができるシンプルなソーシャルメディアプラットフォームです。

## 目次

- [インストール](#インストール)
- [使用方法](#使用方法)
- [API ドキュメント](#api-ドキュメント)
- [コントリビューション](#コントリビューション)
- [ライセンス](#ライセンス)

## インストール

1. **リポジトリをクローンする:**

   ```bash
   git clone https://github.com/yourusername/social-media-app.git
   cd social-media-app
   ```

2. **依存関係をインストールする:**

   ```bash
   npm install
   ```

3. **環境変数を設定する:**

   ルートディレクトリに `.env` ファイルを作成し、必要な環境変数を追加します。例:

   ```env
   DATABASE_URL=your_database_url
   JWT_SECRET=your_jwt_secret
   ```

4. **データベースのマイグレーションを実行する:**

   ```bash
   npm run migrate
   ```

5. **アプリケーションを起動する:**

   ```bash
   npm start
   ```

   アプリケーションは `http://localhost:3000` で動作します。

## 使用方法

アプリケーションが起動したら、ウェブインターフェースや提供された API を通じてソーシャルメディアプラットフォームと対話できます。

### ウェブインターフェース

ブラウザを開き、`http://localhost:3000` にアクセスしてウェブインターフェースを利用します。

### API

アプリケーションとはプログラム経由でも API を使って対話することができます。主なエンドポイントは以下の通りです:

- **ユーザー:**

  - `GET /users` - ユーザーの一覧を取得
  - `POST /users` - 新しいユーザーを作成
  - `GET /users/{id}` - 特定のユーザーを取得
  - `PUT /users/{id}` - ユーザーを更新
  - `DELETE /users/{id}` - ユーザーを削除

- **投稿:**

  - `GET /posts` - 投稿の一覧を取得
  - `POST /posts` - 新しい投稿を作成
  - `GET /posts/{id}` - 特定の投稿を取得
  - `PUT /posts/{id}` - 投稿を更新
  - `DELETE /posts/{id}` - 投稿を削除

- **コメント:**

  - `GET /posts/{post_id}/comments` - 特定の投稿に対するコメントの一覧を取得
  - `POST /posts/{post_id}/comments` - 投稿にコメントを追加
  - `GET /comments/{comment_id}` - 特定のコメントを取得
  - `PUT /comments/{comment_id}` - コメントを更新
  - `DELETE /comments/{comment_id}` - コメントを削除

- **いいね:**

  - `GET /posts/{post_id}/likes` - 特定の投稿に対するいいねの一覧を取得
  - `POST /posts/{post_id}/likes` - 投稿にいいねを追加
  - `DELETE /posts/{post_id}/likes` - 投稿のいいねを削除

- **フォロー:**
  - `GET /users/{user_id}/followers` - 特定のユーザーのフォロワー一覧を取得
  - `GET /users/{user_id}/following` - 特定のユーザーがフォローしているユーザーの一覧を取得
  - `POST /users/{user_id}/follow` - ユーザーをフォロー
  - `DELETE /users/{user_id}/follow` - ユーザーのフォローを解除

## コントリビューション

貢献を歓迎します！バグ報告、新機能の提案、プルリクエストはお気軽に行ってください。

## ライセンス

このプロジェクトは [MIT ライセンス](LICENSE) の下でライセンスされています。
