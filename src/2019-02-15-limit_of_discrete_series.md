---
title: su(1,1)のlimit of discrete series
---
# su(1,1)のlimit of discrete series

## limit of discrete series

$V=\mathbb{C}[z,z^{-1}]$
に対して、$V$上の表現
$\rho : \mathfrak{sl}(2,\mathbb{C}) \to End(V)$
を、以下で定義する。

$\rho(e) = z^2 \dfrac{d}{dz} + z$

$\rho(f) = -\dfrac{d}{dz}$

$\rho(h) = 2 z \dfrac{d}{dz} + 1$

ここで、$e,f,h$は、以下の条件を満たすChevalley基底とする

$[h,e]=2e , [h,f]=-2 f , [e,f] = h$

初等的な計算で、

$\begin{cases} \rho(h)z^n = (2n+1)z^n \\ \rho(e) z^n = (n+1) z^{n+1} \\ \rho(f)z^n = -n z^{n-1} \end{cases}$

が分かる。

 &nbsp;

$(\rho,V)$が$\mathfrak{sl}(2,\mathbb{C})$の表現を定めることは容易にわかるが、既約ではなく、以下の2つの不変部分空間を持つ。

$V_{+} = \mathbb{C}[z]$

$V_{-} = z^{-1}\mathbb{C}[z^{-1}]$

$V_{+}$,$V_{-}$それぞれへの$\mathfrak{sl}(2,\mathbb{C})$の表現は、limit of discrete seriesとして知られる表現になっている。

$(\rho,V)$は、連続主系列表現の一つであり、連続主系列表現は、殆どの場合は、既約になるけど、これは、そうでない。

反線形写像$\theta: \mathfrak{sl}(2,\mathbb{C}) \to \mathfrak{sl}(2,\mathbb{C})$を

$\theta(e) = f , \theta(f) = e , \theta(h)=-h$

で定めると、$\theta$の固定点は、実Lie環を定義する。このLie環は、$\mathfrak{su}(1,1)$

次に、$V$上の内積を

$(z^n,z^m) = \delta_{nm}$

で定めると、$v,w \in V$と$x \in \mathfrak{sl}(2,\mathbb{C})$に対して

$(\theta(x) v , w ) + (v , \theta(x)w) = 0$

が成立する。

$V$自体は、この内積について完備ではないけれど、
$z \mapsto e^{i \theta}$によって、

$\mathbb{C}[z,z^{-1}] \hookrightarrow L^2(S^1)$

が定義できる。これは、単射であり、また、

$(f(z) , g(z)) = \dfrac{1}{2\pi}\displaystyle \int_{0}^{2\pi} f(e^{i\theta})\overline{g(e^{i \theta})} d\theta$

で、内積を保つ。

## Poisson積分

$V=\mathbb{C}[z,z^{-1}]$と、$\mathbb{C}[w] \oplus \bar{w} \mathbb{C}[\bar{w}]$
の間には、自然な(ベクトル空間としての同型が存在する)。

更に、
$\mathbb{C}[w] \oplus \bar{w} \mathbb{C}[\bar{w}]$
と、二変数調和多項式の全体
$\mathcal{H} = \{f \in \mathbb{C}[x,y] | \Delta f = 0 \}$
には、
$(w,\bar{w}) \mapsto (x+iy , x- iy)$
によって、1:1対応が存在する。

$V$から、$\mathcal{H}$への写像は、解析的には、Poisson積分で与えることができる。解析的な文脈では、Poisson積分は、単位円板$D= \{ z \in \mathbb{C} | |z| < 1 \}$の境界$\partial D \simeq S^1$上の関数から、$D$上の調和関数への写像と見なされる

Poisson核を形式的に、

$P(z,w) = \displaystyle \sum_{n=0}^{\infty}　z^n \bar{w}^n + \displaystyle \sum_{n=1}^{\infty} z^{-n} w^n$

とすれば

$P(e^{i \theta} , w) = \dfrac{1}{1-e^{i\theta}\bar{w}} + \dfrac{e^{- i\theta}w}{1-e^{-i\theta}w} = \dfrac{1-|w|^2}{|1-e^{-i\theta}w|^2} = \dfrac{1-|w|^2}{|w-e^{i\theta}|^2}$

となり、通常のPoisson核を得ることが出来る


##　Cayley変換

単位円板は、上半平面$\mathbb{C}_{+} = \{ z \in \mathbb{C} | \mathrm{Im}(z) > 0\}$からの等角全単射を持つ。$\mathbb{C}_{+}$の境界は、$\mathbb{R}$である。

上半平面から、単位円板への全射

$z \mapsto \dfrac{z-i}{z+i}$

は、Cayley変換として知られる。

$n \in \mathbb{Z}$に対して

$z^n \mapsto v_{n}(x)=\dfrac{1}{\sqrt{\pi}} \dfrac{1}{x+i}\left( \dfrac{x-i}{x+i}\right)^n$

$H' = -i(1+x^2)\dfrac{d}{dx}-ix$

$E' = \dfrac{1}{2i}(x-i)^2 \dfrac{d}{dx} + \dfrac{1}{2i}(x-i)$

$F' = \dfrac{i}{2} (x+i)^2 \dfrac{d}{dx} + \dfrac{i}{2}(x+i)$

とすると

$H' \cdot v_n = (2n+1) v_n$

$E' \cdot v_n = (n+1) v_{n+1}$

$F' \cdot v_n = -n v_{n-1}$

こうして、再び、limit of discrete seriesの実現を得る。$v_n(x)$に、広く使われる名前は、付いていないようだけど、Wienerの有理関数と呼ばれていることがある

歪エルミート共役を取る操作$\theta'$は、以下で定まる

$\theta'(H') = -H' , \theta'(E') = F' , \theta'(F') = E'$

そして、$\theta'$の固定点は、以下の元の実係数の線型結合で与えられる

$H = -(E'+F') = 2 \dfrac{d}{dx} + 1$

$E = \dfrac{1}{2}(iH' + iE' - iF') = x^2 \dfrac{d}{dx} + x$

$F = -\dfrac{1}{2}(iH' - i E' + iF') = -\dfrac{d}{dx}$

$g = \left(\begin{array}{cc} a & b \\ c & d \end{array}\right) \in SL(2,\mathbb{R})$の$L^2(\mathbb{R})$への作用を

$\rho(g)(f)(x) =  \dfrac{1}{cx+d}f\left(\dfrac{ax+b}{cx+d}\right)$

で定める時、無限小作用は、$H,E,F$の線形結合で与えられる

## Laguerre関数

$v_n(x)$は、Fourier変換すると、スケーリングと定数倍を除いて、Laguerre関数に移る

$n \geq 0$の時

$\dfrac{1}{2 \pi} \displaystyle \int_{-\infty}^{\infty} e^{-itx} \dfrac{(x-i)^n}{(x+i)^{n+1}}dx = \begin{cases} \dfrac{1}{i}e^{-t}L_n(2t) & (t \geq 0) \\ 0 & (t <0) \end{cases}$

$L_n(t)$は、Laguerre多項式で、

$L_n(t) = \dfrac{e^t}{n!} \dfrac{d^n}{dt^n} (e^{-t} t^n)$

によって定義される

Laguerre関数$e^{-x/2}L_n(x)$が、$L^2(0,\infty)$の直交基底をなすことは、よく知られている

$V=\mathbb{C}[z,z^{-1}]$を、$V_{+}=\mathbb{C}[z]$と$V_{-} = z^{-1}\mathbb{C}[z^{-1}]$という二つのlimit of discrete seriesの表現空間に分解したが、この分解は

$L^2(\mathbb{R}) \simeq L^2(0,\infty) \oplus L^2(-\infty,0)$

に対応している。

$h_n(x) = \begin{cases} e^{-x/2}L_n(x)U(x) & (n \geq 0) \\ -e^{x/2}L_{-n-1}(-x)U(-x) & (n<0) \end{cases}$

$U(x) = \begin{cases} 1 & (x \geq 0) \\ 0 & (x<0) \end{cases}$

とすれば、$h_n(x)$は、$L^2(\mathbb{R})$の正規直交基底になる。

Fourier変換しただけなので、$h_n(x)$を基底として、limit of discrete seriesを実現することもできる

## Hilbert変換と解析信号
$h_n(\omega)$と$v_n(t)$は、互いにFourier変換の関係にある。

$L^2(\mathbb{R})$から$L^2(\mathbb{R})$へのHilbert変換は、

$v_n(t) \mapsto -i v_n(t) (n \geq 0)$

$v_n(t) \mapsto i v_n(t) (n<0)$

という変換として理解できる。$\mathcal{H}$をHilbert変換とすると

$u \mapsto \dfrac{1}{2}(u + i \mathcal{H}(u))$

は、$n \geq 0$に於いて、$v_n$を不変に保ち、$n<0$では、$v_n$を0に移すので、limit of (positive) discrete seriesへの射影となる

しばしば、実信号をFourier変換して、正周波数成分のみを逆Fourier変換で戻すことによって、解析信号を得るという操作が行われる(Hilbert変換を計算する方法としても使える)が、正周波数成分をFourier変換した空間の基底は、$h_n(\omega)$ $(n \geq 0)$ で与えられるので、同様に、limit of discrete seriesの表現空間へ射影している操作になっている。
