# 📋 GitHub Issues テンプレート集

以下の内容をコピー&ペーストして、GitHub Issues に登録してください。
各Issueは独立しているため、順次作成できます。

---

## Issue #1: GitHub CLI認証を完了する

**Labels:** `setup`, `authentication`
**Priority:** High
**Assignee:** 自分

### 概要
GitHub CLI (gh) のインストールは完了しているが、認証が未完了のため、リポジトリ操作やIssue管理ができない。

### 完了条件
- [ ] ブラウザで https://github.com/login/device にアクセス
- [ ] ワンタイムコード `E28E-9867` を入力
- [ ] デバイス認証を許可
- [ ] `gh auth status` で認証成功を確認
- [ ] `gh repo view Bubu1029/Bubu1029.github.io` でテスト実行

### 技術メモ
- GitHub CLI v2.86.0 インストール済み
- PATH設定完了済み
- 認証コード: `E28E-9867`

---

## Issue #2: X(Twitter)投稿の実際の埋め込み作業

**Labels:** `content`, `social-media`, `enhancement`
**Priority:** Medium
**Assignee:** 自分

### 概要
現在はプレースホルダーテキストのX投稿埋め込み枠があるが、実際の投稿に差し替える必要がある。

### 完了条件
- [ ] AI関連の投稿を3つ選定
- [ ] 各投稿の埋め込みコードを取得
- [ ] `index.html`の該当セクション更新
- [ ] `portfolio.html`にも同様の更新適用
- [ ] 表示確認とレスポンシブテスト

### 参考情報
- X Profile: https://x.com/BuBu_AIIlust
- 埋め込みガイド: `x-embed-guide.md`

### 関連ファイル
- `index.html` (🐦 X Posts セクション)
- `portfolio.html`
- `x-embed-guide.md`

---

## Issue #3: 実際のAIイラスト作品画像への差し替え

**Labels:** `content`, `gallery`, `enhancement`
**Priority:** Medium
**Assignee:** 自分

### 概要
現在はプレースホルダー画像を使用しているが、実際のAI作品画像に差し替えて視覚的魅力を向上させる。

### 完了条件
- [ ] AI作品画像を4-6点選定
- [ ] 適切なサイズに最適化（400x200px推奨）
- [ ] Gitリポジトリにアップロード（`/images/`フォルダ）
- [ ] ギャラリーセクションの画像パス更新
- [ ] 各作品の説明文を実際の内容に更新
- [ ] Open Graph画像の設定

### 技術要件
- 画像形式: WebP推奨（fallback: JPEG）
- レスポンシブ対応
- 適切なalt属性設定
- ファイルサイズ最適化（50KB以下推奨）

### 関連ファイル
- `index.html` (Gallery セクション)
- `portfolio.html`

---

## Issue #4: 各プロジェクトの詳細ページを作成

**Labels:** `feature`, `content`, `documentation`
**Priority:** Low
**Assignee:** 自分

### 概要
現在のプロジェクトカードは概要のみのため、詳細な技術情報や成果を紹介するページを作成する。

### 完了条件
- [ ] `project-rag-chatbot.html` - RAG就業規則チャットボット詳細ページ
- [ ] `project-local-llm.html` - ローカルLLM環境構築詳細ページ
- [ ] 各ページに技術構成図やスクリーンショット追加
- [ ] メインページからのリンク設定

### 含めるべき内容
- プロジェクト概要・背景
- 技術的課題と解決方法
- アーキテクチャ図・システム構成図
- 成果・効果測定・KPI
- 学んだこと・今後の展開
- 使用技術スタック詳細

### 関連ファイル
- `index.html` (プロジェクトカードのリンク更新)
- `portfolio.html` (プロジェクトカードのリンク更新)

---

## Issue #5: 技術ブログの継続的更新システム構築

**Labels:** `blog`, `automation`, `feature`
**Priority:** Medium
**Assignee:** 自分

### 概要
現在は単発のブログ記事だが、継続的な技術情報発信のためのブログシステムを構築する。

### 完了条件
- [ ] `blog-index.html` - ブログ記事一覧ページ作成
- [ ] `blog/nvidia-gpu-evaluation.html` - NVIDIA GPU評価結果の詳細記事
- [ ] `blog/system-architect-prep.html` - システムアーキテクト試験準備記事
- [ ] `blog/mcp-research.html` - MCP調査結果記事
- [ ] 記事間のナビゲーション実装
- [ ] RSS配信設定（GitHub Pages対応）

### 技術要件
- 静的サイト生成対応
- 記事カテゴリ分類（AI/LLM, 制御システム, 転職活動）
- 検索機能（クライアントサイド JavaScript）
- ソーシャルシェア機能

### 関連ファイル
- `blog.html` (既存記事)
- `blog-index.html` (新規作成)

---

## Issue #6: ポートフォリオサイトの採用効果測定

**Labels:** `analytics`, `career`, `data`
**Priority:** Medium
**Assignee:** 自分

### 概要
ポートフォリオサイトが転職活動にどの程度効果があるかを測定・分析する。

### 完了条件
- [ ] Google Analytics 4 設定
- [ ] 主要ページの訪問数測定
- [ ] 参照元分析（LinkedIn、X、直接アクセス等）
- [ ] 採用担当者からのフィードバック収集
- [ ] 履歴書・職務経歴書への効果的な記載方法確立
- [ ] 月次レポート作成フォーマット

### 分析観点
- アクセス数・セッション時間・直帰率
- デバイス別アクセス傾向（PC/スマホ/タブレット）
- 最も閲覧されるセクション
- コンバージョン率（問い合わせ・X フォロー等）

### 関連ファイル
- 全HTML ファイル（Analytics タグ追加）

---

## Issue #7: グローバル企業向け英語版ポートフォリオ作成

**Labels:** `i18n`, `career`, `enhancement`
**Priority:** Low
**Assignee:** 自分

### 概要
外資系企業やグローバル企業への転職を視野に入れ、英語版ポートフォリオを作成する。

### 完了条件
- [ ] `index-en.html` の作成
- [ ] `portfolio-en.html` の作成
- [ ] `README-en.md` の作成
- [ ] 技術用語の適切な英訳
- [ ] 文化的な表現の調整
- [ ] 言語切り替え機能
- [ ] 英語圏での一般的なポートフォリオ形式に合わせた調整

### 翻訳留意点
- 「制御エンジニア」→ "Control Systems Engineer"
- 日本特有の企業文化・実績を分かりやすく説明
- GitHub Pages での多言語対応
- SEO 対応（hreflang 設定）

### 関連ファイル
- `index.html` (言語切り替えボタン追加)
- `portfolio.html` (言語切り替えボタン追加)

---

## Issue #8: Lighthouse スコア95+を目指したパフォーマンス最適化

**Labels:** `performance`, `optimization`, `enhancement`
**Priority:** Medium
**Assignee:** 自分

### 概要
ポートフォリオサイトの読み込み速度とユーザー体験を向上させる。

### 完了条件
- [ ] Lighthouse Performance Score 95+ 達成
- [ ] 画像の最適化（WebP対応・次世代フォーマット）
- [ ] CSS の最小化・最適化・Critical CSS 抽出
- [ ] JavaScript の遅延読み込み・コード分割
- [ ] Web フォントの最適化（font-display: swap）
- [ ] CDN の活用検討

### 技術要件
- Core Web Vitals 改善（LCP, FID, CLS）
- PWA 対応検討
- オフライン表示対応
- キャッシュ戦略最適化

### 測定ツール
- Lighthouse CI
- PageSpeed Insights
- WebPageTest

### 関連ファイル
- 全HTML ファイル
- CSS ファイル（最適化）
- 画像ファイル（圧縮・変換）

---

## Issue #9: セキュリティ設定とプライバシー保護の強化

**Labels:** `security`, `privacy`, `enhancement`
**Priority:** Medium
**Assignee:** 自分

### 概要
個人情報保護とセキュリティ強化のためのベストプラクティスを適用する。

### 完了条件
- [ ] Content Security Policy (CSP) 設定
- [ ] HTTPS 強制リダイレクト（GitHub Pages設定）
- [ ] `privacy-policy.html` - プライバシーポリシー作成
- [ ] 外部リンクの `rel="noopener"` 設定
- [ ] 不要な個人情報の削除・匿名化
- [ ] GitHub Secrets の適切な管理

### セキュリティチェック項目
- XSS 対策（CSP, サニタイズ）
- 機密情報の露出チェック
- 依存関係の脆弱性スキャン
- アクセスログの分析

### 関連ファイル
- 全HTML ファイル（CSP メタタグ追加）
- `privacy-policy.html` (新規作成)

---

# 📝 Issue 作成手順

## 1. 認証完了後の Issue 作成方法

```bash
# 認証完了後、以下のコマンドで Issue を一括作成可能
gh issue create --title "GitHub CLI認証を完了する" --body-file issue-templates/issue-01.md --label "setup,authentication"
```

## 2. Web UI での作成方法

1. https://github.com/Bubu1029/Bubu1029.github.io/issues にアクセス
2. 「New Issue」をクリック
3. 上記のテンプレートをコピー&ペースト
4. 適切なラベルを設定
5. 「Submit new issue」をクリック

## 3. 優先度順の推奨作成順序

1. **Issue #1** - GitHub CLI認証（即座に実行）
2. **Issue #2** - X投稿埋め込み（今週中）
3. **Issue #3** - AI作品画像（今週中）
4. **Issue #6** - 効果測定（2週間以内）
5. **Issue #5** - ブログシステム（2週間以内）
6. **Issue #8** - パフォーマンス最適化（2週間以内）
7. **Issue #9** - セキュリティ強化（1ヶ月以内）
8. **Issue #4** - 詳細ページ（1ヶ月以内）
9. **Issue #7** - 英語版（1ヶ月以内）

---

**📋 これらの Issue を順次実装することで、ポートフォリオサイトが転職活動の強力な武器として完成します！**