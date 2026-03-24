# Business Context Output Template

Replace `{{...}}` placeholders with hearing results. Mark undecided items with `💡`.

---

```markdown
# Business Context Document

> Generated: {{date}}
> Product: {{product_name}}

---

## 1. Business Overview

### 1.1 Product Identity

| Item | Value |
|------|-------|
| Product Type | {{product_type}} |
| Stage | {{product_stage}} |
| Domain | {{business_domain}} |
| Revenue Model | {{revenue_model}} |
| User Scale | {{user_scale}} |

### 1.2 Differentiation & KPIs

**Competitive Advantage**: {{competitive_advantage}}

**Reference Products**: {{reference_products}}

**Key Metrics UI Should Optimize**:
{{key_metrics}}

---

## 2. Target Users

### 2.1 Primary Persona

| Item | Value |
|------|-------|
| User Type | {{primary_user}} |
| IT Literacy | {{tech_literacy}} |
| Primary Device | {{usage_context}} |
| Usage Frequency | {{usage_frequency}} |

### 2.2 Core Tasks & Pain Points

**Most Frequent Tasks**:
{{core_tasks}}

**Current Pain Points**:
{{pain_points}}

**Decision Maker** (B2B): {{decision_maker}}

### 2.3 Accessibility & Locale

| Item | Value |
|------|-------|
| Language | {{language_locale}} |
| A11y Priority | {{a11y_priority}} |
| Data Sensitivity | {{data_sensitivity}} |

---

## 3. Brand & Design Direction

### 3.1 Brand Personality

{{brand_personality}}

### 3.2 Visual Direction

| Item | Direction |
|------|-----------|
| Visual Mood | {{visual_mood}} |
| Color Direction | {{color_direction}} |
| Typography | {{typography_direction}} |
| Content Density | {{content_density}} |

### 3.3 UX Principles (Priority Order)

1. {{ux_priority_1}}
2. {{ux_priority_2}}

### 3.4 Information Architecture

{{information_architecture}}

### 3.5 Navigation Pattern

{{navigation_pattern}}

### 3.6 Constraints

{{design_constraints}}

### 3.7 Speed vs Quality

{{speed_vs_quality}}

### 3.8 Future Vision (1 Year)

{{future_vision}}

---

## 4. Key User Journeys

### 4.1 Onboarding Strategy

{{onboarding_strategy}}

### 4.2 Primary Flow

{{primary_flow}}

### 4.3 Error Recovery

{{error_recovery}}

### 4.4 Empty State Strategy

{{empty_state_strategy}}

### 4.5 Delight Moments

{{delight_moments}}

### 4.6 Trust Signals

{{trust_signals}}

---

## 5. UI Implications Summary

Based on the business context above, the following UI decisions are recommended:

### Color & Typography
{{ui_implication_color_typo}}

### Layout & Density
{{ui_implication_layout}}

### Interaction & Animation
{{ui_implication_interaction}}

### Accessibility
{{ui_implication_a11y}}

### Component Priorities
{{ui_implication_components}}
```

---

## Generation Notes

- Section 5 "UI Implications Summary" is the key bridge to `ui-guideline-hearing`.
  Translate business context into concrete UI recommendations.
- Examples of business→UI translation:
  - B2B SaaS + 高密度 → Table-heavy layout, compact spacing, keyboard shortcuts
  - B2C + 低リテラシー → Large touch targets, progressive disclosure, step-by-step flows
  - フィンテック + 信頼感 → Blue tones, serif accents, explicit confirmations, data freshness indicators
  - スタートアップ MVP → shadcn/ui defaults, skip custom tokens, focus on core flow only
- Keep the document under 400 lines.
