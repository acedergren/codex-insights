---
name: Agent Workflow Roast
description: Evidence-first coaching reports for local agent workflow review.
colors:
  ink: "#121827"
  muted: "#62708a"
  report-bg: "#eef3f8"
  workspace: "#fbfcfe"
  panel: "#ffffff"
  soft-panel: "#f6f8fb"
  line: "#dfe6ef"
  line-strong: "#d6e0ec"
  primary-blue: "#2f6fd6"
  success-green: "#2f9b67"
  insight-purple: "#7b61c9"
  warning-orange: "#d88318"
  danger-red: "#c84b43"
  nav-ink: "#101923"
  playground-bg: "#0b1118"
  playground-panel: "#121b26"
  playground-panel-2: "#172333"
  playground-line: "#26364a"
  playground-text: "#eef5ff"
  playground-muted: "#9fb0c4"
typography:
  headline:
    fontFamily: "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "clamp(1.55rem, 3vw, 2.35rem)"
    fontWeight: 700
    lineHeight: 1.08
    letterSpacing: "0"
  title:
    fontFamily: "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "1rem"
    fontWeight: 700
    lineHeight: 1.25
    letterSpacing: "0"
  body:
    fontFamily: "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "0.88rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0"
  label:
    fontFamily: "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "0.82rem"
    fontWeight: 720
    lineHeight: 1.2
    letterSpacing: "0"
  mono-label:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.86rem"
    fontWeight: 760
    lineHeight: 1.2
    letterSpacing: "0"
rounded:
  xs: "5px"
  sm: "6px"
  md: "8px"
  lg: "10px"
  xl: "12px"
  pill: "999px"
spacing:
  xs: "8px"
  sm: "10px"
  md: "14px"
  lg: "18px"
  xl: "24px"
components:
  button-primary:
    backgroundColor: "{colors.primary-blue}"
    textColor: "{colors.panel}"
    rounded: "{rounded.sm}"
    padding: "0 10px"
    height: "38px"
    typography: "{typography.label}"
  nav-link:
    backgroundColor: "{colors.soft-panel}"
    textColor: "{colors.nav-ink}"
    rounded: "{rounded.sm}"
    padding: "7px 10px"
    typography: "{typography.label}"
  badge-info:
    backgroundColor: "#f7fbff"
    textColor: "{colors.primary-blue}"
    rounded: "{rounded.sm}"
    padding: "4px 12px"
    height: "28px"
    typography: "{typography.label}"
  panel-card:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "18px 20px"
  input-dark:
    backgroundColor: "{colors.playground-panel-2}"
    textColor: "{colors.playground-text}"
    rounded: "7px"
    padding: "0 10px"
    height: "38px"
    typography: "{typography.body}"
---

# Design System: Agent Workflow Roast

## 1. Overview

**Creative North Star: "The Honest Workbench"**

Agent Workflow Roast should feel like a practical surface where a developer lays out evidence, compares the signals, and leaves with a better next move. It is candid, local, and work-focused: the visual system earns trust by making receipts easy to scan before it offers coaching.

The report UI uses restrained light surfaces, crisp borders, compact panels, and a small semantic accent set. The playground uses a darker workbench variant for prompt experimentation, but it keeps the same density, rounded geometry, and direct component language. The system rejects a punitive scorecard, generic SaaS-dashboard tropes, and raw log-dump density.

**Key Characteristics:**

- Evidence first, coaching second.
- Compact panels with clear hierarchy and modest depth.
- Semantic color reserved for status, categories, and action.
- System sans typography with mono labels only where command-like context matters.
- Controls that feel dense, calm, and actionable.

## 2. Colors

The palette is a restrained product palette: cool neutral surfaces, dark ink, one primary blue, and a small set of semantic coaching colors.

### Primary

- **Receipt Blue**: The primary action, selection, link, and navigation accent. Use it sparingly so blue continues to mean "look here" or "act here."

### Secondary

- **Evidence Green**: Success, progress, positive trend, and useful confirmation.
- **Insight Purple**: Pattern, synthesis, and coaching category accents.
- **Review Orange**: Warning, medium-priority friction, and attention without alarm.
- **Boundary Red**: Error, failure, and high-risk friction.

### Neutral

- **Workbench Ink**: Primary text and high-trust labels.
- **Muted Steel**: Secondary text, timestamps, descriptions, and low-emphasis metadata.
- **Report Mist**: Outer report background.
- **Workspace White**: Main report container and high-density content surface.
- **Soft Panel**: Nested grouping, evidence blocks, and quiet repeated cards.
- **Rule Line**: Dividers, panel strokes, nav strokes, and low-contrast boundaries.
- **Night Workbench**: Playground background and dark-mode experiment surface.

### Named Rules

**The Receipt-First Color Rule.** Color must identify action, status, or category. It is not decoration.

**The No Punitive Heatmap Rule.** Never turn the roast into a red-heavy grade board. Red is reserved for concrete failure or risk.

## 3. Typography

**Display Font:** Inter with system sans fallbacks.
**Body Font:** Inter with system sans fallbacks.
**Label/Mono Font:** ui-monospace, SFMono-Regular, Menlo, Consolas, monospace.

**Character:** The type system is utilitarian and compact. It should read like a sharp internal tool, not a marketing page or a terminal dump.

### Hierarchy

- **Display** (700, clamp(1.55rem, 3vw, 2.35rem), 1.08): Report titles only. Keep the clamp modest and never use hero-sized product marketing type.
- **Headline** (700, 1.1rem to 1.65rem, 1.2): Metric values, node centers, and high-importance report summaries.
- **Title** (700, 1rem, 1.25): Panel headings and section titles.
- **Body** (400, 0.84rem to 0.98rem, 1.35 to 1.5): Report prose, evidence notes, and descriptions. Cap long prose at 65 to 75 characters where layout allows.
- **Label** (690 to 760, 0.72rem to 0.86rem, 1.2): Badges, nav links, controls, compact metadata, and command labels.

### Named Rules

**The Tool-Type Rule.** Use one sans family for nearly everything. Mono appears only for commands, paths, code, or the `/roast` label.

**The Scan-First Rule.** Headings must create visible jumps in scale or weight. If panel headings, labels, and body copy blur together, the type hierarchy is too flat.

## 4. Elevation

The system uses structural layers: borders and modest shadows separate report regions, while tonal panels organize dense evidence. Shadows are present but quiet. They support reading order, not atmosphere.

### Shadow Vocabulary

- **Workspace Lift** (`box-shadow: 0 18px 50px rgb(17 24 39 / 0.08)`): The single outer report container on light backgrounds.
- **Panel Lift** (`box-shadow: 0 10px 24px rgb(17 24 39 / 0.04)`): Standard report panels.
- **Node Lift** (`box-shadow: 0 10px 24px rgb(17 24 39 / 0.06)`): Diagram nodes and objects that need to sit above a canvas.

### Named Rules

**The Structural Layer Rule.** Pair borders with soft shadows only for major containers and diagram nodes. Repeated cards should stay mostly tonal and bordered.

**The No Ghost-Card Rule.** Do not use a decorative 1px border plus a large soft shadow on every element. If everything floats, nothing is evidence.

## 5. Components

Components are dense, calm, and actionable. Shapes stay compact: 6px to 12px for real containers, full pill only for tiny badges and status marks.

### Buttons

- **Shape:** Compact rounded rectangles (6px to 7px radius); full-width only in the playground sidebar where the grid needs it.
- **Primary:** Receipt Blue or the dark playground primary (`#1f5fbf`) with white text, minimum height 38px, and tight horizontal padding.
- **Hover / Focus:** Use border shift, tone shift, and visible focus rings. Do not add decorative motion.
- **Secondary / Ghost / Tertiary:** Use panel backgrounds, Rule Line borders, and strong label weight rather than low-contrast gray text.

### Chips

- **Style:** Full-pill radius with tinted semantic background and matching semantic text.
- **State:** Use for status, category, and confidence labels. A chip must name a meaningful state, never merely decorate a card.

### Cards / Containers

- **Corner Style:** Report panels use 8px; the main workspace uses 12px; playground panels use 10px.
- **Background:** White panels on light report surfaces, Soft Panel for nested blocks, and Night Workbench panels in the playground.
- **Shadow Strategy:** Follow the Structural Layer Rule. Main surfaces may lift; repeated evidence cards should rely on borders and tonal contrast.
- **Border:** Rule Line by default, stronger line only for the outer workspace.
- **Internal Padding:** 14px for compact cards, 18px to 24px for panel headers and primary report sections.

### Inputs / Fields

- **Style:** Dark playground fields use Playground Panel 2, Playground Line borders, 7px radius, and inherited Inter text.
- **Focus:** Shift border toward Receipt Blue and add a visible outline. Placeholder text must meet contrast requirements.
- **Error / Disabled:** Use Boundary Red for errors and muted text plus lower opacity for disabled states. Never rely on color alone.

### Navigation

- **Style:** Sticky quick navigation uses compact pill-like links, 6px radius, pale blue-gray fills, and strong label weight.
- **States:** Active or selected states should use Receipt Blue with a clear border or fill change. Hover may deepen the panel tone.
- **Mobile:** Preserve horizontal scrolling for dense report nav instead of stacking every link into a tall block.

### Report Metrics

Metric rows combine a semantic circular icon, a compact title, a large numeric value, and a muted explanation. Icons are status anchors, not illustrations. Do not convert metric rows into oversized hero-stat cards.

## 6. Do's and Don'ts

### Do:

- **Do** lead every report surface with evidence and then coaching.
- **Do** keep semantic colors rare enough that they still mean action, status, or category.
- **Do** use 8px panel radii, 6px control radii, and 999px only for tiny status chips or icons.
- **Do** keep text contrast at WCAG AA or better across report and playground surfaces.
- **Do** preserve the local, privacy-respecting feel: the interface should look like it handles sensitive work history carefully.

### Don't:

- **Don't** create a punitive scorecard. The interface must not shame the user, over-focus on grades, or turn coaching into gamified judgment.
- **Don't** use generic SaaS-dashboard tropes: hero metrics, vague productivity claims, decorative card grids, or gradient-text emphasis.
- **Don't** ship raw log-dump density. Evidence must be grouped, labeled, and scannable.
- **Don't** use red as a general "bad workflow" wash. Boundary Red is for concrete error, failure, or high-risk friction only.
- **Don't** add side-stripe borders, decorative glass effects, oversized shadows, or rounded cards above 16px.
