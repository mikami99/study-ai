<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>


## Githubpagesでマークダウン書き方メモ

### リンクの書き方

リンクしたいとき基本的に以下のように書く

```markdown
[表示](リンク先)
```

#### 外部リンク

外部サイト、たとえば[Google](https://google.com)へのリンク

```markdown
外部サイト、たとえば[Google](https://google.com)へのリンク
```

#### 内部リンク

同じPages内のリンクは相対パスでmdファイル(htmlファイル)を指定する

たとえば[GithubPages設定の記事](./githubpages_setting.md)へのリンク

```markdown
たとえば[GithubPages設定の記事](./githubpages_setting.md)へのリンク
```

### タグのかきかた

使いそうなタグ

#### hタグ

- ↑「Githubpagesでマークダウン書き方メモ」はh2
- ↑「タグのかきかた」はh3
- ↑「hタグ」はh4

自動生成されるリンク（リポジトリ名表示でPagesのtopへのリンク）がh1で作成されるから自分で書くのはh2からにする。
orセクションタグ入れてちゃんと構造化するとh1からでもいい気がするけどhtml5詳しくないからわからん

```markdown
## Githubpagesでマークダウン書き方メモ
### タグのかきかた
#### hタグ
```

#### テーブル

[テーブルジェネレータ](https://www.tablesgenerator.com/markdown_tables) が優秀

|へっだ１|へっだ２|
|-------|-------|
|でーた１|でーた２|

```markdown
|へっだ１|へっだ２|
|-------|-------|
|でーた１|でーた２|
```

#### リスト

- ul
- ul
    - 子階層ul
    - 子階層ul
- ul
    1. 子階層ol
    1. 子階層ol

````markdown
- ul
- ul
    - 子階層ul
    - 子階層ul
- ul
    1. 子階層ol
    1. 子階層ol
````



