---
title: Hopf fibration
---

# Hopf fibration

## 大学受験生の常識

__絶対値が1の複素数で、二次元回転を表すことができる__

$U(1) = \{z \in \mathbf{C} \:\mid |z| = 1 \}$

$SO(2) = \{ R \in Mat(2,\mathbb{R}) \mid R^{T} R = 1 , \det(R) = 1 \}$

$\left(\begin{array}{cc} a & c \\ b & d \end{array} \right) \left(\begin{array}{cc} a & b \\ c & d\end{array} \right) = \left(\begin{array}{cc} a^2+c^2 & ab+cd \\ ab+cd & b^2+d^2 \end{array} \right) = \left( \begin{array}{cc} 1 & 0 \\ 0 & 1\end{array} \right)$

$\det \left(\begin{array}{cc} a & b \\ c & d \end{array} \right) = ad -bc=1$

$\Rightarrow (a-d)^2 + (b+c)^2 = (a^2+c^2)+(b^2+d^2) - 2(ad-bc) = 0$

$\therefore) a=d , b=-c$ かつ $a^2+b^2=1$

$\rho :U(1) \xrightarrow{\sim} SO(2)$

$\rho(z) = \left(\begin{array}{cc} Re(z) & Im(z) \\ -Im(z) & Re(z) \end{array} \right)$

## プログラマの常識

__絶対値が$1$の四元数で、三次元回転を表すことができる__

$\mathbb{H} = \{ x_0  + x_1\mathbf{i} + x_2 \mathbf{j} + x_3 \mathbf{k} \mid x_n \in \mathbb{R} , n=1,2,3 \}$

$\mathbf{i}^2 = \mathbf{j}^2 = \mathbf{k}^2=-1$ , $\mathbf{i}\mathbf{j}=-\mathbf{j}\mathbf{i}=\mathbf{k}$ , $\mathbf{j} \mathbf{k} =-\mathbf{k}\mathbf{j}= \mathbf{i}$ , $\mathbf{k} \mathbf{i} = -\mathbf{i}\mathbf{k}=\mathbf{j}$

$U(1,\mathbb{H}) = \{ x \in \mathbb{H} \:\mid |x|=1 \}$

$SO(3) = \{R \in Mat(3,\mathbb{R}) | R^{T}R = 1 , \det(R)=1 \}$

$\rho : U(1,\mathbb{H}) \to SO(3)$

$\rho(x_0+x_1\mathbf{i} + x_2 \mathbf{j} + x_3 \mathbf{k}) = \left( \begin{array}{ccc} x_0^2 + x_1^2-x_2^2-x_3^2 & 2(x_1x_2-x_0x_3) & 2(x_0x_2+x_1x_3) \\ 2(x_0x_3+x_1x_2) & x_0^2-x_1^2+x_2^2-x_3^2 & 2(-x_0x_1+x_2x_3) \\ 2(x_1x_3 - x_0x_2) & 2(x_2x_3 + x_0x_1) & x_0^2-x_1^2-x_2^2+x_3^2 \end{array} \right)$

$\rho(1) = \rho(-1) = 1$ → $\rho$は、1:1ではない

[__check me__] $\rho(x)^T \rho(x) = 1$ , $\det \rho(x) = 1$  , $\rho(x)\rho(y) = \rho(xy)$ ←頑張って計算すればできるが．．．

## 随伴表現

$\mathbb{H} \simeq \mathbb{R}^4$
なので
$Ad(q) : v \mapsto q v q^{-1} , q \in U(1,\mathbb{H}) , v\in\mathbb{H}$
によって、$Ad : U(1,\mathbb{H}) \to GL(4,\mathbb{R})$
を作れる

[__簡単に分かる__]$Ad(1) = 1$ , $Ad(q^{-1}) = Ad(q)^{-1}$ , $Ad(q_1q_2)=Ad(q_1)Ad(q_2)$

$Ad(q) = \left( \begin{array}{c|ccc} 1 & 0 & 0 & 0 \\ \hline 0 & r_{11} & r_{12} & r_{13} \\ 0 & r_{21} & r_{22} & r_{23} \\ 0 & r_{31} & r_{32} & r_{33} \end{array} \right)$

の形をしていて

$\mathrm{Im}(\mathbb{H}) = \{x_1 \mathbf{i} + x_2 \mathbf{j} + x_3 \mathbf{k} \:\mid x_n \in \mathbb{R} , n=1,2,3 \} \simeq \mathbb{R}^3$

だから

$Ad(q) : q \mapsto q v q^{-1} , q \in U(1,\mathbb{H}) ,v\in \mathrm{Im}(\mathbb{H})$
によって、$Ad : U(1,\mathbb{H}) \to GL(3,\mathbb{R})$
を作れる

自明に
$SO(3) \subset GL(3, \mathbb{R})$
であるけど、
$Ad(U(1,\mathbb{H})) = SO(3)$
が成立する

[__自明じゃない特徴付け__] $Ad$は、$U(1,\mathbb{H})$ の(同値を除いて)唯一の三次元既約表現

## 随伴表現:一般的な"定義"
$\epsilon$を、$\epsilon^2=0$である形式的な変数とする

$X \in \mathfrak{u}(1,\mathbb{H}) \subset \mathbb{H}\Leftrightarrow 1 + \epsilon X \in U(1,\mathbb{H})$ ("定義")

$\Leftrightarrow |1+\epsilon X|=1+\epsilon(X+\bar{X})=1 \Leftrightarrow X \in \mathrm{Im}(\mathbb{H})$
なので
$\mathfrak{u}(1,\mathbb{H}) = \mathrm{Im}(\mathbb{H})$

$Ad : U(1,\mathbb{H}) \to End(\mathfrak{u}(1,\mathbb{H}))$

$Ad(q)v = q v q^{-1}$ $(q \in U(1,\mathbb{H}) , v \in \mathfrak{u}(1,\mathbb{H}))$

$\space$

$X \in \mathfrak{so}(3) \subset Mat(3,\mathbb{R}) \Leftrightarrow 1 + \epsilon X \in SO(3)$ ("定義")

$\Leftrightarrow (1+\epsilon X)^T(1+\epsilon X) = 1+\epsilon (X+X^{T})=1$,
$\det(1+\epsilon X) = 1 + \epsilon \cdot tr(X) = 1$

$\mathfrak{so}(3) = \{ X \in Mat(3,\mathbb{R}) \mid X+X^{T}=0 \}$

$Ad(q): v \mapsto q v q^{-1} \in \mathfrak{so}(3)$ $(q \in SO(3) , v \in \mathfrak{so}(3))$

$\because)qq^{T}=1 \Rightarrow Ad(q)v + (Ad(q)v)^T = qvq^{-1} + (q v q^{-1})^{T} = q(v+v^{T})q^{T}=0$

## Hopf fibration

$U(1,\mathbb{H}) = \{ x \in \mathbb{H} \:\mid |x|=1 \}$

$S^3 = \{ (q_0,q_1,q_2,q_3) \in \mathbb{R}^4 \mid q_0^2+q_1^2+q_2^2+q_3^2=1 \}$

$U(1,\mathbb{H}) \leftrightarrow S^3$ : 一対一対応

$SO(3)$ は二次元球面に作用する

$S^2 = \{(x_1,x_2,x_3) \in \mathbb{R}^3 \mid x_1^2+x_2^2+x_3^2 = 1 \}$

$Ad : U(1,\mathbb{H}) \to SO(3)$
を介して、$U(1,\mathbb{H})$も$S^2$に作用する

$\left( \begin{array}{ccc} q_0^2 + q_1^2-q_2^2-q_3^2 & 2(q_1q_2-q_0q_3) & 2(q_0q_2+q_1q_3) \\ 2(q_0q_3+q_1q_2) & q_0^2-q_1^2+q_2^2-q_3^2 & 2(-q_0q_1+q_2q_3) \\ 2(q_1q_3 - q_0q_2) & 2(q_2q_3 + q_0q_1) & q_0^2-q_1^2-q_2^2+q_3^2 \end{array} \right) \left( \begin{array}{ccc} 1 \\ 0 \\ 0
\end{array} \right) = \left( \begin{array}{c} q_0^2 + q_1^2-q_2^2-q_3^2 \\ 2(q_0q_3+q_1q_2) \\ 2(q_1q_3 - q_0q_2) \end{array} \right)$

$q \in U(1,\mathbb{H}) \simeq S^3 \mapsto Ad(q)(1,0,0)^T \in S^2$
によって、写像
$S^3 \to S^2$
が定まる（Hopf fibration,1931)

[__Hopf fibration__] 現代幾何では、基本的な例

- $S^2$上の非自明な主$U(1)$束

- 高次ホモトピー群$\pi_3(S^2)$の生成元


## 二次元表現とHopf fibration
$\psi(q_0 + q_1 \mathbf{i} + q_2 \mathbf{j} + q_3 \mathbf{k}) = \left( \begin{array}{cc} q_0 + q_1 \it{i} & q_2 + q_3 \it{i} \\ -q_2+q_3 \it{i} & q_0 - q_1 \it{i} \end{array} \right)$


$\psi: U(1,\mathbb{H}) \to GL(2,\mathbb{C})$
は単射で、群準同型である

$SU(2) = \{ U \in Mat(2,\mathbb{C}) \mid U^{\dagger}U = 1 , \det(U)=1 \} = \psi(U(1,\mathbb{H}))$

$S^3 = \{ (\alpha,\beta) \in \mathbb{C}^2 \mid |\alpha|^2 + |\beta|^2 = 1\} \mapsto \left(\begin{array}{cc} \alpha & -\bar{\beta} \\ \beta & \bar{\alpha} \end{array} \right) \in SU(2)$
は1:1写像

$U(1,\mathbb{H}) \to S^2$は既に作ったから

$\pi: S^3 \to SU(2) \to U(1,\mathbb{H}) \to S^2$
を以下のように作れることが分かる

$\pi: (\alpha,\beta) \in S^3 \mapsto (|\alpha|^2 - |\beta|^2 ,-2 \mathrm{Im}(\bar{\alpha}\beta) , 2\mathrm{Re}(\bar{\alpha}\beta)) \in S^2$

$\pi^{-1}(1,0,0) = \{ (\alpha,0) \in \mathbb{C}^2 \mid |\alpha|=1 \} \subset S^3$


## Pauli行列
物理などでは、以下の形をよく使う。

$\sigma_{1} = \left(\begin{array}{cc} 0 & 1 \\ 1 & 0 \end{array}\right)$,
$\sigma_{2} = \left(\begin{array}{cc} 0 & -\textit{i} \\ \textit{i} & 0 \end{array}\right)$,
$\sigma_{3} = \left(\begin{array}{cc} 1 & 0 \\ 0 & -1 \end{array}\right)$

$(x_0,x_1,x_2,x_3) \mapsto x_0 I + \textit{i}x_1\sigma_1 + \textit{i}x_2\sigma_2 + \textit{i} x_3\sigma_3 = \left(\begin{array}{cc} x_0+\textit{i}x_3 & x_2+\textit{i}x_1 \\  -x_2+\textit{i}x_1 & x_0-\textit{i}x_3 \end{array}\right) = X$

$q \in U(1,\mathbb{H}) \mapsto Q = \left(\begin{array}{cc} q_0+\textit{i} q_3 & q_2+\textit{i}q_1 \\  -q_2+\textit{i}q_1 & q_0-\textit{i}q_3 \end{array}\right) \in SU(2)$

と
$X \mapsto QXQ^{-1}$
から
$R:U(1,\mathbb{H}) \to SO(3)$
を以下のようにも作れる

$R(q) = \left( \begin{array}{ccc} q_0^2 + q_1^2-q_2^2-q_3^2 & 2(q_0q_3+q_1q_2) & 2(-q_0q_2+q_1q_3) \\ 2(-q_0q_3+q_1q_2) & q_0^2-q_1^2+q_2^2-q_3^2 & 2(q_0q_1+q_2q_3) \\ 2(q_1q_3 + q_0q_2) & 2(q_2q_3 - q_0q_1) & q_0^2-q_1^2-q_2^2+q_3^2 \end{array} \right)$

$(\alpha,\beta) = (q_0 + \textit{i}q_3 , -q_2+\textit{i}q_1)$
とすれば

$q \mapsto R(q) (0,0,1)^T = (2\mathrm{Re}(\bar{\alpha}\beta) , 2\mathrm{Im}(\bar{\alpha}\beta),|\alpha|^2-|\beta|^2) \in S^2$

## 準備:複素射影直線
$\mathbb{P}^1(\mathbb{C}) = \mathbb{C} \cup \{\infty\}$

[__fact__] $\mathbb{P}^1(\mathbb{C}) \simeq S^2$

$f : \mathbb{P}^1(\mathbb{C}) \to S^2$

$f(z) = \begin{cases} (0,0,-1) & (z=\infty) \\ \left(\dfrac{2 \mathrm{Re}(z)}{1+|z|^2} ,\dfrac{2 \mathrm{Im}(z)}{1+|z|^2},\dfrac{1-|z|^2}{1+|z|^2}  \right) & (z \in \mathbb{C}) \end{cases}$

$g : S^2 \to \mathbb{P}^1(\mathbb{C})$

$g(x_1,x_2,x_3) = \begin{cases} \infty & (x_3=-1) \\ \dfrac{x_1}{1+x_3} + \dfrac{x_2}{1+x_3} \textit{i} & (x_3 \neq -1) \end{cases}$

## 再びHopf fibration
$\pi: (\alpha,\beta) \in S^3 \mapsto (2\mathrm{Re}(\bar{\alpha}\beta),2 \mathrm{Im}(\bar{\alpha}\beta),|\alpha|^2 - |\beta|^2) \in S^2$

$s : \mathbb{C}^2 \setminus \{(0,0)\} \to \mathbb{P}^1(\mathbb{C})$

$s(z_1,z_2) = \begin{cases} z_2/z_1 & (z_1 \neq 0) \\ \infty & (z_1=0) \end{cases}$

$f : \mathbb{P}^1(\mathbb{C}) \to S^2$

$f(z) = \begin{cases} \left(\dfrac{2 \mathrm{Re}(z)}{1+|z|^2} ,\dfrac{2 \mathrm{Im}(z)}{1+|z|^2},\dfrac{1-|z|^2}{1+|z|^2} \right) & (z \in \mathbb{C}) \\ (0,0,-1) & (z=\infty)  \end{cases}$

$f \circ s(z_1,z_2) = \left(\dfrac{2 \mathrm{Re}(\bar{z_1}z_2)}{|z_1|^2+|z_2|^2} ,\dfrac{2 \mathrm{Im}(\bar{z_1}z_2)}{|z_1|^2+|z_2|^2} ,\dfrac{|z_1|^2-|z_2|^2}{|z_1|^2+|z_2|^2}\right)$

$(\alpha,\beta) \in S^3 = \{ (\alpha,\beta) \in \mathbb{C}^2 \mid |\alpha|^2 + |\beta|^2 = 1\}$
に対して

$\pi(\alpha,\beta) = f \circ s(\alpha,\beta)$


## quaternionic Hopf fibration

同様に、
$S^7 \subset \mathbb{H}^2 \setminus \{(0,0)\}$
と見なすことが出来

$\mathbb{P}^1(\mathbb{H}) = \mathbb{H} \cup \{\infty\}$
として

$s_{\mathbb{H}} : \mathbb{H}^2 \setminus \{(0,0)\}\to  \mathbb{P}^1(\mathbb{H})$

$F_{\mathbb{H}} : \mathbb{P}^1(\mathbb{H}) \simeq S^4$

が定義でき、$F_{\mathbb{H}} \circ s_{\mathbb{H}} : \mathbb{H}^2 \setminus \{(0,0)\} \to S^4$
を$S^7$に制限することで、

$\pi_{\mathbb{H}} : S^7 \to S^4$

$\pi_{\mathbb{H}}(z_1,z_2) = (|z_1|^2-|z_2|^2 , 2\bar{z_1}z_2) \in \mathbb{R} \times \mathbb{H} \simeq \mathbb{R}^5$

が得られる。

任意の
$p \in S^4$に対して
$\pi_{\mathbb{H}}^{-1}(p) \simeq U(1,\mathbb{H}) \simeq S^3$


## isomorphisms

$\begin{cases} GL(1,\mathbb{R}) \simeq GL_{+}(1,\mathbb{R}) \times \{\pm 1\} & , x \mapsto \left(|x|,x/|x| \right) \\ GL(1,\mathbb{C}) \simeq GL_{+}(1,\mathbb{R}) \times U(1) & , x \mapsto \left(|x|,x/|x|\right) \\ GL(1,\mathbb{H}) \simeq GL_{+}(1,\mathbb{R}) \times U(1,\mathbb{H}) & , x \mapsto \left(|x|,x/|x|\right) \end{cases}$

$\mathbb{C}^2\setminus\{\mathbf{0}\} \to S^3 \simeq (\mathbb{C}^2\setminus\{\mathbf{0}\})/GL_{+}(1,\mathbb{R}) \to S^2 \simeq \mathbb{P}^{1}(\mathbb{C}) \simeq (\mathbb{C}^2\setminus\{\mathbf{0}\})/GL(1,\mathbb{C}) \simeq S^3/U(1)$

$\mathbb{H}^2\setminus\{\mathbf{0}\} \to S^7 \simeq (\mathbb{H}^2\setminus\{\mathbf{0}\})/GL_{+}(1,\mathbb{R}) \to S^4 \simeq \mathbb{P}^{1}(\mathbb{H}) \simeq (\mathbb{H}^2\setminus\{\mathbf{0}\})/GL(1,\mathbb{H})  \simeq S^7/U(1,\mathbb{H})$

[__一般化__]

$\begin{cases} S^{n}/\{\pm 1\} \simeq \mathbb{P}^{n}(\mathbb{R}) \\ S^{2n+1}/U(1) \simeq \mathbb{P}^{n}(\mathbb{C}) \\ S^{4n+3}/U(1,\mathbb{H}) \simeq \mathbb{P}^{n}(\mathbb{H}) \end{cases}$


[__おまけ__]以下は全部2:1写像

$\begin{cases} SL(2,\mathbb{R}) \to SO(2,1)=\mathrm{Conf}(S^1) \\ SL(2,\mathbb{C}) \to SO(3,1)=\mathrm{Conf}(S^2) \\ SL(2,\mathbb{H}) \to SO(5,1)=\mathrm{Conf}(S^4) \end{cases}$
