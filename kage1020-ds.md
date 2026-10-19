---
marp: true
theme: kage1020-ds
paginate: true
_class: cover
_paginate: false
---

# kage1020 デザインシステムの Marp テーマ

## 静かで、迷わせず、手を止めさせない

<p class="name">kage1020</p>
<p class="organization">2026年10月19日</p>

---

<!--
_class: appendix
_paginate: false
-->

## 区切りのスライド

---

<!--
header: 章のタイトル
footer: 節のタイトル
-->

## 通常のスライド

題の下に hairline を 1 本だけ引く。太さを持つのは題だけで、本文は `body` の 400。

- 色味は `accent` ひとつ、信号は `danger` ひとつ
- 影・ぼかし・グラデーションは使わない
  - 境界は面差しか hairline のどちらか
  - 角は小さく揃える

---

### h3 の見出し

1. 番号は等幅の `mono` で組む
2. 印と番号は `ink-muted` にして本文より退かせる
3. 行長は 40em 程度まで

**強調**は太さで、<mark>元の文の該当箇所</mark>は `mark` の印で示す。リンクは[下線](https://github.com/kage1020/marp-theme)で示す。

---

## コード

アドレス・パス・コマンドは `mono`。キー操作は <kbd>⌘</kbd> + <kbd>Z</kbd> のように書く。

```ts
// コメントは ink-muted、文字列と数値は accent
export function greet(name: string, count = 3): string {
  return `こんにちは、${name}さん`.repeat(count);
}
```

---

## 表

| 名前 | 場所 | 鉢の数 |
| :--- | :--- | -----: |
| モンステラ | 温室 A | 12 |
| パキラ | 窓辺 | 3 |
| ポトス | 棚の上 | 128 |

右揃えの列は数値とみなし、等幅で桁を揃える。縞と縦線は使わない。

---

## 引用と出典

> 明るい日陰に置き、土の表面が乾いたらたっぷり水を与える。

<cite>植物の観察ノート</cite>
<cite class="right"><https://github.com/kage1020/marp-theme></cite>

---

## 画像（中央）

![center h:400](https://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)

<p class="caption">キャプションは meta の ink-muted</p>

---

## 画像（右）

![right w:480](https://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)

画像は右に寄せ、文はその左に回り込む。

動画にも同じ指定が使える。

---

## 枠で囲む箱は 2 つだけ

<div class="callout">

入力のまとまりや手順など、ひとまとまりで読ませたいもの。

</div>

<div class="callout danger">

**確認が必要な事柄**だけに使う。地は `danger-soft`、文は `ink` のまま。

</div>

---

## 色見本

<code class="color" style="--color: #2d70b3">accent #2d70b3</code>
<code class="color" style="--color: oklch(0.577 0.245 27.325)">danger</code>
<code class="color" style="--color: #ffeab2">mark #ffeab2</code>

<p class="meta">補足は .meta で ink-muted の小さい文字にする</p>

<p class="before-right-arrow">矢印に続けて、結論や次の一手を書く。</p>

---

<!--
_class: dark
-->

## ダークテーマ

`class: dark`（または `invert`）で、同じ役割名のまま dark の値に切り替わる。

```sh
# コメント
$ npx @marp-team/marp-cli --html --theme-set kage1020-ds.css kage1020-ds.md
```

| 項目 | 値 |
| :--- | --: |
| 角丸 | 14 |

---

<!--
_class: cover dark
_paginate: false
_header: ""
_footer: ""
-->

# ありがとうございました

<p class="name">kage1020</p>
