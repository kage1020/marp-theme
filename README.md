# marp-theme

my customized marp theme

## Usage

use `.vscode/settings.json` to set the theme

```json
{
  "markdown.marp.themes": [
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage1020.css",
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage1020-academic.css",
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage1020-ds.css"
  ]
}
```

then, set frontmatter in markdown file

```markdown
---
marp: true
theme: kage1020
---
```

## Preview

### cover slide

```markdown
<!--
_class: cover
-->
```

![](.docs/cover.png)

### appendix slide

```markdown
---
_class: appendix
---
```

![](.docs/appendix.png)

### default slide

```markdown
---
<!--
header: Title for Chapter
footer: Sub Title for Sub Chapter
paginate: true
-->
```

![default design](.docs/default.png)

### with image alignment

#### centering

```markdown
![center](image.pnghttps://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)
```

![centering image](.docs/image-center.png)

#### right aligned

```markdown
![right](image.pnghttps://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)
```

![right aligned image](.docs/image-right.png)

### table

```markdown
| header1 | header2 | header3 |
| ------- | ------- | ------- |
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
| cell7   | cell8   | cell9   |
```

![table](.docs/table.png)

![table academic](.docs/table-academic.png)

### Color code

```markdown
<code class="color" style="--color: red">red</code>
```

![color code](.docs/color.png)

## Blockquote and Citation

```markdown
> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.
<cite class="center">Someone famous in Source Title</cite>
```

![blockquote and citation](.docs/blockquote.png)

### arrow

```markdown
<p class="before-right-arrow">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Atque eaque beatae quas facere ut blanditiis nisi sint laudantium, possimus nobis sed iste commodi praesentium eveniet assumenda porro esse omnis, repellat itaque totam, quisquam facilis voluptatem consequuntur corrupti! Tenetur distinctio atque quisquam nihil? Dignissimos quibusdam obcaecati nam odio consequatur recusandae ex.</p>
```

![arrow](.docs/arrow.png)

## kage1020-ds

A theme that follows the kage1020 design system: near-monochrome, one accent hue (`accent`), one signal hue (`danger`), no shadows or gradients, and boundaries drawn either by a surface difference (`bg-subtle`) or a 1px hairline (`line`). Colors are the design system tokens as-is; type, spacing and radii are scaled ×1.75 for slides (body 16px → 28px). Fonts are not loaded; the OS default `sans` / `mono` stacks are used.

```markdown
---
marp: true
theme: kage1020-ds
paginate: true
---
```

See [kage1020-ds.md](kage1020-ds.md) for every feature. HTML must be enabled (`--html` for Marp CLI, `markdown.marp.enableHtml` for VS Code) to use the `<div>`, `<cite>`, `<kbd>` and `<p class>` snippets below.

![kage1020-ds cover](.docs/ds-cover.png)

![kage1020-ds default](.docs/ds-default.png)

| Markdown | Result |
| --- | --- |
| `_class: cover` | Title slide with the design system's cover art (top right) |
| `_class: appendix` | Section divider on the `bg-subtle` surface |
| `_class: dark` (or `invert`) | Dark theme; combine as `_class: cover dark` |
| `header` / `footer` / `paginate` | `meta` text in `ink-muted`; page number as `3 / 13` in `mono` |
| `\| --: \|` (right-aligned column) | Treated as numbers: `mono` with tabular figures |
| `<th class="up">` / `<th class="down">` | Sort direction shown as `↑` / `↓` |
| `<div class="callout">` / `<div class="callout danger">` | The only two boxed containers: a group, or something that needs confirmation |
| `<kbd>⌘</kbd>` | Key hint |
| `<mark>` | Highlight on the referenced part of the source text |
| `<p class="meta">` / `<p class="caption">` | Supplementary text in `ink-muted` |
| `![center](…)` / `![right](…)` | Centered / right-floated image |
| `<code class="color" style="--color: #2d70b3">` | Color swatch |
| `<cite>` / `<cite class="center">` / `<cite class="right">` | Citation |

![kage1020-ds dark](.docs/ds-dark.png)
