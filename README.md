# 和美商事 WABI Trading Website

日本の伝統工芸品を海外に販売するビジネス向けの多言語対応Webサイト

## ファイル構成

```
├── index.html          # 日本語版メインページ
├── index-en.html       # 英語版メインページ
├── thank-you.html      # お問い合わせ完了ページ
└── README.md          # このファイル
```

## 特徴

- **レスポンシブデザイン**: スマートフォン・タブレット・PC対応
- **多言語対応**: 日本語・英語の2言語
- **和風デザイン**: 茶色と金色を基調とした日本らしいデザイン
- **動作するお問い合わせフォーム**: Formspreeを使用
- **SEO対策**: メタタグ・構造化データ対応

## お問い合わせフォームの設定

お問い合わせフォームを実際に動作させるには、以下の手順でFormspreeの設定が必要です：

### 1. Formspreeアカウントの作成
1. [Formspree.io](https://formspree.io) にアクセス
2. 無料アカウントを作成（月50件まで無料）

### 2. フォームの作成
1. ダッシュボードで「+ New Form」をクリック
2. Form name: `WABI Trading Contact Form`
3. 作成されたフォームIDをコピー (例: `abc123def`)

### 3. HTMLファイルの修正
以下の2つのファイルでフォームIDを置き換えてください：

**index.html** (日本語版)
```html
<!-- 行483付近 -->
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```
↓
```html
<form class="contact-form" action="https://formspree.io/f/abc123def" method="POST">
```

**index-en.html** (英語版)
```html
<!-- 同じ箇所 -->
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```
↓
```html
<form class="contact-form" action="https://formspree.io/f/abc123def" method="POST">
```

### 4. 動作確認
1. Webサイトをサーバーにアップロード
2. フォームからテスト送信
3. 初回送信時はFormspreeの認証画面が表示されるので確認をクリック
4. 設定したメールアドレスにお問い合わせが届くことを確認

## GitHub Pagesでの公開手順

1. GitHubアカウントでログイン
2. 新しいリポジトリを作成 (`wabi-trading-website` など)
3. `index.html`, `index-en.html`, `thank-you.html` をアップロード
4. Settings > Pages で「Deploy from a branch」を選択
5. Branch: `main` を選択して Save
6. 数分後に `https://[ユーザー名].github.io/[リポジトリ名]/` でアクセス可能

## カスタマイズ

### 会社情報の変更
- **会社名**: HTMLファイル内の「和美商事」「WABI Trading」を変更
- **連絡先**: フッター部分の住所・電話番号・メールアドレスを変更
- **商品情報**: 商品セクションの内容を実際の取扱商品に変更

### デザインの変更
CSSの以下の部分を変更することでカラーテーマを調整できます：
- メインカラー: `#d4af37` (金色)
- ダークカラー: `#2c1810` (茶色)
- 背景色: `#f8f6f0` (ベージュ)

### SEOの最適化
- title タグとmeta description の内容を実際のビジネスに合わせて変更
- 画像のalt属性を追加
- 構造化データの追加を検討

## トラブルシューティング

### フォームが動作しない場合
1. FormspreeのフォームIDが正しく設定されているか確認
2. HTTPSでアクセスしているか確認（HTTPでは動作しません）
3. ブラウザのコンソールでエラーが出ていないか確認

### レスポンシブデザインの問題
- 各デバイスでの表示確認
- CSSのメディアクエリの調整

## ライセンス

このテンプレートは自由に使用・改変していただけます。商用利用も可能です。

## サポート

技術的な質問やカスタマイズのご相談は、GitHubのIssuesまたはお問い合わせフォームからご連絡ください。