# Task Management PWA — デプロイ手順

## 📦 ファイル構成

```
task-management-pwa/
├── index.html          ← メインアプリ
├── manifest.json       ← PWA設定
├── sw.js              ← Service Worker（オフライン対応）
└── icons/
    ├── penguin.svg     ← 元SVG
    ├── icon-72x72.png
    ├── icon-96x96.png
    ├── icon-128x128.png
    ├── icon-144x144.png
    ├── icon-152x152.png
    ├── icon-192x192.png
    ├── icon-384x384.png
    └── icon-512x512.png
```

---

## 🚀 GitHub Pages でデプロイ（無料）

### 1. GitHubアカウントを作成
https://github.com にアクセスしてアカウントを作成（既にあればスキップ）

### 2. 新しいリポジトリを作成
- GitHubで「New repository」をクリック
- Repository name: `task-management`（好きな名前でOK）
- Public を選択
- 「Create repository」をクリック

### 3. ファイルをアップロード
- リポジトリページで「uploading an existing file」をクリック
- ZIPを解凍した中身をすべてドラッグ＆ドロップ
  - `index.html`, `manifest.json`, `sw.js`, `icons/` フォルダ
- 「Commit changes」をクリック

### 4. GitHub Pages を有効化
- リポジトリの「Settings」タブ → 左メニュー「Pages」
- Source: 「Deploy from a branch」を選択
- Branch: `main`、フォルダ: `/ (root)` を選択
- 「Save」をクリック

### 5. 完成！
数分後にアクセス可能になります：
```
https://あなたのユーザー名.github.io/task-management/
```

---

## 📱 スマホにインストール

### iPhone (Safari)
1. 上記URLをSafariで開く
2. 共有ボタン（□↑）をタップ
3. 「ホーム画面に追加」をタップ
4. 「追加」をタップ → ペンギンアイコンがホーム画面に！

### Android (Chrome)
1. 上記URLをChromeで開く
2. 「ホーム画面に追加」のバナーが自動表示 or メニュー(⋮)→「アプリをインストール」
3. インストール完了 → ペンギンアイコンがホーム画面に！

---

## 🎨 カスタマイズ

### テーマカラーを変更したい場合
- `manifest.json` の `theme_color` を変更
- `index.html` の `<meta name="theme-color">` を変更

### アプリ名を変更したい場合
- `manifest.json` の `name` と `short_name` を変更

---

## ⚠️ 注意点
- PWAはHTTPS環境が必須です（GitHub Pagesは自動でHTTPS対応）
- 通知機能はアプリが開いている間のみ動作します
- データはブラウザのlocalStorageに保存されるため、ブラウザのデータを消すとタスクも消えます
