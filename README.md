# marp-theme

my customized marp theme

## Usage

use `.vscode/settings.json` to set the theme

```json
{
  "markdown.marp.themes": [
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage.css",
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage-academic.css"
  ]
}
```

then, set frontmatter in markdown file

```markdown
---
marp: true
theme: kage
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
