---
title: 2次元量子Kepler系の束縛状態
---
# 2次元量子Kepler系の束縛状態

二次元量子Kepler系を解くことを考える。シュレディンガー方程式は<br>
$\hat{H} \Psi = E \Psi$

$\hat{H} = -\dfrac{\hbar^2}{2 \mu} ( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} ) - \dfrac{k}{r}$

$r = \sqrt{x_1^2+x_2^2}$
となる。

束縛状態と散乱状態があるが、まずは、束縛状態。解き方は、いくつもあるが、比較的ポピュラーでない2つの方法を取り上げる

##解法1)Levi-Civita変換により、量子調和振動子の計算に帰着する

Levi-Civita変換の論文は1920年に出版されているので、最初は古典的なKepler系に対するものとして発見されたのだと思う。数十年後に、Kustaanheimo-Stiefel変換と呼ばれるようになる、3次元での類似物が発見された。

$x_1 = \dfrac{1}{2}(u_1^2 - u_2^2) , x_2=u_1u_2$という変数変換を行うと、$r=\dfrac{1}{2}(u_1^2+u_2^2)=u^2/2$で、シュレディンガー方程式は

$\left[ -\dfrac{\hbar^2}{2 \mu} \dfrac{1}{u^2} (\dfrac{\partial^2}{\partial u_1^2} + \dfrac{\partial^2}{\partial u_2^2}) - \dfrac{2 k}{u^2} \right] \Psi = E\Psi$

となる。両辺に$r = u^2/2$をかけて、移項すると、次の形の式を得る

$\left[ -\dfrac{\hbar^2}{4 \mu} (\dfrac{\partial^2}{\partial u_1^2} + \dfrac{\partial^2}{\partial u_2^2}) - \dfrac{E}{2} u^2 \right]\Psi = k \Psi$

これは、量子調和振動子の定常シュレディンガー方程式と同じ形をしている。$E \lt 0$の時

$M=2\mu , \omega = \sqrt{\dfrac{-E}{2 \mu}} , \epsilon = k$

と置くと

$\left( - \dfrac{\hbar^2}{2 M} (\dfrac{\partial^2}{\partial u_1^2} + \dfrac{\partial^2}{\partial u_2^2}) + \dfrac{1}{2} M \omega^2 u^2 \right) \Psi = \epsilon \Psi$

で、調和振動子の場合$\epsilon = (n_1 + n_2 + 1)\hbar \omega$ $(n_1,n_2=0,1,2,\cdots)$の時のみ解を持つ。

ところで、任意の$n_1,n_2$の組に対する調和振動子の固有状態が、そのまま量子Kepler系の固有状態となるわけではない。というのも、$(u_1,u_2) \to (-u_1,-u_2)$という変換によって、$x_1,x_2$は不変であるから、このような変換によって波動関数の値が変わってしまうようだと、量子Kepler系の波動関数と見なすことはできなくなる。つまり、調和振動子の波動関数はとして偶関数であることが、量子Kepler系の波動関数とみなせるために必要である(これは十分条件でもあるが、それを示すためはは実際に波動関数を計算してしまうのが早い。表現論的には振動子表現がシンプレティック代数の表現として既約でなく、2つの既約表現の直和に分解することに由来する)。偶関数であるためには、$n_1+n_2$が偶数であればよい。$n_1+n_2=2n$とすると

$E = -\dfrac{2 \mu k^2}{(2 n + 1)^2 \hbar^2}$ $(n=0,1,2,\cdots)$

となる。$n$が量子Kepler系の主量子数で、$2n=n_1+n_2$の非負整数解の個数分だけ縮退しているので、$2n+1$重に縮退している。基底状態は、規格化定数を除けば

$\Psi_0(x) = \exp( -\dfrac{2 \mu k}{\hbar^2} r)$

となる。


##解法2)spectrum generating algebraによる方法

多分、発見者はBarutら(1971年頃?)。3次元で考えられたが、任意次元で同様の計算ができる。

以下の10個の微分作用素を考えると、これらは閉じたLie環をなす(証明略)。

$L = x_1 \dfrac{\partial}{\partial x_2} - x_2 \dfrac{\partial}{\partial x_1}$

$A_1 = \dfrac{1}{2} x_1 \left( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} \right) - \dfrac{\partial}{\partial x_1} \cdot (x_1 \dfrac{\partial}{\partial x_1} + x_2 \dfrac{\partial}{\partial x_2}) + \dfrac{1}{2} x_1 + \dfrac{1}{2} \dfrac{\partial}{\partial x_1}$

$A_2 = \dfrac{1}{2} x_2 \left( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} \right) - \dfrac{\partial}{\partial x_2} \cdot (x_1 \dfrac{\partial}{\partial x_1} + x_2 \dfrac{\partial}{\partial x_2}) + \dfrac{1}{2} x_2 + \dfrac{1}{2} \dfrac{\partial}{\partial x_2}$

$B_1 = \dfrac{1}{2} x_1 \left( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} \right) - \dfrac{\partial}{\partial x_1} \cdot (x_1 \dfrac{\partial}{\partial x_1} + x_2 \dfrac{\partial}{\partial x_2}) - \dfrac{1}{2} x_1 + \dfrac{1}{2} \dfrac{\partial}{\partial x_1}$

$B_2 = \dfrac{1}{2} x_2 \left( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} \right) - \dfrac{\partial}{\partial x_2} \cdot (x_1 \dfrac{\partial}{\partial x_1} + x_2 \dfrac{\partial}{\partial x_2}) - \dfrac{1}{2} x_2 + \dfrac{1}{2} \dfrac{\partial}{\partial x_2}$

$T_1 = -\dfrac{r}{2}\left( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} \right) - \dfrac{r}{2}$

$T_2 = x_1 \dfrac{\partial}{\partial x_1} + x_2 \dfrac{\partial}{\partial x_2} + \dfrac{1}{2}$

$T_3 = -\dfrac{r}{2}\left( \dfrac{\partial^2}{\partial x_1^2} + \dfrac{\partial^2}{\partial x_2^2} \right) + \dfrac{r}{2}$

$\Gamma_1 = r \dfrac{\partial}{\partial x_1}$
$\Gamma_2 = r \dfrac{\partial}{\partial x_2}$


量子Kepler系のシュレディンガー方程式を

$r(\hat{H} - E)\Psi = 0$

と置くと
$r(\hat{H} - E) = \dfrac{\hbar^2}{2 \mu}(T_1 + T_3) - k - E (T_3 - T_1)$

なので

$\left[ \dfrac{\hbar^2}{2 \mu}(T_1 + T_3) + E (T_1 - T_3) - k \right] \Psi = 0$

と書くことができる。

$T_1,T_2,T_3$が$su(1,1)$代数をなす($[T_1,T_2]=T_3 , [T_2,T_3]=-T_1 , [T_3,T_1]=T_2$)ことから、有名な公式

$e^A B e^{-A} = e^{ad(A)} B$

を使って

$e^{\theta T_2} T_1 e^{-\theta T_2} = T_1 cosh(\theta) + T_3 sinh(\theta)$

$e^{\theta T_2} T_3 e^{-\theta T_2} = T_1 sinh(\theta) + T_3 cosh(\theta)$

となる。このことを利用して、量子Kepler系のシュレディンガー方程式を$T_1$や$T_3$の固有値問題に帰着させることができる。より初等的な見方としては、$e^{\theta T_2}$はスケーリング変換であり、適当なスケーリング変換によって、$E \lt 0$の時は$T_3$の固有値問題に、$E \gt 0$の時は$T_1$の固有値問題に帰着できるというだけのことである。調和振動子のシュレディンガー方程式を解く時には、スケーリング変換をほとんど空気のように行っているに過ぎない。また、ここでやっていることは、本質的には、解法1と同じである。$r(\hat{H} - E)\Psi = 0$をLevi-Civita変換すると、これは解法1で見た調和振動子の式と同一になる。

spectrum generating algebraの作用素もLevi-Civita変換すると、以下のような式を得る。

$L = \dfrac{1}{2} \left(u_2 \dfrac{\partial}{\partial u_1} - u_1 \dfrac{\partial}{\partial u_2} \right)$

$T_1 = -\dfrac{1}{4} \left(\dfrac{\partial^2}{\partial u_1^2} + \dfrac{\partial^2}{\partial u_2^2} \right) - \dfrac{1}{4}(u_1^2+u_2^2)$

$T_2 = \dfrac{1}{2}(u_1 \dfrac{\partial}{\partial u_1} + u_2 \dfrac{\partial}{\partial u_2} + 1)$

$T_3 = -\dfrac{1}{4} \left(\dfrac{\partial^2}{\partial u_1^2} + \dfrac{\partial^2}{\partial u_2^2} \right) + \dfrac{1}{4}(u_1^2+u_2^2)$

$\Gamma_1 = \dfrac{1}{2} \left( u_1 \dfrac{\partial}{\partial u_1} - u_2 \dfrac{\partial}{\partial u_2} \right)$

$\Gamma_2 = \dfrac{1}{2} \left( u_2 \dfrac{\partial}{\partial u_1} + u_1 \dfrac{\partial}{\partial u_2} \right)$

$A_1 = -\dfrac{1}{4} \left(\dfrac{\partial^2}{\partial u_1^2} - \dfrac{\partial^2}{\partial u_2^2} \right) + \dfrac{1}{4}(u_1^2-u_2^2)$

$A_2 = -\dfrac{1}{2} \dfrac{\partial^2}{\partial u_1 \partial u_2} + \dfrac{1}{2}u_1 u_2$

$B_1 = -\dfrac{1}{4} \left(\dfrac{\partial^2}{\partial u_1^2} - \dfrac{\partial^2}{\partial u_2^2} \right) - \dfrac{1}{4}(u_1^2-u_2^2)$

$B_2 = -\dfrac{1}{2} \dfrac{\partial^2}{\partial u_1 \partial u_2} - \dfrac{1}{2}u_1 u_2$


調和振動子の座標では、$T_3$の固有状態はHermite多項式$H_n(x)$を使って

$\phi_{nm}(u) = H_n(u_1) H_m(u_2) e^{-(u_1^2+u_2^2)/2}$

と書ける。

$T_3 \cdot \phi_{nm}(u) = \dfrac{n+m+2}{2} \phi_{nm}(u)$

で特に

$T_3 \cdot \phi_{00} = \dfrac{1}{2} \phi_{00}$

が、最小の固有値を持つ固有状態である。Kepler系の座標で書くならば、$e^{-r}$に相当する。


上記spectrum generating algebraの作用によって、n+mは2ずつ変動するので、$\phi_{00}$に作用させて得られるのは、偶関数のみ($n+m$が偶数の$\phi_{nm}$の線型結合で書ける)である。作用の仕方を具体的に書いておく(面倒なので、ブラ・ケット記法を用いる)

$T_3|n,m\rangle = (n+m+1)/2|n,m\rangle$

$L |n,m\rangle = (n/2)|n-1,m+1\rangle - (m/2)|n+1,m-1\rangle$

$A_1|n,m\rangle = (n-m)/2|n,m\rangle$

$A_2|n,m\rangle = (n/2)|n-1,m+1\rangle + (m/2)|n+1,m-1\rangle$

$(G_2+B_2)|n,m\rangle = -\frac{1}{2}|n+1,m+1\rangle$

$(G_1+B_1)|n,m\rangle = -\frac{1}{4}|n+2,m\rangle + \frac{1}{4}|n,m+2\rangle$

$(T_1+T_2)|n,m\rangle = -\frac{1}{4}|n+2,m\rangle - \frac{1}{4}|n,m+2\rangle$

$(G_2-B_2)|n,m\rangle = 2nm|n-1,m-1\rangle$

$(G_1-B_1)|n,m\rangle = n(n-1)|n-2,m\rangle  - m(m-1)|n,m-2\rangle$

$(T_1-T_2)|n,m\rangle = -n(n-1)|n-2,m\rangle - m(m-1)|n,m-2\rangle$

この式を眺めれば、$|0,0\rangle$から始めて、$n+m$が偶数の$|n,m\rangle$が全て得られることが分かる。


上記spectrum generating algebraの基底のうち、$T_3$と可換なのは$A_1,A_2,L$であり、これら3つの元は複素Lie環$so(3,\mathbf{C})$と同型なLie環の基底となり、

$C = A_1^2 + A_2^2 - L^2$

がCasimir作用素となっている。また、

$C = T_3^2 - \dfrac{1}{4}$

という関係式が成立している。Cartan対合の固定点となる実Lie環を決める。$\phi_{nm}$が直交するようなHermite内積を入れると、明らかに

$(\phi_{n',m'} , A_1 \phi_{n,m}) + (A_1 \phi_{n',m'} , \phi_{n,m}) \neq 0$

である。$\sqrt{-1}A_1 , \sqrt{-1}A_2,L$は閉じた実Lie環をなし、$so(3)$と同型で、かつ、ユニタリー表現として作用しているので、これが求めるLie環である

$so(3)$の既約ユニタリー表現はよく知られている通り、全て有限次元である。$n+m$が偶数であるような$\phi_{nm}$で張られるベクトル空間を考えると、これはspectrum generating algebraの既約表現空間となっているが、これをこの$so(3)$に制限して既約分解すると、各既約表現空間上では$T_1$は定数倍で作用する。この分解の仕方は、$so(3)$の$1,3,5,\cdots,(2n+1),\cdots$次元既約表現が一回ずつ出てくるという形になる。これが$T_1$が離散スペクトルを持つことの表現論的な理解となる。


同様に$T_1$と可換なのは$B_1,B_2,L$であり、これら3つの元も複素Lie環$so(3,\mathbf{C})$と同型なLie環の基底となり、

$B_1^2+B_2^2+L^2 = T_1^2 + \dfrac{1}{4}$

という関係がある。こちらは散乱状態と関係してくる。

ついでに、$T_2$についても

$\left[T_2,\Gamma_1 \right] = \left[T_2 , \Gamma_2 \right] = \left[T_2 , L \right]= 0$

かつ

$\Gamma_1^2 + \Gamma_2^2 - L^2 = T_2^2 - \dfrac{1}{4}$

という関係が成立している。形式的には

$T_2 (u_1^2 + u_2^2)^{s/2} = \dfrac{s+1}{2} (u_1^2 + u_2^2)^{s/2}$

$L (u_1^2 + u_2^2)^{s/2} = 0$

なので、$(u_1^2 + u_2^2)^{s/2}$に$\Gamma_1,\Gamma_2$を作用させていくと、$\Gamma_1,\Gamma_2,L$のなすLie環の既約表現がひとつ得られる。任意の$s \in \mathbf{C}$について、ユニタリーとなるわけではない<br>
