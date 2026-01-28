# nippou-plugin

日報を月次ごとにMarkdownとして記録するClaude Codeプラグイン。作業内容をカテゴリ分類して追記します。

## インストール

### マーケットプレイス経由（推奨）

```bash
# 1. マーケットプレイスを追加
/plugin marketplace add kmmm99/nippou-plugin

# 2. プラグインをインストール
/plugin install nippou@kmmm99/nippou-plugin
```

### その他のインストール方法

```bash
/plugins install github:kmmm99/nippou-plugin
```

または、ローカルインストール:

```bash
# ~/.claude/plugins/local/ にクローン
git clone https://github.com/kmmm99/nippou-plugin ~/.claude/plugins/local/nippou-plugin
```

## 使用方法

Claude Codeで以下のコマンドを実行します。

```
/nippou
```

### コマンド使用例

```
/nippou 先ほど聞いた内容を日報に記載してください。
```

### 保存形式例

```
## 2026-01-25

### 作業内容
- [リファクタリング] hogehoge
- [環境構築] てすとてすと
- [ドキュメント] テストテスト
- [調査] testtest

### 変更ファイル
- あのイーハトーヴォのすきとおった風、夏でも底に冷たさをもつ青いそら、うつくしい森で飾られたモリーオ市、郊外のぎらぎらひかる草の波。

### メモ
- あのイーハトーヴォのすきとおった風、夏でも底に冷たさをもつ青いそら、うつくしい森で飾られたモリーオ市、郊外のぎらぎらひかる草の波。
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
- **日報ファイル**: `~/Documents/claude-outputs/nippou/nippou_yyyymm.md`
- **過去月退避先**: `~/Documents/claude-outputs/nippou/nippou_old/`
```

## ファイル構造

```
nippou-plugin/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   └── nippou.md
└── README.md
```

## ライセンス

MIT License

## 注意事項

- 日報の記録はセキュリティの観点から自動更新ではありません。記録が必要な際は都度 `/nippou` コマンドを実行してください。
- 本プラグインの使用によって生じたデータの損失、システムの障害、その他いかなる損害についても、作者は一切の責任を負いません。使用は自己責任でお願いいたします。

---

  **作成日**: 2026-01-25  
  **最終更新日**: 2026-01-25  