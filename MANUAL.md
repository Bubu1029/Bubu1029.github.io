# Portfolio Site Management Manual

Bubu1029.github.io - ポートフォリオサイト構築・管理マニュアル

---

## 1. プロジェクト概要

| 項目 | 内容 |
|------|------|
| サイトURL | https://bubu1029.github.io |
| リポジトリ | https://github.com/Bubu1029/Bubu1029.github.io |
| X(Twitter) | https://x.com/BuBu_AIIlust |
| ホスティング | GitHub Pages (無料) |
| デプロイ方法 | mainブランチへのpushで自動デプロイ (GitHub Actions) |
| 作成日 | 2026年2月14日 |

---

## 2. ファイル構成

```
Bubu1029.github.io/
├── index.html              # メインポートフォリオ (ダークテーマ)
├── portfolio.html           # スタイリッシュ版 (サイバーパンク風)
├── blog.html                # 開発記録ブログ
├── daily-summary.html       # 作業完了レポート (2/14)
├── README.md                # GitHubプロフィール用Markdown
├── CLAUDE.md                # Claude Code自動応答設定
├── Agents.md                # AIエージェント自動実行設定
├── x-embed-guide.md         # X埋め込み機能の使用ガイド
├── gh-setup-complete.md     # GitHub CLIセットアップ記録
├── github-issues-templates.md # Issue テンプレート集
├── issues-todo.md           # Issue一覧 (TODO管理)
├── 20260214.md              # 2/14 作業記録
├── LICENSE
└── .github/
    └── workflows/
        └── static.yml       # GitHub Pages自動デプロイ設定
```

---

## 3. 実施した作業一覧

### 3.1 ポートフォリオサイト構築

#### index.html (メインサイト)
- ダークテーマのモダンなシングルページポートフォリオ
- セクション構成: Hero / Skills / Experience Timeline / Projects / Contact
- カスタムカーソル、パーティクルアニメーション (Canvas API)
- スクロール連動フェードインアニメーション (Intersection Observer)
- レスポンシブデザイン (モバイル対応)

#### portfolio.html (サイバーパンク版)
- index.htmlと同じ構造・内容で別デザイン
- グラスモーフィズム (backdrop-filter: blur) 採用

#### README.md (GitHubプロフィール)
- shields.ioバッジによるTech Stack表示
- Career Highlights / Featured Projects / Certifications
- GitHub Stats画像埋め込み

### 3.2 ブログ・レポート作成

| ファイル | 内容 |
|---------|------|
| blog.html | 開発プロセスの記録。技術選定・デザイン方針・使用技術の詳細 |
| daily-summary.html | 2/14の作業完了レポート。統計・成果・ファイル一覧・次ステップ |
| 20260214.md | Markdown形式の作業記録。タスク完了状況・KPI・学び |

### 3.3 X(Twitter)埋め込み機能

x-embed-guide.mdに詳細手順を記載。概要:

1. 埋め込みたいツイートをXで開く
2. 「...」メニュー > 「ツイートを埋め込む」を選択
3. 生成された `<blockquote>` コードをコピー
4. index.htmlの該当箇所に貼り付け
5. GitHubにpush → 自動デプロイ

埋め込みコードのテンプレート:
```html
<blockquote class="twitter-tweet" data-theme="light" data-width="350">
    <p lang="ja" dir="ltr">ツイート内容</p>
    <a href="https://x.com/BuBu_AIIlust/status/ツイートID">@BuBu_AIIlust</a>
</blockquote>
```

Twitter Widgetsスクリプト (HTML末尾に必要):
```html
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
```

### 3.4 Claude Code自動化設定

#### CLAUDE.md
- X/Twitter URL検出時の自動埋め込み処理ルール
- ポートフォリオ自動更新のトリガー条件と手順
- 技術スタック情報・キャリア目標のコンテキスト

#### Agents.md
- `x-embed-manager`: X投稿の自動埋め込み管理
- `portfolio-optimizer`: ポートフォリオの継続的最適化

### 3.5 GitHub CLI (gh) セットアップ

gh-setup-complete.mdに詳細を記載。

- GitHub CLI v2.86.0 をインストール
- 実行ファイル: `/c/Users/simia/bin/gh.exe`
- 認証: ブラウザ認証方式 (https://github.com/login/device)

基本コマンド:
```bash
gh auth status              # 認証状態確認
gh repo view                # リポジトリ情報
gh issue list               # Issue一覧
gh issue create --title "..." --body "..."  # Issue作成
gh pr create --title "..." --body "..."     # PR作成
```

### 3.6 GitHub Actions (CI/CD)

`.github/workflows/static.yml` で自動デプロイを設定済み:
- mainブランチへのpushをトリガーにGitHub Pagesへデプロイ
- `actions/checkout@v4` → `actions/configure-pages@v5` → `actions/upload-pages-artifact@v3` → `actions/deploy-pages@v4`

### 3.7 Issue管理の整備

github-issues-templates.mdに9件のIssueテンプレートを用意:

| # | タイトル | 優先度 |
|---|---------|--------|
| 1 | GitHub CLI認証を完了する | High |
| 2 | X投稿の実際の埋め込み作業 | Medium |
| 3 | AIイラスト作品画像への差し替え | Medium |
| 4 | プロジェクト詳細ページの作成 | Low |
| 5 | 技術ブログの継続的更新システム構築 | Medium |
| 6 | ポートフォリオサイトの採用効果測定 | Medium |
| 7 | 英語版ポートフォリオ作成 | Low |
| 8 | Lighthouseスコア95+パフォーマンス最適化 | Medium |
| 9 | セキュリティ設定とプライバシー保護 | Medium |

---

## 4. 技術仕様

### 4.1 使用技術

| カテゴリ | 技術 |
|---------|------|
| マークアップ | HTML5 |
| スタイル | CSS3 (Grid, Flexbox, Animations, Custom Properties) |
| スクリプト | JavaScript ES6+ (Canvas API, Intersection Observer) |
| フォント | Google Fonts (Inter, Space Grotesk) |
| アイコン | Font Awesome 6.4.0 |
| バッジ | shields.io |
| 外部API | Twitter Widgets JS |
| ホスティング | GitHub Pages |
| CI/CD | GitHub Actions |
| CLI | GitHub CLI (gh) |

### 4.2 デザイン仕様

カラーパレット:
```
プライマリ: #667eea (ブルーパープル)
セカンダリ: #764ba2 (ディープパープル)
アクセント:  #4facfe / #00f2fe (シアン系)
テキスト:   #1a1a2e (ダーク) / #8892b0 (ライト)
背景:      #0c0c0c → #1a1a2e (ダークグラデーション)
```

レスポンシブブレークポイント:
- 768px以下: モバイル対応 (ナビ非表示, 1カラムグリッド)

### 4.3 サイト構造 (index.html / portfolio.html)

```
nav          固定ナビゲーションバー (ブラーエフェクト)
#home        Hero セクション (フローティングカード3枚)
#skills      技術スキル (4カテゴリ: AI/LLM, Control, System, GPU)
#experience  キャリアタイムライン (2期間)
#projects    プロジェクトカード (3件)
#contact     連絡先・SNSリンク
footer       コピーライト
```

---

## 5. 運用手順

### 5.1 コンテンツ更新の流れ

```
1. ローカルでファイルを編集
2. git add <変更ファイル>
3. git commit -m "変更内容"
4. git push origin main
5. GitHub Actionsが自動デプロイ (数分で反映)
```

### 5.2 新しいプロジェクトを追加する

index.html の `#projects` セクション内 `.projects-grid` に以下を追加:

```html
<div class="project-card fade-in">
    <div class="project-image">
        <i class="fas fa-アイコン名"></i>
    </div>
    <div class="project-content">
        <h3 class="project-title">プロジェクト名</h3>
        <p class="project-desc">説明文</p>
        <div class="project-tech">
            <span class="tech-tag">技術1</span>
            <span class="tech-tag">技術2</span>
        </div>
        <div class="project-links">
            <a href="リンクURL" class="project-link">
                <i class="fas fa-external-link-alt"></i>
                詳細を見る
            </a>
        </div>
    </div>
</div>
```

### 5.3 スキルタグを追加する

index.html の `#skills` セクション内、該当カテゴリの `.skill-items` に追加:

```html
<span class="skill-tag">新しいスキル名</span>
```

### 5.4 キャリア経歴を追加する

index.html の `.timeline` 内に追加:

```html
<div class="timeline-item fade-in">
    <div class="timeline-content">
        <div class="timeline-date">期間</div>
        <h3 class="timeline-title">役職・タイトル</h3>
        <p class="timeline-desc">説明文</p>
    </div>
    <div class="timeline-marker"></div>
</div>
```

### 5.5 README.mdの同期更新

index.htmlを更新した場合、README.mdの対応セクションも手動で同期する:
- Tech Stack → shields.ioバッジを追加/更新
- Career Highlights → テキストを更新
- Featured Projects → プロジェクト情報を更新
- Certifications → 資格情報を更新

---

## 6. 未完了タスク (次のステップ)

### 優先度: 高
- [ ] GitHub CLI認証の完了
- [ ] X投稿の実際の埋め込み (現在プレースホルダー)

### 優先度: 中
- [ ] AIイラスト作品画像の実装 (現在プレースホルダー)
- [ ] Google Analytics導入
- [ ] ブログシステム拡張 (記事一覧ページ, カテゴリ分類)
- [ ] Lighthouseスコア最適化
- [ ] セキュリティ強化 (CSP, noopener設定)

### 優先度: 低
- [ ] 各プロジェクトの詳細ページ作成
- [ ] 英語版ポートフォリオ作成
- [ ] PWA対応

---

## 7. トラブルシューティング

### デプロイされない
1. GitHub Actionsの実行状況を確認: リポジトリ > Actions タブ
2. mainブランチにpushされているか確認: `git log --oneline -5`
3. GitHub Pagesの設定確認: Settings > Pages > Source が GitHub Actions になっているか

### X埋め込みが表示されない
1. Twitter Widgetsスクリプトが `</body>` 前に読み込まれているか確認
2. `<blockquote>` 内のURL形式が正しいか確認
3. 埋め込み対象のツイートが公開状態か確認
4. ブラウザの広告ブロッカーが無効か確認

### レスポンシブが崩れる
1. `<meta name="viewport" content="width=device-width, initial-scale=1.0">` が `<head>` 内にあるか確認
2. Chrome DevToolsのデバイスモードで各ブレークポイントをテスト
3. `.container` の `max-width` 設定を確認
