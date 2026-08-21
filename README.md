# marp-theme

my customized marp theme

## Usage

use `.vscode/settings.json` to set the theme

```json
{
  "markdown.marp.themes": [
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage1020.css",
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/kage1020-academic.css",
    "https://raw.githubusercontent.com/kage1020/marp-theme/main/claude-code.css"
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

## claude-code theme

A dark theme inspired by the Claude Code CLI.

```markdown
---
marp: true
theme: claude-code
paginate: true
header: Chapter Title
footer: Sub Title
---
```

### layout

- top left: a character (`--cc-character`) and its one-line comment (`.comment`)
- top right: `header`
- center: slide contents
- bottom: a prompt box filled with the `#` heading of the slide
- bottom left: `footer`
- bottom right: page number

![default slide](.docs/claude-code-default.png)

### cover slide

```markdown
<!--
_class: cover
-->

# Title

## Subtitle

Author / Date
```

![cover slide](.docs/claude-code-cover.png)

### divider slide

Written as a slash command. Use `##` instead of `#` on this class.

```markdown
<!--
_class: divider
-->

## getting-started
```

![divider slide](.docs/claude-code-divider.png)

### character comment

```markdown
<p class="comment">a one-line comment</p>
<p class="comment thinking">thinking...</p>
```

### agent log style

```markdown
<p class="tool">Read(slides.md)</p>
<p class="result">Read 128 lines</p>
<p class="result"><span class="added">+ 12 lines</span> / <span class="removed">- 3 lines</span></p>
```

![agent log style](.docs/claude-code-tool.png)

### classes

| class                | description                                  |
| -------------------- | -------------------------------------------- |
| `_class: cover`      | cover slide                                  |
| `_class: divider`    | section divider slide                        |
| `_class: middle`     | align the contents to the vertical center    |
| `.comment`           | speech balloon of the character              |
| `.comment.thinking`  | dashed and dimmed balloon                    |
| `.tool`              | tool call line                               |
| `.result`            | tool result line                             |
| `.added` / `.removed`| green / red text                             |
| `.dim` / `.accent`   | dimmed / accent colored text                 |
| `.center` / `.right` | text alignment                               |

Image alignment (`![center]` / `![right]`) works as same as the `kage1020` theme.
Marp background images (`![bg]`, `![bg left:40%]`) are also usable. The content
frame is hidden on the slides using a split background image.

### customize

Every color and metric is a CSS variable, so it can be overridden per deck or per slide.

```markdown
<style>
section {
  --cc-character: url("./avatar.png");
  --cc-character-size: 64px;
  --cc-accent: #d97757;
  --cc-bg: #1f1e1d;
}
</style>
```

| variable                | default   | description                        |
| ----------------------- | --------- | ---------------------------------- |
| `--cc-character`        | asterisk  | image of the character (`none` to hide) |
| `--cc-character-size`   | `56px`    | size of the character              |
| `--cc-bg`               | `#1f1e1d` | slide background                   |
| `--cc-panel`            | `#262624` | prompt box background              |
| `--cc-panel-alt`        | `#302f2c` | balloon / code background          |
| `--cc-border`           | `#3d3b37` | border of the content frame        |
| `--cc-fg`               | `#e8e6df` | text color                         |
| `--cc-dim`              | `#8d887e` | header, footer and page number     |
| `--cc-accent`           | `#d97757` | accent color                       |
| `--cc-gutter`           | `40px`    | horizontal margin of the frame     |
| `--cc-frame-top`        | `94px`    | top position of the content frame  |
| `--cc-frame-bottom`     | `150px`   | bottom position of the content frame |
