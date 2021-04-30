<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

## 機械学習
### 線形回帰モデル

- 機械学習（前半）　17:35~

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

\begin{split} 
&\frac{\partial}{\partial \boldsymbol{w}} J(\boldsymbol{w}) = 0 \cr 
\Leftrightarrow &\frac{\partial}{\partial \boldsymbol{w}} \frac{1}{n}\sum_{i} (\hat{y}_{i}-y_{i})^2 = 0 \cr 
\Leftrightarrow &\frac{\partial}{\partial \boldsymbol{w}} \frac{1}{n}\sum_{i} (\boldsymbol{x}_i^T \cdot\boldsymbol{w}-y_{i})^2 = 0 \cr 
\Leftrightarrow &\frac{\partial}{\partial \boldsymbol{w}} \frac{1}{n}(X\boldsymbol{w}-\boldsymbol{y})^T(X\boldsymbol{w}-\boldsymbol{y}) = 0 \cr 
\Rightarrow &\frac{1}{n}(2X^TX\boldsymbol{w}-2X^T\boldsymbol{y}) = 0 
\end{split}


### ロジスティック回帰モデル
### 主成分分析
### アルゴリズム
### サポートベクターマシン
