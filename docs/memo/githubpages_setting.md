## Githubpages設定とか

アカウント取得は省略

### 基本的なところまで

1. アカウント取得
2. リポジトリ作成(自分はPublicにしたけどPrivateでもできるかも？)
3. ローカルと良しなにつなぐ

### pages用のディレクトリ作成と設定

1. 適当にREADME.mdとか作ってコミットしとく。Masterでもmainでもお好きな名前でどうぞ。
2. フォルダ「docs」をプロジェクト直下に作る。ファイルゼロはコミットできない
3. SettingsのPagesから、ブランチとdocs使う設定選んでSave

### mathjax

mdファイルトップに以下の記載を入れる。

```html
<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>
```
