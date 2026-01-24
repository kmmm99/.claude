# claude-nippou

日報を月次ファイルに記録するClaude Codeプラグイン。作業内容をカテゴリ分類して追記します。

## インストール

```bash
/plugins install github:kmmm99/nippou-plugin
```

または、ローカルインストール:

```bash
# ~/.claude/plugins/local/ にクローン
git clone https://github.com/kmmm99/nippou-plugin ~/.claude/plugins/local/nippou-plugin
```

## 使用方法

Claude Codeで以下のコマンドを実行:

```
/nippou [作業内容]
```

### 例

```
/nippou 認証機能のバグ修正
/nippou リファクタリング作業
```

## 機能

- 月次ファイル（`nippou_yyyymm.md`）に作業内容を追記
- 日付セクション（`## yyyy-mm-dd`）で整理
- 月を跨いだ際の自動アーカイブ（`nippou_old/` に移動）
- カテゴリ分類（実装、バグ修正、リファクタリング等）

## カスタマイズ

保存先ディレクトリを変更する場合は、`commands/nippou.md` 内の以下の行を編集:

```markdown
- **ベースディレクトリ**: `~/Documents/claude-outputs/nippou/`
```

## ファイル構造

```
claude-nippou/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   └── nippou.md
└── README.md
```

## ライセンス

MIT License
