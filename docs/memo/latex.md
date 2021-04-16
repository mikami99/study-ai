<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

## LaTeXの基本的なアレ

書き方とか。ただしGithubpagesで今回の手順においてなので常にこれで想定の表記になるとは限らん。

### 数式

インラインで例えばこんな数式$y=f(x)$を書きたいときは"$"で囲む。

```markdown
インラインで例えばこんな数式$y=f(x)$を書きたいときは"$"で囲む。
```

独立行で書くなら"$$"で囲む

$$
x = \frac{-b\pm \sqrt{b^2-4ac}}{2a}
$$

```markdown
独立行で書くなら"$$"で囲む

$$
x = \frac{-b\pm \sqrt{b^2-4ac}}{2a}
$$
```

行を変えたいなら全体がeqnarrayの中で\crする。そろえたい部分があれば"&"で囲む。

\begin{eqnarray}
x^2 + 3 &=& 4x - 8 \cr
x^2 -4x + 3 -8 &=& 0 \cr
x^2 -4x - 5  &=& 0 \cr
(x - 5)(x + 1) &=& 0 \cr
x &=& -1,5 
\end{eqnarray}


```markdown
\begin{eqnarray}
x^2 + 3 &=& 4x - 8 \cr
x^2 -4x + 3 -8 &=& 0 \cr
x^2 -4x - 5  &=& 0 \cr
(x - 5)(x + 1) &=& 0 \cr
x &=& -1,5 \cr 
\end{eqnarray}
```


