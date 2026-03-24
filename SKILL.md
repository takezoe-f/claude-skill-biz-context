---
name: biz-context-hearing
description: >
  事業方向性・ターゲットユーザー・ブランド方針・ユーザージャーニーをヒアリングで収集し、
  UI設計の土台となるビジネスコンテキストドキュメントを生成するスキル。
  事業コンテキストをUIの意思決定に変換する「事業→UI翻訳レイヤー」として機能する。
  単体で使えるが、ui-guideline-hearing と組み合わせると最大効果を発揮する。
  トリガー: 「デザイン作成したい」「UIを作りたい」「画面を設計したい」
  「事業コンテキストを整理して」「ビジネス要件をヒアリングして」「ターゲットユーザーを定義したい」
  「ブランド方針を決めたい」「UXの方向性を決めたい」「/biz-context-hearing」
  「プロダクトのUI方針を決めたい」「デザインの方向性を相談したい」
  「新しいプロダクトを作りたい」「アプリを作りたい」
---

# Business Context Hearing

Conduct a structured interview to capture business direction, then translate it into UI design implications.

## When This Skill Activates

This skill should trigger **before** technical UI decisions are made. Specifically:

- User says "デザイン作成したい" / "UIを作りたい" / "アプリを作りたい" → Run this first, then suggest `ui-guideline-hearing`
- User says "事業コンテキスト" / "ビジネス要件" → Run this standalone
- `ui-guideline-hearing` can reference the output of this skill

## Workflow

Execute phases sequentially. Use `AskUserQuestion` for each round (max 4 questions per call).
Read [references/hearing-questions.md](references/hearing-questions.md) for the full question bank.

### Phase 1: Business Overview (2 rounds)

1. **Product Identity**: product type, stage, domain, revenue model
2. **Scale & Differentiation**: user scale, competitive advantage, reference products, key KPIs

### Phase 2: Target Users (3 rounds)

1. **Primary Persona**: user type, IT literacy, usage context, usage frequency
2. **Needs & Pain Points**: core tasks, pain points, decision maker (B2B)
3. **Accessibility & Locale**: language/locale, a11y priority, data sensitivity

### Phase 3: Brand & Design Direction (3 rounds)

1. **Brand Personality**: brand persona, visual mood, color direction, typography direction
2. **UX Principles**: UX priority, information architecture, navigation pattern, content density
3. **Constraints & Priorities**: design constraints, speed vs quality, future vision

### Phase 4: Key User Journeys (2 rounds)

1. **Core Journeys**: onboarding strategy, primary flow, error recovery
2. **Edge Cases & Emotional Design**: empty states, delight moments, trust signals

### Phase 5: Generate Document

1. Read [references/context-template.md](references/context-template.md)
2. Fill template with all collected answers
3. **Critical**: Generate Section 5 "UI Implications Summary" — translate every business decision into a concrete UI recommendation
4. Write to user-specified path (default: `docs/biz-context.md`)
5. Suggest running `ui-guideline-hearing` next if not already done

## Business → UI Translation Rules

The core value of this skill is translating business context into actionable UI guidance.
Apply these mappings when generating Section 5:

| Business Signal | UI Implication |
|-----------------|----------------|
| B2B SaaS + 高密度 | Table-heavy, compact spacing, keyboard shortcuts, power-user features |
| B2C + 低リテラシー | Large touch targets (48px+), progressive disclosure, step-by-step wizards |
| フィンテック + 信頼感 | Blue tones, serif accents, explicit confirmations, data freshness timestamps |
| MVP / スピード優先 | UI library defaults (shadcn/ui), skip custom tokens, focus on core flow only |
| 毎日数時間利用 | Keyboard-first, dense UI, customizable layout, persistent sidebar |
| 月に数回利用 | Strong wayfinding, onboarding hints, forgiving inputs |
| データ機密性:高 | Masking by default, confirm-before-reveal, audit trail visibility |
| モバイル中心 | Bottom navigation, thumb-zone aware layout, offline states |
| 多言語 | i18n-ready spacing (text expansion buffer), RTL consideration, icon-first labels |
| エンジニア向け | Monospace accents, CLI-like shortcuts, code blocks, dark mode default |

## Handling "Undecided" Answers

Same policy as `ui-guideline-hearing`:
1. Do not block progress
2. Propose a sensible default with `💡` marker and 1-sentence rationale
3. Collect all defaults in a summary at the end

## Integration with ui-guideline-hearing

When both skills are used together, the flow is:

```
biz-context-hearing → docs/biz-context.md
                            ↓ (read as input)
ui-guideline-hearing → docs/ui-guideline.md
```

`ui-guideline-hearing` should read `docs/biz-context.md` at the start of Phase 0 and use the "UI Implications Summary" to:
- Pre-fill sensible defaults for undecided technical questions
- Validate that technical choices align with business direction
- Flag conflicts (e.g., "MVP mode but chose complex token system")
