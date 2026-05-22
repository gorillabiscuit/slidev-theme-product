# slidev-theme-product

A Slidev theme inspired by Apple product pages.

**One idea per slide. Display-scale type. Restrained palette. Animated bar charts.**

![Preview](https://raw.githubusercontent.com/gorillabiscuit/slidev-theme-product/main/preview.png)

---

## Install

Add to your `slides.md` frontmatter:

```yaml
---
theme: product
colorSchema: light
fonts:
  sans: Inter
  weights: '400,500,600,700'
  provider: google
---
```

Slidev will prompt to install the theme automatically on first run.

---

## Design principles

This theme encodes four rules:

1. **One idea per slide.** If a slide has three messages, split it into three slides.
2. **Headlines do the work.** Make them large, short, and confident. No full sentences.
3. **Whitespace is content.** Content sits in the centre with generous breathing room.
4. **Restrained palette.** Mostly white or `--product-bg-alt`, with the accent colour used for one element per slide.

---

## CSS tokens

Override any token in your own `style.css`:

```css
:root {
  /* Palette */
  --product-ink:     #1d1d1f;   /* primary text */
  --product-muted:   #86868b;   /* secondary text */
  --product-bg:      #ffffff;
  --product-bg-alt:  #f5f5f7;   /* section backgrounds */
  --product-accent:  #0071e3;   /* Apple blue — eyebrows & labels */

  /* Data colours (use one per chart) */
  --product-blue:    #007AFF;
  --product-green:   #34C759;
  --product-red:     #FF3B30;
  --product-gray:    #8E8E93;

  /* Type scale */
  --product-display: clamp(48px, 6.5vw, 88px);
  --product-h1:      clamp(28px, 3.8vw, 48px);
  --product-h2:      clamp(22px, 2.8vw, 34px);
  --product-body:    clamp(16px, 1.3vw, 19px);
  --product-eyebrow: clamp(12px, 0.9vw, 14px);
}
```

---

## Layouts

Uses Slidev's built-in layouts. Recommended patterns:

| Layout | Use for |
|---|---|
| `intro-image-right` | Cover slide with photo |
| `fact` | Single stat or number — fills the slide |
| `section` | Chapter divider — `f5f5f7` background |
| `statement` | Full-screen recommendation or conclusion |
| `two-cols` | Pros/cons, before/after comparisons |
| `default` | Everything else |

---

## Utility classes

### `.eyebrow`
Short accent-coloured label above the main heading.

```html
<div class="eyebrow">Context</div>
## Why this. Why now.
```

### `.source-line`
Tiny citation pinned to the bottom-left of the slide. Consistent across all slides.

```html
<div class="source-line">Author · Year · Grade B</div>
```

### `.bar-row` / `.bar-track` / `.bar`
Horizontal animated bar chart. Bars animate from left on slide entry. Use `max-width` inline to set the bar length. Use one colour per chart — avoid mixing data colours.

```html
<div class="bar-row">
  <div class="bar-label" style="width:200px">Managed buildings</div>
  <div class="bar-track" style="height:36px">
    <div class="bar" style="max-width:70%; background:var(--product-blue)">70%</div>
  </div>
  <div class="bar-note">Knight Frank 2024</div>
</div>
```

---

## Recommended workflow

```bash
# Start
npm init slidev@latest my-deck
cd my-deck
# Add theme to slides.md frontmatter: theme: product
npx slidev slides.md

# Export PDF
npx slidev export slides.md --format pdf
```

---

## Source evidence grade convention

This theme includes a convention for citing sources used in the [keynot](https://github.com/shawnzam/keynot) tradition of graded evidence:

- **Grade A** — Peer-reviewed academic
- **Grade B** — Credible industry body (major consultancies, government data)
- **Grade C** — Operator / provider marketing
- **Grade D** — Anecdotal / agent commentary

Use the sources appendix slide pattern (see `example.md`) with `.source-line` on each data slide for consistent attribution.

---

## Contributing

Issues and PRs welcome. See `example.md` for all supported patterns.

---

## License

MIT © Wouter Schreuders
