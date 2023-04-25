# marp-theme
my customized marp theme

## Usage

### custom color

```css
:root {
    --primary-color: #368F8B;
    --secondary-color: #160F29;
    --tertiary-color: #F3DFC1;
    --primary-dark-color: #246A73;
    --tertiary-dark-color: #DDBEA8;
}
```

### cover slide

```markdown
<!--
_class: cover
-->
```

![cover design](.docs/cover.png)

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

### TODO slide (for WIP)

```markdown
---
<!--
header: Title for Chapter
footer: Sub Title for Sub Chapter
paginate: true
_class: todo
-->
```

![TODO design](.docs/todo.png)

### image alignment

#### centering

```markdown
![center](image.pnghttps://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)
```

![centering image](.docs/center.png)

#### right aligned

```markdown
![right](image.pnghttps://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)
```

![right aligned image](.docs/right.png)

### DOM display type

```css
.flex {
    display: flex;
    justify-content: center;
    align-items: center;
}

.grid {
    display: grid;
    place-items: center;
}

.grid-cols-4 {
    grid-template-columns: repeat(4, minmax(0, 1fr));
}
```

```markdown
<div class="flex">
    <ul>
        <li>Content 1</li>
        <li>Content 2</li>
        <li>Content 3</li>
    </ul>
    <ul>
        <li>Content 4</li>
        <li>Content 5</li>
        <li>Content 6</li>
    </ul>
</div>
```
