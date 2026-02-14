# 📝 X埋め込み機能の使用方法

## 🔧 セットアップ完了内容

あなたのポートフォリオサイトに以下のX埋め込み機能を追加しました：

### 1. 個別ツイート埋め込み (3枠)
- 特定のツイートを美しくカード形式で表示
- レスポンシブ対応のグリッドレイアウト
- ホバーエフェクト付き

### 2. タイムライン埋め込み
- あなたの最新ツイートを自動表示
- 400px高さのウィジェット
- 透明背景でサイトデザインと統合

### 3. Twitter Widgets スクリプト
- 公式のTwitter埋め込み機能を有効化
- 自動読み込み・更新対応

## 📋 使用方法

### ステップ1: 個別ツイート埋め込み

1. 埋め込みたいツイートのURLをコピー
   - 例: `https://x.com/BuBu_AIIlust/status/1234567890123456789`

2. `index.html`の以下の部分を編集：

```html
<blockquote class="twitter-tweet" data-theme="light" data-width="350">
    <p lang="ja" dir="ltr">ここに実際のツイート内容をコピー</p>
    <a href="https://x.com/BuBu_AIIlust/status/実際のツイートID">実際のツイートURL</a>
</blockquote>
```

### ステップ2: 簡単な方法（推奨）

1. X（Twitter）で埋め込みたいツイートを開く
2. 右上の「⋯」メニューをクリック
3. 「ツイートを埋め込む」を選択
4. 生成されたHTMLコードをコピー
5. `index.html`の対応する`<blockquote>`タグ全体を置き換え

### ステップ3: タイムライン設定

タイムライン埋め込みは既に設定済みです。特別な操作は不要で、自動的にあなたの最新ツイートが表示されます。

## 🎨 カスタマイズオプション

### データ属性の調整

```html
data-theme="light"     <!-- テーマ: light/dark -->
data-width="350"       <!-- 幅の指定 -->
data-height="400"      <!-- 高さの指定（タイムラインのみ） -->
data-chrome="nofooter noborders transparent" <!-- 外観オプション -->
```

### CSS スタイル調整

```css
.x-embed-container {
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    /* グリッドの列数・幅を調整 */
}

.x-embed-item {
    /* 個別カードのスタイル調整 */
}
```

## 🚀 実装例

### 例1: AI作品のツイート
```html
<blockquote class="twitter-tweet" data-theme="light" data-width="350">
    <p lang="ja" dir="ltr">新しいAI生成イラストが完成しました！🎨<br>Stable Diffusionで制作した幻想的な風景です。<br><br>#AIイラスト #StableDiffusion #デジタルアート</p>
    <a href="https://x.com/BuBu_AIIlust/status/1234567890123456789">@BuBu_AIIlust のツイート</a>
</blockquote>
```

### 例2: 技術記事のツイート
```html
<blockquote class="twitter-tweet" data-theme="light" data-width="350">
    <p lang="ja" dir="ltr">NVIDIA RTX 5070 TiでのLLM性能評価結果をブログに公開しました📊<br>70Bモデルでも快適に動作します！<br><br>詳細: https://example.com/blog <br><br>#GPU #LLM #AI開発</p>
    <a href="https://x.com/BuBu_AIIlust/status/1234567890123456790">@BuBu_AIIlust のツイート</a>
</blockquote>
```

## ⚠️ 注意事項

1. **プライバシー**: 公開ツイートのみ埋め込み可能
2. **更新**: ツイートを削除/非公開にすると埋め込みも表示されなくなります
3. **読み込み**: 初回表示時にTwitterのサーバーから読み込むため、若干の遅延があります
4. **レート制限**: 大量のツイート埋め込みは避けてください

## 🔄 更新方法

新しいツイートに更新する場合：
1. 新しいツイートの埋め込みコードを取得
2. 対応する`<blockquote>`タグを置き換え
3. GitHubにコミット・プッシュ

これで動的なX埋め込み機能が完成しました！🎉