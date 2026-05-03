# Portfolio9
ポートフォリオ用GitHubです。

## アプリ概要
Next.jsとSupabaseを用いた趣味のイベント等のスケジュール管理アプリです。

## サイトイメージ
![アプリ画像](https://github.com/mai-s419/portfolio9/blob/c8fa77959ee2bac9aee3a1494f50c3ef7f4d40dd/docs/%E3%82%A4%E3%83%A1%E3%83%BC%E3%82%B8%E7%94%BB%E5%83%8F.png?raw=true)

## サイトURL  
https://calendar-app-beta-brown.vercel.app
- 画面中部の『Continue as Guest』ボタンから、メールアドレスとパスワードを入力せずにログインできます。

## 使用技術
- フロントエンド：Next.js 15.3
- バックエンド：Next.js 15.3、~Python 3.13.3（FastAPI0.115.12）~
- データベース：Supabase
- デプロイ：Vercel
- バージョン管理：Git、GitHub
- テスト・デバッグ：DevTools（Chrome）
- CI/CD：GitHub Actions（ESLint）

## 設計ドキュメント
[要件定義・基本設計・詳細設計の一覧_Googleスプレッドシート](https://docs.google.com/spreadsheets/d/1f-_8Aa_L2etDloKb86AdRKEppvwO9TMyVad2Mhhba5U/edit?usp=sharing)

詳細設計時のワイヤーフレーム、ER図、ワークフロー図の画像はdocsディレクトリに格納しています。（[こちらからアクセス](./docs)）

## 機能一覧
- ユーザー登録、ログイン機能（Supabase Authを利用）
- イベントの追加、編集、削除機能
   - 同イベントに紐づく複数日程の登録が可能
- 重要日程の優先表示機能
- カレンダー表示機能（月表示）
- メモ機能

## テスト・修正の設計及び実施書
[テスト・修正の設計及び実施書_Googleスプレッドシート](https://docs.google.com/spreadsheets/d/1ph7XaLu4a2k_kDBEpj_ySTBPETJvg5143ZMk5G90DUA/edit?usp=sharing)

## アプリの改善案
[アプリの改善案_Googleスプレッドシート](https://docs.google.com/spreadsheets/d/1fgynpBKhx8zaNkMweeYVQl52bP6Z8dJZOmmY8MHXjQM/edit?usp=sharing)

## 備考
[ESLintの実行結果_GitHub Actions](https://github.com/aihat9161/PortfolioExample_Next.js_BlogAppWorX_ENGINEER-CLASS/actions/runs/14956271682/job/42012343864)

- 活用した生成AIとその用途
  - ChatGPT：要件定義、設計、各種リサーチ
  - v0：アプリのモック作成
  - GitHub Copilot Chat：ローカル環境でのコードの修正相談

- リファクタリングの規則
  - 2つ以上のファイルで使う、行数が10以上のUIコンポーネントはcomponentsフォルダに移行
  - 2つ以上のファイルで使う、行数が10以上の関数はlibフォルダに移行
  - 変数名で2つ以上の単語が入る場合は、「isPublished」のように二つ目以降の単語の頭を大文字とする
