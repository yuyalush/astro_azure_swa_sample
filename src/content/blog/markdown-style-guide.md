---
title: 'Markdown Style Guide'
description: 'Astro で Markdown コンテンツを書く際に使用できる基本的な Markdown 構文のサンプル集です。'
pubDate: 'Jun 19 2024'
heroImage: '../../assets/blog-placeholder-1.jpg'
---

Astro で Markdown コンテンツを書く際に使用できる基本的な Markdown 構文のサンプルです。

## 見出し

HTML の `<h1>`—`<h6>` 要素は、セクション見出しの 6 つのレベルを表します。`<h1>` が最上位、`<h6>` が最下位のレベルです。

# H1

## H2

### H3

#### H4

##### H5

###### H6

## 段落

これは段落のサンプルテキストです。段落を作成するには、テキストをそのまま行に書くと、Markdown が自動的に段落要素として扱います。空白行で区切ることで複数の段落を作成できます。

段落は文章の基本単位です。長すぎる内容は辺高をの空白行で複数の段落に分割すると読みやすい文章になります。

## 画像

### 構文

```markdown
![Alt text](./full/or/relative/path/of/image)
```

### 出力

![blog placeholder](../../assets/blog-placeholder-about.jpg)

## 引用

ブロック引用要素は、別のソースから引用したコンテンツを表します。任意で、`footer` または `cite` 要素内に出典を記載したり、注釈や略語などのインライン変更を加えたりすることができます。

### 出典なしの引用

#### 構文

```markdown
> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Note** that you can use _Markdown syntax_ within a blockquote.
```

#### 出力

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Note** that you can use _Markdown syntax_ within a blockquote.

### 出典ありの引用

#### 構文

```markdown
> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>
```

#### 出力

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: 上記の引用は、2015年11月18日の Gopherfest における Rob Pike の[トーク](https://www.youtube.com/watch?v=PAAkCSZUG1c)からの抜粋です。

## テーブル

### 構文

```markdown
| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |
```

### Output

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

## コードブロック

### 構文

3つのバックティック ( ``` ) を新しい行に書き、コードを記述し、再度 3 つのバックティックで閉じることでコードブロックを作成できます。言語固有のシンタックスハイライトを有効にするには、最初の 3 つのバックティックの直後に言語名を一単語で記述します（例: html, javascript, css, markdown, typescript, txt, bash）

````markdown
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```
````

### 出力

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

## リストの種類

### 番号付きリスト

#### 構文

```markdown
1. First item
2. Second item
3. Third item
```

#### 出力

1. First item
2. Second item
3. Third item

### 箇条書きリスト

#### 構文

```markdown
- List item
- Another item
- And another item
```

#### 出力

- List item
- Another item
- And another item

### ネストしたリスト

#### 構文

```markdown
- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese
```

#### 出力

- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese

## その他の要素 — abbr, sub, sup, kbd, mark

### 構文

```markdown
<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
```

### 出力

<abbr title="Graphics Interchange Format">GIF</abbr> はビットマップ画像形式です。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> でセッションを終了します。

ほとんどの <mark>サンショウウオ</mark> は夜行性で、昆虫・ミミズ・その他の小さな生き物を捕食します。
