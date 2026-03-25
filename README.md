# Business Context Hearing

事業方向性・ターゲットユーザー・ブランド方針・ユーザージャーニーを対話形式でヒアリングし、UI 設計の土台となるビジネスコンテキストドキュメントを生成する Claude Code スキル。事業コンテキストを UI の意思決定に変換する「事業 → UI 翻訳レイヤー」として機能します。

## 機能

- 構造化されたヒアリング（事業概要・ターゲットユーザー・ブランド方針・ユーザージャーニーの4フェーズ）
- ビジネスシグナルから UI 設計への自動変換（例: B2B SaaS → テーブル重視・コンパクト設計）
- 未決定事項へのデフォルト提案（技術スタック・チーム規模に基づく推奨値）
- `docs/biz-context.md` の自動生成（UI Implications Summary セクション付き）
- `ui-guideline-hearing` スキルとの連携（ビジネスコンテキストを UI ガイドラインに引き継ぎ）

## 前提条件

特になし

## インストール

```bash
# Claude Code のスキルディレクトリにクローン
git clone https://github.com/takezoe-f/claude-skill-biz-context.git ~/.claude/skills/biz-context-hearing/
```

## 使い方

以下のようなフレーズで起動します：

- `デザイン作成したい`
- `UIを作りたい`
- `事業コンテキストを整理して`
- `ターゲットユーザーを定義したい`
- `ブランド方針を決めたい`
- `/biz-context-hearing`

## ライセンス

MIT
