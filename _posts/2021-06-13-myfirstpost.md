# fast_templateを使ってブログを書く

[このページ](https://www.fast.ai/2020/01/16/fast_template/)を参照しています。

目次は、番号の箇条書きを表す 1. の後に、TOC と書く：

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

アスタリスクで挟むと*イタリック*、アスタリスク２つで挟むと**ボールド**、１重引用符で挟むと'コードフォント文字'、
角かっこでリンク名を挟み、その後ろに丸かっこの中にurlを書くと、リンクを作ることができる：[マークダウンガイドへのリンク](https://www.markdownguide.org/cheat-sheet/)　
脚注はキャレット＋数字を角かっこに入れたもので表す。 [^1]
横罫線は３つのハイフンで書ける。

---

## 箇条書き

箇条書きは、-(ハイフン)で書ける:

- アイテム 1
- アイテム 2

番号の箇条書きは、1. (1とピリオド)で書ける:

1. アイテム 1
1. アイテム 2

## 引用や箱など

引用は、> で始める：

> これは引用です。

警告ボックスは、include alert.html text="箱に入れたい文字" を、中かっこ+%で囲む。

{% include alert.html text="警告ボックス" %}

情報ボックスは、include info.html text="箱に入れたい文字" を、中かっこ+%で囲む。

{% include info.html text="情報ボックス" %}

## 画像

!と[] の後に、丸括弧で画像ファイルのパスとキャプションを書く。

![](/images/logo.png "fast.aiのロゴ")

## コード

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

## 表

縦棒とハイフンを使って書く。

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |

## Footnotes

脚注はキャレット＋数字を角かっこに入れたもので表す。

[^1]: 脚注です。

## 数式

_config.yml の use_math を true にする。

    # Set this to true to get LaTeX math equation support
    use_math: true

すると、tex記法で数式が書ける。KaTeXというものが使われているっぽい。
https://katex.org/docs/supported.html

VS Code の機能拡張で、Markdown Preview Enhanced をインストールすると、Previewも数式に変換されるので便利。このプレビューを見るには、エディター上で右クリックをして、Markdown Preview Enhancedを選択する。