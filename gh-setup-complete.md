# 🚀 GitHub CLI (gh) セットアップ完了

## ✅ インストール状況

GitHub CLI v2.86.0 が正常にインストールされました！

```
gh version 2.86.0 (2026-01-21)
https://github.com/cli/cli/releases/tag/v2.86.0
```

## 📍 インストール場所

- **実行ファイル**: `/c/Users/simia/bin/gh.exe`
- **PATH設定**: 自動的に追加済み
- **アクセス**: `gh` コマンドでどこからでも利用可能

## 🔐 認証設定

### 現在の状態
- インストール: ✅ 完了
- 認証: ⏳ 要完了

### 認証手順

1. **ワンタイムコードをコピー**: `E28E-9867`

2. **ブラウザで以下のURLを開く**:
   ```
   https://github.com/login/device
   ```

3. **認証手順**:
   - GitHubにログイン
   - ワンタイムコードを入力: `E28E-9867`
   - デバイスの認証を許可

4. **認証確認**:
   ```bash
   gh auth status
   ```

## 🛠 基本的な使い方

### リポジトリ情報の確認
```bash
gh repo view Bubu1029/Bubu1029.github.io
```

### Issues管理
```bash
gh issue list
gh issue create --title "新機能追加" --body "詳細説明"
```

### Pull Request作成
```bash
gh pr create --title "機能追加" --body "変更内容の説明"
```

### GitHub Pages設定
```bash
gh api repos/Bubu1029/Bubu1029.github.io/pages
```

### リリース管理
```bash
gh release list
gh release create v1.0.0 --title "Initial Release"
```

## 📚 よく使うコマンド

### プロジェクト管理
```bash
# リポジトリのクローン
gh repo clone Bubu1029/Bubu1029.github.io

# フォーク作成
gh repo fork owner/repo

# リポジトリ作成
gh repo create my-new-repo --public
```

### CI/CD管理
```bash
# GitHub Actions確認
gh run list

# ワークフロー実行
gh workflow run deploy.yml
```

### 統計情報
```bash
# リポジトリ統計
gh api repos/Bubu1029/Bubu1029.github.io --jq '.stargazers_count'

# コントリビューター情報
gh api repos/Bubu1029/Bubu1029.github.io/contributors
```

## 🔄 次のステップ

1. **ブラウザ認証を完了** (コード: `E28E-9867`)
2. **認証状態確認**: `gh auth status`
3. **基本コマンドテスト**: `gh repo view Bubu1029/Bubu1029.github.io`

## 💡 便利な設定

### エディター設定
```bash
gh config set editor "code --wait"  # VS Code
gh config set editor vim            # Vim
```

### デフォルトプロトコル
```bash
gh config set git_protocol https
```

## 🎉 これで準備完了！

GitHub CLIを使ってポートフォリオサイトの管理がより効率的になります。
- Issue管理
- Pull Request作成
- GitHub Pages設定
- 自動化ワークフローの実行

認証を完了すれば、すべての機能が利用可能になります！