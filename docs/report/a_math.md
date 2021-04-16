<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

## 応用数学
### 第1章：線形代数

固有値固有ベクトルについては学部講義にて履修済み。

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

#### 期待値と分散

確率分布$f(X)$に対して、期待値$E(X)$と、分散$Var(X)$は以下のように与えられる。

\begin{eqnarray}
E(X) &=& \int xf(x)dx \cr
Var(X) &=& E(x^2)-(E(x))^2 
\end{eqnarray}

#### 各種分布

| 分布名           | 分布$f(X)$                                                         | 概要                 | 
| ---------------- | ------------------------------------------------------------------ | -------------------- | 
| ベルヌーイ分布   | $\mu ^x (1-\mu)^{1-x}$                                             | 二値をとる離散       | 
| マルチヌーイ分布 |                                                                    | 複数の結果をとる離散 | 
| 二項分布         | $\frac{n!}{x!(n-x)!}\lambda ^x (1-\lambda)^{n-x}$                  | ベルヌーイを複数回   | 
| ガウス分布       | $\sqrt{\frac{1}{2\pi\sigma^2}}\exp{-\frac{1}{2\sigma^2}(x-\mu)^2}$ | 釣鐘<br>偏差値のやつ | 


### 第3章：情報理論

#### 情報量

$$
I(x) = -\log(P(x))
$$

対数の底が2の場合、情報量$I$の単位は[bit]

#### シャノンエントロピー

情報量の期待値で、起こりやすさの指標になりうる

\begin{eqnarray}
H(x) &=& E\left[I(X)\right] \cr
&=& -\sum (P(x)\log(P(x)))
\end{eqnarray}

#### カルバック・ライブラー　ダイバージェンス

二つの確率分つ$P,Q$の差分の指標

$$
D_{KL}(P||Q)= \mathbb{E}_{x\sim P}\left[\log\frac{P(x)}{Q(x)}\right]
$$


#### 交差エントロピー

$Q$の自己情報量を$P$の分布から表現

\begin{eqnarray}
H(P,Q) &=& H(P) + D_{KL}(P||Q) \cr
&=& -\mathbb{E}_{x\sim P}\log Q(x)
\end{eqnarray}
