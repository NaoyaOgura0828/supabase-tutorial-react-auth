# supabase-tutorial-react-auth
[Supabase](https://supabase.com/)の[公式Reactチュートリアル](https://supabase.com/docs/guides/getting-started/tutorials/with-react)。<br>
基本的なユーザー管理アプリを構築する。以下の機能が含まれる。
- Supabase Database: ユーザーデータを格納するためのPostgresデータベース。
- Supabase Auth: ユーザーはマジックリンク(パスワードなし、電子メールアドレスのみ)でサインインできます。
- Supabase Storage: ユーザーは写真をアップロードできます。
- Row Level Security: データは保護されているため、個人は自分のデータにのみアクセスできます。
- Instant APIs: データベーステーブルを作成すると、APIが自動的に生成されます。

<br>

# Requirement
Fedora37ローカル環境上のDocker環境内で実行確認済。<br>
また、Reactは以下のバージョンで実行確認済。

```bash
$ node -v
v19.3.0

$ npm -v
9.2.0

$ yarn -v
1.22.19
```

<br>

# Installation
## プロジェクトを作成する
1. [app.supabase.com](https://app.supabase.com/projects)にアクセスする。
2. `New project`をクリックする。
3. プロジェクトの詳細を入力する。
4. 新しいデータベースが起動するまで待つ。

<br>

## データベーススキーマを設定する
1. ダッシュボードの[SQL Editor](https://app.supabase.com/project/_/sql)ページに移動する。
2. `User Management Starter`をクリックする。
3. `Run`をクリックする。

<br>

## APIキーを取得する
1. ダッシュボードの[Settings](https://app.supabase.com/project/_/settings/general)ページに移動する。
2. サイドバーの`API`をクリックする。
3. このページで`API URL`, `anon`, `service_role`を取得する。

<br>

## Repositoryをクローンする
git cloneコマンドで本Repositoryを任意のディレクトリ配下にcloneする。

<br>

## 環境変数の設定
本Repository直下に`.env`ファイルを作成し、以下のとおり設定する。

```conf
REACT_APP_SUPABASE_URL = ${プロジェクトURL} # API Settings で取得したProject URL
REACT_APP_SUPABASE_ANON_KEY = ${APIプロジェクトキーanon} # Project API keys で取得したanon
```

<br>

## パッケージをインストールする
本Repository直下で以下のコマンドを実行する。

```bash
# パッケージをインストールする
$ yarn install
```

<br>

# Usage
本Repository直下で以下のコマンドを実行する。

```bash
$ yarn start
```