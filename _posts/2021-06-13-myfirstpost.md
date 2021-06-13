# ブログのタイトル

目次です：

1. TOC
{:toc}

## 基本的な設定

ブログ記事のファイル名のフォーマットは以下のようにする必要がある:

`YEAR-MONTH-DAY-filename.md`

ここで、 `YEAR` は４桁の数字で、 `MONTH` と `DAY` は２桁の数字で、 `filename` はどのような名前でもよい。 `.md` はマークダウンファイルの拡張子。

ファイルの最初の行は、#で始まり、空白文字を入れて、ブログのタイトル、というものである必要がある。
これは "*レベル1の見出し*" をマークダウンで書く方法である。
#を２個以上つけると、レベル2, 3 などの見出しが書ける。
（上で使っている`## 基本的な設定`のように。）

## 基本フォーマット

で挟むと*イタリック*、**ボールド**、'コードフォント文字'、[リンク](https://www.markdownguide.org/cheat-sheet/)　を作ることができる。
脚注は [^1]
罫線は、

---

## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![](/images/logo.png "fast.ai's logo")

## Code

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |

## Footnotes

[^1]: This is the footnote.

