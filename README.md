# NEXTPARTS 商品DB入力アプリ

Supabase（NEXTPARTSプロジェクト）への商品データ入力用Webアプリ。

## メンバーがアクセスするURL（本番）
https://aprecia.github.io/nextparts-db-admin/

※GitHub Pagesで配信。更新は index.html を修正して git push するだけ。

## 使い方（ローカル）
index.html をブラウザで開くだけでも使えます（要ログイン）。

## 公開する場合（Vercel）
```
cd /Users/mizutani/NEXTPARTS-DB-ADMIN
vercel --prod
```
※静的ファイル1枚なのでビルド設定不要。

## 利用ユーザーの追加（社内メンバー）
Supabaseダッシュボード → Authentication → Users → Add user
https://supabase.com/dashboard/project/mmdindajwedeaseadrnq/auth/users
メールアドレスとパスワードを設定して「Auto Confirm User」にチェック。

## セキュリティ
- 全テーブルにRLS設定済み（ログインユーザーのみ読み書き可）
- ページ内のキーはanonキー（公開前提のキー）のため埋込OK

## 機能
1. バリエーション登録：部品選択＋純正品番＋仕入価格 → Vコード自動採番（v+6桁）
2. 商品登録：V検索選択＋車名検索選択（ゆらぎ対応）＋型式 → 商品コード自動組立
3. 登録直後にNE出力プレビュー（商品名・売価・ヤフオクカテゴリ・キーワード）
