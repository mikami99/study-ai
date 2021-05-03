<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

## 機械学習
### 線形回帰モデル

- 機械学習（前半）　17'35"~

連続値の入力から、連続値の出力を予想する以下のモデル

$$
\hat{y} = \boldsymbol{w}^T \boldsymbol{x} = w_0 + \sum_{j=1}^{m}{w_j x_j} 
$$

$\hat{y}$の記法は、慣例として**予測値**を表す。ここでの目標は$\boldsymbol{w}$を確定し、未知の$\boldsymbol{x}$に対する$\hat{y}$が求められるようになることであり、$\boldsymbol{w}$決定に**最小二乗法**を用いる。

#### 最小二乗法

**平均二乗誤差（Mean Squared Error）**を最小にするようにする。

※MSEは外れ値の影響が大きく出るので注意。

MSEは以下のようにあらわされる。

$$
J(\boldsymbol{w}) = \frac{1}{n}\sum_{i} (\hat{y}_{i}-y_{i})^2
$$


この時に$J(\boldsymbol{w})$を最小とするような$\boldsymbol{w}=\boldsymbol{\hat{w}}$を求める

$$
\boldsymbol{\hat{w}} = argmin(J(\boldsymbol{w}))
$$

最小にするとは、勾配が0であること。

$$
\begin{split} 
&\frac{\partial}{\partial \boldsymbol{w}} J(\boldsymbol{w}) = 0 \cr 
\Leftrightarrow &\frac{\partial}{\partial \boldsymbol{w}} \frac{1}{n}\sum_{i} (\hat{y}_{i}-y_{i})^2 = 0 \cr 
\Leftrightarrow &\frac{\partial}{\partial \boldsymbol{w}} \frac{1}{n}\sum_{i} (\boldsymbol{x}_i^T \cdot\boldsymbol{w}-y_{i})^2 = 0 \cr 
\Leftrightarrow &\frac{\partial}{\partial \boldsymbol{w}} \frac{1}{n}(X\boldsymbol{w}-\boldsymbol{y})^T(X\boldsymbol{w}-\boldsymbol{y}) = 0 \cr 
\Rightarrow &\frac{1}{n}(2X^TX\boldsymbol{w}-2X^T\boldsymbol{y}) = 0 \cr
\Rightarrow &\boldsymbol{w} = (X^TX)^{-1} X^T\boldsymbol{y}
\end{split} 
$$

#### ハンズオン

- 機械学習（前半）　2:13'00"~

### 非線形回帰モデル

直線ではない回帰を行う。二次関数や三次関数。三角関数などなど

$$
\begin{split} 
y &= w_0 + w_1 x + w_2 x^2 + \cdots + x_n x^n \cr
y &= w_0 + w_1 \sin(x) + w_2\cos(x)
\end{split} 
$$

つまり、任意の$x$の関数$\phi(x)$を用いて以下のように書けるもの

$$
y = w_0 + w_1 \phi_1(x) + \cdots + w_n \phi_n(x)
$$

これは$\boldsymbol{w}=(w_0,\cdots,w_n)^T$に関しては線形である。(linear-in-parameter)

### ロジスティック回帰モデル
### 主成分分析
### アルゴリズム
### サポートベクターマシン
