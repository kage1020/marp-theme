---
marp: true
theme: claude-code
paginate: true
---

<!--
_class: cover
_paginate: false
-->

# Claude Code Theme for Marp

## ターミナルのようにスライドを書く

kage1020 / 2026

---

<!--
_class: divider
_paginate: false
-->

## getting-started

---

<!--
header: Layout
footer: claude-code theme
-->

# このスライドのレイアウト

<p class="comment">スライドの各パーツはこんな配置になっているよ！</p>

- 左上: キャラクターと `.comment` の吹き出し
- 右上: `header`
- 中央: コンテンツ（枠線の内側）
- 下部: プロンプト入力欄に `#` の見出し（タイトル）
- 左下: `footer` / 右下: ページ番号

---

# 書き方

<p class="comment">フロントマターはこれだけ。</p>

```markdown
---
marp: true
theme: claude-code
paginate: true
header: Chapter Title
footer: Sub Title
---

# プロンプト欄に出したいタイトル

<p class="comment">キャラクターのひとこと</p>

本文をここに書きます。
```

---

<!--
_class: middle
-->

# 縦方向の中央寄せ

<p class="comment"><code>_class: middle</code> でコンテンツを上下中央に配置できるよ。</p>

短いスライドは中央寄せにすると収まりが良いです。

---

# テキストの装飾

<p class="comment">よく使う記法をまとめておくね。</p>

**太字** は明るい色、*斜体* はアクセントカラー、`inline code` はコードカラー。

[リンク](https://github.com/kage1020/marp-theme) は青、<mark>マーク</mark> はハイライト。

キー操作は <kbd>Ctrl</kbd> + <kbd>C</kbd> のように書けます。

> 引用は左側にアクセントバーが付きます。

<cite>Someone famous in Source Title</cite>

---

# リストと見出し

## 見出し 2

- 第 1 階層
  - 第 2 階層
    - 第 3 階層

### 見出し 3

1. 番号付きリスト
2. 番号付きリスト

---

# コードブロック

```ts
// シンタックスハイライトはダークテーマに合わせています
export function greet(name: string): string {
  const message = `Hello, ${name}!`;
  console.log(message);
  return message;
}
```

---

# テーブル

| Command   | Description             | Shortcut          |
| --------- | ----------------------- | ----------------- |
| `/init`   | CLAUDE.md を生成する    | -                 |
| `/clear`  | 会話履歴をクリアする    | <kbd>Ctrl</kbd>+L |
| `/review` | 変更をレビューする      | -                 |

---

# ツール実行風の表示

<p class="comment">エージェントのログっぽい見た目も作れるよ。</p>

<p class="tool">Read(slides.md)</p>
<p class="result">Read 128 lines</p>

<p class="tool">Edit(slides.md)</p>
<p class="result"><span class="added">+ 12 lines</span> / <span class="removed">- 3 lines</span></p>

<p class="dim">補足のテキストは .dim で控えめにできます。</p>

---

# 画像

<p class="comment thinking">考え中のときは .thinking を付けると点線になるよ…</p>

![center w:520](https://fastly.picsum.photos/id/572/600/400.jpg?hmac=3_xPFtsTox_qOMEQHVdd3m_cGlmM0lVdL9Y7WtWbNYo)

---

# キャラクターを差し替える

<p class="comment">自分のアイコンにもできるよ。</p>

```markdown
<style scoped>
section {
  --cc-character: url("./avatar.png");
  --cc-character-size: 64px;
}
</style>
```

`--cc-character: none` で非表示にもできます。
