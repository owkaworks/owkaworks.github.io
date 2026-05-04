# OWKA WORKS — ホームページ

GitHub Pages で公開するポートフォリオサイトです。

## ファイル構成

```
├── index.html            # トップページ（アプリ一覧・About・お問い合わせ）
├── privacy-policy.html   # プライバシーポリシー（バス遅延通知アプリ）
└── README.md             # このファイル
```

## GitHub Pages で公開する手順

### 1. GitHubリポジトリを作成

GitHub（https://github.com）で新しいリポジトリを作成します。

- リポジトリ名: `ユーザー名.github.io`（ユーザーサイトの場合）  
  または任意の名前（例: `owka-works`、プロジェクトサイトの場合）
- Public に設定
- 他のオプションはデフォルトのまま

### 2. ファイルをプッシュ

```bash
cd owka-works-site
git init
git add .
git commit -m "初回公開"
git branch -M main
git remote add origin https://github.com/ユーザー名/リポジトリ名.git
git push -u origin main
```

### 3. GitHub Pages を有効化

1. GitHubでリポジトリのページを開く
2. **Settings** → 左メニュー **Pages**
3. Source を **Deploy from a branch** に設定
4. Branch を **main** / **/ (root)** に設定
5. **Save** をクリック

### 4. 公開URLを確認

数分後に以下のURLでアクセスできます:

- ユーザーサイト: `https://ユーザー名.github.io`
- プロジェクトサイト: `https://ユーザー名.github.io/リポジトリ名/`

## カスタマイズ方法

### アプリを追加する

`index.html` の `<!-- Coming Soon -->` の**前**に、以下のテンプレートを追加:

```html
<div class="app-card fade-in">
  <div class="app-card-visual" style="background: linear-gradient(135deg, #色1, #色2);">
    <span class="app-icon">絵文字</span>
    <span class="app-badge">Android</span>
  </div>
  <div class="app-card-body">
    <h3>アプリ名</h3>
    <p class="app-subtitle">説明文</p>
    <div class="app-features">
      <span>機能1</span>
      <span>機能2</span>
    </div>
    <div class="app-card-links">
      <a href="URL">Google Play</a>
      <a href="privacy-policy-アプリ名.html">プライバシーポリシー</a>
    </div>
  </div>
</div>
```

### プライバシーポリシーを追加する

`privacy-policy.html` をコピーして `privacy-policy-アプリ名.html` を作成し、内容を書き換えてください。

### Google Play / App Store 公開後

`index.html` 内の以下のコメントを解除して、ストアURLを設定:

```html
<!-- <a href="#">Google Play</a> -->
```

↓

```html
<a href="https://play.google.com/store/apps/details?id=パッケージ名">Google Play</a>
```

## TODO（公開前チェックリスト）

- [ ] メールアドレスの確認（owkaworks@gmail.com で公開してよいか）
- [ ] X（Twitter）アカウントURLの設定
- [ ] Google Play 公開後にストアリンクを追加
- [ ] 必要に応じて独自ドメインを設定（Settings → Pages → Custom domain）
