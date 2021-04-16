<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

## 応用数学
### 第1章：線形代数

固有値固有ベクトルについては学部抗議にて履修済み。

#### 特異値分解

$m \times n$行列$M$に対して次のような表記をした場合の$\Gamma$の対角成分を$M$の**特異値**という

$$
M = U\Gamma V^T
$$

またこの時の$U,V$を$U=(u_1,u_2,\dots),V=(v_1,v_2,\dots)$としたときの$u_i$を**左特異ベクトル**といい、$v_i$を**右特異ベクトル**という。


この時に以下の関係が成立する。

$$
M\boldsymbol{v}=\sigma\boldsymbol{u}\\
M^T\boldsymbol{u}=\sigma\boldsymbol{v} 
$$

ここから

$$
M^TM\boldsymbol{v}=\sigma M^T\boldsymbol{u}=\sigma^2\boldsymbol{u}\\
MM^T\boldsymbol{u}=\sigma M^T\boldsymbol{v}=\sigma^2\boldsymbol{v}
$$


よって、特異値ベクトル$u,v$はそれぞれ$MM^T,M^TM$の固有ベクトルであり、固有値は$\sigma^2$になる。


### 第2章：確率・統計
### 第3章：情報理論

