# Business Context Hearing Questions

Each phase uses AskUserQuestion (max 4 questions per call). Ask 2-4 rounds per phase.

---

## Phase 1: Business Overview (2 rounds)

### Round 1: Product Identity

**Q1: Product Type**
- header: "プロダクト種別"
- question: "どんな種類のプロダクトですか？"
- options:
  - B2B SaaS (企業向けサービス)
  - B2C アプリ (一般消費者向け)
  - 社内ツール / 管理画面
  - マーケットプレイス / プラットフォーム
- multiSelect: false

**Q2: Product Stage**
- header: "フェーズ"
- question: "プロダクトの現在のフェーズは？"
- options:
  - 新規立ち上げ (0→1、MVP段階)
  - グロース期 (PMF達成後、スケール中)
  - 成熟期 (安定運用、改善フェーズ)
  - リニューアル / リプレース
- multiSelect: false

**Q3: Business Domain**
- header: "事業ドメイン"
- question: "事業ドメインは？(「その他」で具体的に入力も可)"
- options:
  - EC / リテール
  - フィンテック / 金融
  - ヘルスケア / 医療
  - HR / 人材 / 教育
- multiSelect: false

**Q4: Revenue Model**
- header: "収益モデル"
- question: "主な収益モデルは？"
- options:
  - サブスクリプション (月額/年額)
  - トランザクション課金 (従量/手数料)
  - 広告モデル
  - ライセンス / 受託 / 社内利用
- multiSelect: false

### Round 2: Scale & Differentiation

**Q1: User Scale**
- header: "ユーザー規模"
- question: "現在 or 想定のユーザー規模は？"
- options:
  - ~100人 (少数の限定ユーザー)
  - 100~10,000人 (中規模)
  - 10,000~100,000人 (大規模)
  - 100,000人以上 (マス向け)
- multiSelect: false

**Q2: Competitive Advantage**
- header: "差別化"
- question: "プロダクトの主な差別化ポイントは？"
- options:
  - UX / 使いやすさ
  - 機能の豊富さ / 高機能
  - 価格 / コストパフォーマンス
  - スピード / パフォーマンス
- multiSelect: true

**Q3: Reference Products**
- header: "参考プロダクト"
- question: "UI/UXの参考にしているプロダクトはありますか？(「その他」で具体名を入力)"
- options:
  - Notion / Linear 系 (クリーン・ミニマル)
  - Figma / Miro 系 (クリエイティブツール)
  - Stripe / Vercel 系 (デベロッパー向け洗練)
  - 特にない / まだ決めていない
- multiSelect: true

**Q4: Key Metrics**
- header: "重要KPI"
- question: "UIが最も影響すべきKPIは？"
- options:
  - コンバージョン率 (CVR / 課金率)
  - リテンション / DAU・MAU
  - タスク完了率 / 業務効率
  - オンボーディング完了率
- multiSelect: true

---

## Phase 2: Target Users (3 rounds)

### Round 1: Primary Persona

**Q1: Primary User**
- header: "主要ユーザー"
- question: "メインのユーザー像は？"
- options:
  - ビジネスパーソン (営業・マーケ・経営層)
  - エンジニア / デベロッパー
  - デザイナー / クリエイター
  - 一般消費者 (幅広い層)
- multiSelect: false

**Q2: Tech Literacy**
- header: "ITリテラシー"
- question: "ユーザーのITリテラシーは？"
- options:
  - 高い (エンジニア・テック企業社員)
  - 中程度 (日常的にPCを使うオフィスワーカー)
  - 低い (ITに不慣れ、高齢者含む)
  - 混在 (リテラシーが大きくばらつく)
- multiSelect: false

**Q3: Usage Context**
- header: "利用環境"
- question: "主な利用環境は？"
- options:
  - デスクトップ (オフィスのPC)
  - モバイル中心 (スマホメイン)
  - タブレット (現場 / 店舗)
  - マルチデバイス (どこからでも)
- multiSelect: false

**Q4: Usage Frequency**
- header: "利用頻度"
- question: "ユーザーの典型的な利用頻度は？"
- options:
  - 毎日数時間 (業務ツール)
  - 毎日数分 (チェック・確認系)
  - 週に数回 (必要な時だけ)
  - 月に数回 (低頻度)
- multiSelect: false

### Round 2: User Needs & Pain Points

**Q1: Core Task**
- header: "コアタスク"
- question: "ユーザーがこのプロダクトで最も頻繁に行うタスクは？(「その他」で具体的に入力)"
- options:
  - データの閲覧・分析 (ダッシュボード・レポート)
  - データの入力・編集 (フォーム・CRUD)
  - コミュニケーション (チャット・コメント・通知)
  - ワークフロー管理 (タスク・承認・進捗)
- multiSelect: true

**Q2: Pain Point**
- header: "課題"
- question: "ユーザーが現在抱えている最大のペインは？"
- options:
  - 操作が複雑 / 学習コストが高い
  - 処理が遅い / 待ち時間が長い
  - 必要な情報にたどり着けない
  - 既存ツールの連携が悪い
- multiSelect: true

**Q3: Decision Maker**
- header: "意思決定者"
- question: "導入 or 利用継続の意思決定者は？(B2Bの場合)"
- options:
  - 実際のエンドユーザー自身
  - 部門長 / マネージャー
  - 経営層 / CxO
  - IT部門 / 情シス
- multiSelect: true

### Round 3: Accessibility & Locale

**Q1: Language & Locale**
- header: "言語/地域"
- question: "対象の言語・地域は？"
- options:
  - 日本語のみ (国内向け)
  - 日英バイリンガル
  - 多言語 (i18n対応)
  - 英語のみ (グローバル)
- multiSelect: false

**Q2: Accessibility Priority**
- header: "A11y重要度"
- question: "アクセシビリティの重要度は？(事業観点で)"
- options:
  - 法的要件あり (公共サービス・金融等)
  - 高い (多様なユーザーベース)
  - 中程度 (ベストエフォート)
  - 低い (限定ユーザー向け社内ツール)
- multiSelect: false

**Q3: Data Sensitivity**
- header: "データ機密性"
- question: "扱うデータの機密性は？(UIでの表示・マスキングに影響)"
- options:
  - 高い (個人情報・金融データ・医療情報)
  - 中程度 (企業の業務データ)
  - 低い (公開情報中心)
- multiSelect: false

---

## Phase 3: Brand & Design Direction (3 rounds)

### Round 1: Brand Personality

**Q1: Brand Personality**
- header: "ブランド人格"
- question: "プロダクトが持つべき人格・トーンは？"
- options:
  - プロフェッショナル / 信頼感 (銀行・法律系)
  - フレンドリー / 親しみやすい (コンシューマー)
  - 先進的 / テック感 (スタートアップ・開発者向け)
  - 落ち着き / プレミアム (高級サービス)
- multiSelect: true

**Q2: Visual Mood**
- header: "ビジュアル"
- question: "UIのビジュアルの方向性は？"
- options:
  - ミニマル / クリーン (余白を活かす)
  - リッチ / 情報密度高め (ダッシュボード型)
  - 遊び心 / イラスト多用 (カジュアル)
  - 構造的 / グリッドベース (業務システム)
- multiSelect: false

**Q3: Color Direction**
- header: "カラー方向性"
- question: "カラーの印象として目指したい方向は？"
- options:
  - ブルー基調 (信頼・安定)
  - グリーン基調 (成長・健康)
  - ダーク基調 (洗練・プロ)
  - 明るい / カラフル (活気・楽しさ)
- multiSelect: false

**Q4: Typography Direction**
- header: "文字の印象"
- question: "タイポグラフィで表現したい印象は？"
- options:
  - ゴシック / モダン (Noto Sans JP, Inter 等)
  - 丸ゴシック / 柔らかい (Rounded M+, Quicksand 等)
  - セリフ / フォーマル (Noto Serif JP, Merriweather 等)
  - 等幅 / テック (JetBrains Mono, IBM Plex Mono 等)
- multiSelect: false

### Round 2: UX Principles

**Q1: UX Priority**
- header: "UX優先度"
- question: "UXデザインで最も優先すべき価値は？(2つまで)"
- options:
  - 学習容易性 (初見で迷わない)
  - 効率性 (慣れたユーザーが速く操作できる)
  - エラー防止 (ミスしにくい)
  - 満足度 (使っていて気持ちいい)
- multiSelect: true

**Q2: Information Architecture**
- header: "情報設計"
- question: "情報設計のアプローチは？"
- options:
  - シンプル (機能を絞り、段階的に開示)
  - パワーユーザー志向 (高機能、カスタマイズ性)
  - ウィザード / ステップ型 (手順に沿って導く)
  - ダッシュボード型 (一覧性重視)
- multiSelect: false

**Q3: Navigation Pattern**
- header: "ナビゲーション"
- question: "UIのナビゲーションパターンの方向性は？"
- options:
  - サイドバー + トップバー (管理画面型)
  - タブ / セグメント (シンプルSPA型)
  - ハブ&スポーク (ホーム画面→詳細)
  - コマンドパレット / 検索中心
- multiSelect: false

**Q4: Content Density**
- header: "情報密度"
- question: "画面あたりの情報密度は？"
- options:
  - 低密度 (余白たっぷり、1画面に少ない要素)
  - 中密度 (バランス型)
  - 高密度 (テーブル・グラフ多数、情報量重視)
  - 可変 (ユーザーがカスタマイズ可能)
- multiSelect: false

### Round 3: Constraints & Priorities

**Q1: Design Constraints**
- header: "制約"
- question: "UIデザインにおける制約は？"
- options:
  - 既存のブランドガイドラインに準拠する必要あり
  - 既存プロダクトとのUI一貫性が必要
  - 規制・コンプライアンス要件あり (金融・医療等)
  - 特に制約なし (自由に決められる)
- multiSelect: true

**Q2: Time vs Quality**
- header: "速度vs品質"
- question: "開発のスピードとUI品質のバランスは？"
- options:
  - スピード優先 (MVPを早く出す)
  - 品質優先 (UIの完成度を重視)
  - バランス型 (主要画面は高品質、その他はスピード)
- multiSelect: false

**Q3: Future Vision**
- header: "将来像"
- question: "1年後のプロダクトの姿として正しいのは？"
- options:
  - 機能拡張 (今の倍以上の機能がある)
  - 深掘り (コア機能のUXを極限まで磨く)
  - プラットフォーム化 (API / プラグイン / エコシステム)
  - 横展開 (別市場・別ユーザー層への拡大)
- multiSelect: false

---

## Phase 4: Key User Journeys (2 rounds)

### Round 1: Core Journeys

**Q1: Onboarding**
- header: "オンボーディング"
- question: "ユーザーの初回体験で最も重要なことは？"
- options:
  - 最短でコア機能の価値を体験させる (Time to Value)
  - ステップバイステップのガイドツアー
  - テンプレート / サンプルデータで即使える
  - 自由に触らせる (探索型)
- multiSelect: false

**Q2: Primary Flow**
- header: "主要フロー"
- question: "最も重要なユーザーフローは？(「その他」で具体的に入力)"
- options:
  - 検索 → 閲覧 → アクション
  - 入力 → 確認 → 送信
  - 一覧 → フィルタ → 詳細 → 編集
  - ダッシュボード → ドリルダウン → エクスポート
- multiSelect: false

**Q3: Error Recovery**
- header: "エラー回復"
- question: "ユーザーがミスした時の回復体験として重視するのは？"
- options:
  - Undo / 取り消しを常に提供
  - 確認ダイアログで事前防止
  - 自動保存 / 下書き保存で損失ゼロ
  - 入力バリデーションで未然防止
- multiSelect: true

### Round 2: Edge Cases & Emotional Design

**Q1: Empty State Strategy**
- header: "空状態"
- question: "データが空の時のUX戦略は？"
- options:
  - CTA (「まず○○を作成しましょう」)
  - サンプルデータ / テンプレートを表示
  - 説明イラスト + ガイド
  - 何も表示しない (空のまま)
- multiSelect: false

**Q2: Delight Moments**
- header: "喜びの瞬間"
- question: "ユーザーに「いいね」と思わせたい瞬間は？"
- options:
  - タスク完了時のフィードバック (成功アニメ・祝福)
  - データの可視化 (数字が見える化される瞬間)
  - スピード感 (操作の即時反映)
  - 細部の作り込み (マイクロインタラクション)
- multiSelect: true

**Q3: Trust Signals**
- header: "信頼性"
- question: "UIで信頼感を伝えるために重要な要素は？"
- options:
  - 操作のフィードバック (保存完了、送信完了の明示)
  - データの鮮度表示 (最終更新日時)
  - セキュリティの可視化 (暗号化、権限表示)
  - ステータスの透明性 (処理中の進捗表示)
- multiSelect: true
