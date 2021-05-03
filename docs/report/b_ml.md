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

---
### 非線形回帰モデル

- 機械学習（後半）　0:00'00"~

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

この$\phi_i(x)$を基底関数という。よく使われるものとしては以下の通り。

|基底関数|関数型|
|---|---|
|多項式|$\phi_j(x)=x^j$|
|ガウス基底|$\phi_j(x)=\exp\left\\{ -\frac{(x-\mu_j)^2}{2h_j} \right\\}$|
|スプライン関数||

※基底関数は完全系を張る必要があるのか？？


- 入力値 : $\boldsymbol{x}\_{i}=(x\_{i0},\cdots,x\_{im})\in \mathbb{R}^m , i = (1,\cdots, n)$  
- 非線形関数ベクトル : $\boldsymbol{\phi(\boldsymbol{x}_i)} =(\phi_0(\boldsymbol{x}_i),\cdots,\phi_k(\boldsymbol{x}_i))^T \in \mathbb{R}^k$
- 非線形関数計画行列 : $\Phi =(\boldsymbol{\phi}(\boldsymbol{x}_1),\cdots,\boldsymbol{\phi}(\boldsymbol{x}_m)^T \in \mathbb{R}^{m\times k}$
- 最尤法での予測 : $\hat{\boldsymbol{y}} = \Phi(\Phi^T \Phi)^{-1} \Phi^T \boldsymbol{y}$

#### 未学習と過学習

未学習とは、関数の自由度が低すぎて情報を表現しきれていない状態。より自由度の高い基底で表現することで解決できる。


過学習は、自由度が高すぎて訓練データに対してのみ極端にフィットしてしまっている状態。以下のような対応を行う。

- 学習データ数を増やす
- 不要な規定を削除して自由度を落とす
- **正則化**の利用

#### 正則化

モデルの複雑化に伴って値が大きくなる**正則化項**$R(\boldsymbol{w})$を導入する。正則化項の寄与度合を決めるパラメータ$\gamma > 0$を用いて


$$
S_{\gamma}=(\boldsymbol{y}-\Phi\boldsymbol{w})^T(\boldsymbol{y}-\Phi\boldsymbol{w})+\gamma R(\boldsymbol{w})
$$

---
### ロジスティック回帰モデル
---
### 主成分分析
---
### アルゴリズム
---
### サポートベクターマシン
