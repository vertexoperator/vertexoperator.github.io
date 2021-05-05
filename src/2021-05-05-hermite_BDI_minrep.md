---
title: so(n+1,2)の極小表現の実現
---
# $so(n+1,2)$の極小表現の実現

共形代数$so(n+1,2)$の極小表現は、massless scalar field equationのpositive energy solutionの空間として実現できる

実空間の座標を
$\mathbf{x} = (x_0,x_1,\cdots,x_n)=(x_0,\mathbf{r})=(t,r\Omega_r)$
と取り、運動量空間の座標を
$\mathbf{k} = (k_0,k_1,\cdots,k_n)=(k,k\Omega_k)$
とする。

ここで、
$\Omega_r ,\Omega_k \in S^{n-1}$
は単位ベクトル。
$r = \sqrt{x_1^2+\cdots + x_n^2}$、$k = \sqrt{k_1^2+\cdots + k_n^2}$

エネルギーと運動量の関係式
$k_0^2 - k_1^2 - \cdots - k_n^2=0$
及び、正エネルギー条件$k_0 >0$より、
$k=k_0 > 0$
が成り立つ。


## 最低ウェイトベクトルの計算
論文[The minimal representation of the conformal group and classic solutions to the wave equation](https://arxiv.org/abs/0901.2280)によって、実空間での最低ウェイトベクトルは、

$\Psi(\mathbf{x}) = \dfrac{1}{((1-it)^2+r^2)^{(n-1)/2}}$

で与えられる。

運動量空間での最低ウェイトベクトルは、実空間の最低ウェイトベクトルをFourier変換すると計算できる。平面波を、hyperspherical harmonicsで展開すると、計算はHankel変換に帰着する。

$f(\mathbf{k}) = \dfrac{k_0}{\pi} \displaystyle \int \Psi(\mathbf{x})e^{-i \mathbf{k} \cdot \mathbf{x}} d\mathbf{r} = \dfrac{k_0}{\pi} \displaystyle \int d\Omega_r \displaystyle \int r^{n-1}dr \Psi(\mathbf{x}) e^{-ikt}e^{ikr\Omega_k\cdot\Omega_r}$

で、平面波を[Angular integrations in m‐dimensional spaces and hyperspherical harmonics](https://doi.org/10.1002/qua.560220406)に従って、以下のように展開する

$e^{ikr\Omega_k\cdot\Omega_r} = 4\pi \displaystyle \sum_{l=0}^{\infty} i^{l} \dfrac{J_{l+\frac{n}{2}-1}(kr)}{(kr)^{\frac{n}{2}-1}}\sum_{\mu}Y_{l\mu}(\Omega_k)Y_{l\mu}^{*}(\Omega_r)$

ここで、$J_{\nu}$は、Bessel関数。そのまま代入すると、以下のようになる。

$f(\mathbf{k})=\dfrac{4k}{k^{\frac{n}{2}-1}}\displaystyle \int d\Omega_r \displaystyle \int r^{\frac{n}{2}}dr\Psi(\mathbf{x})e^{-ikt}\sum_{l=0}^{\infty} i^{l} J_{l+\frac{n}{2}-1}(kr)\sum_{\mu}Y_{l\mu}(\Omega_k)Y_{l\mu}^{*}(\Omega_r)$

$\Psi(\mathbf{x})$は、$\Omega_r$に依存する項がないので、$l=0$のみの項が残り、

$f(\mathbf{k})=\dfrac{4ke^{-ikt}}{k^{\frac{n}{2}-1}}\displaystyle \int d\Omega_r \displaystyle \int \dfrac{r^{\frac{n}{2}}}{((1-it)^2+r^2)^{(n-1)/2}} J_{\frac{n}{2}-1}(kr)dr$

$\nu=\dfrac{n}{2}-1$
として、Hankel変換と球の表面積の計算により、

$f(\mathbf{k}) = \dfrac{4ke^{-ikt}}{k^{\nu}}\displaystyle \int d\Omega_r \dfrac{\sqrt{\pi}}{2^{\nu}\Gamma(\nu+\frac{1}{2})}k^{\nu-1} e^{-(1-it)k}=\dfrac{4\sqrt{\pi}}{2^{\nu}\Gamma(\nu+\frac{1}{2})}\dfrac{\pi^{\nu+1}}{\Gamma(\nu+1)} e^{-k}$

ガンマ関数の公式
$\Gamma(z)\Gamma(z+\frac{1}{2}) = 2^{1-2z}\sqrt{\pi}\Gamma(2z)$
を使って整理すると

$f(\mathbf{k}) =\dfrac{2^{\nu}\pi^{\nu+1}}{\Gamma(d-1)}e^{-k}$

を得る。定数項を除けば

$f(\mathbf{k}) \propto e^{-k}$



## 運動量空間での$so(n+1,2)$の作用
標準的な共形代数の生成元として、添字$a,b=1,\cdots,n$を使って

$P_0 = i k$

$P_{a} = -i k_a$

$M_{0a} = k \partial_{a}$

$M_{ab} = k_a \partial_{b} - k_b \partial_{a}$

$D = \dfrac{n-1}{2} + k_1 \partial_{1} + \cdots + k_n \partial_{n}$

$K_0 = ik(\partial_{1}^2 + \cdots + \partial_{n}^2)$

$K_{a} = i((n-1)\partial_{a} - k_a(\partial_1^2+\cdots \partial_n^2) +2\displaystyle \sum_{j=1}^{n}k_{j}\partial_{j}\partial_{a})$

を取ることができる。


$\mu,\nu=0,\cdots,n$に対して、

$Y_{\mu\nu} = M_{\mu\nu}$

$Y_{\mu,n+1} = -\dfrac{1}{2}(P_{\mu}+K_{\mu})$

$Y_{\mu,n+2} = \dfrac{1}{2}(P_{\mu}-K_{\mu})$

$Y_{n+1,n+2} = D$

と定義する。


添字$p,q,r,s=0,\cdots , n+2$に対して、
$\eta_{pq} = \mathrm{diag}(-1,+1 ,\cdots .+1,+1,-1)$

$Y_{pp} = 0$

かつ、$p>q$に対して、

$Y_{pq} = -Y_{qp}$

と定める。この時、

$[Y_{pq},Y_{rs}] = \left(\eta_{qr}Y_{ps} -\eta_{pr}Y_{qs} - \eta_{qs} Y_{pr} + \eta_{ps} Y_{qr}\right)$

が成立する。

$[D,P_{\mu}]=P_{\mu}$

$[D,K_{\mu}]=-K_{\mu}$

$[K_{\mu},P_{\nu}] = 2(\eta_{\mu\nu} D - M_{\mu\nu})$

$[K_{\lambda} , M_{\mu\nu}] = (\eta_{\lambda\mu}K_{\nu}-\eta_{\lambda\nu}K_{\mu})$

$[P_{\lambda} , M_{\mu\nu}] = (\eta_{\lambda\mu}P_{\nu}-\eta_{\lambda\nu}P_{\mu})$

$[M_{\mu\nu},M_{\lambda\rho}] = (\eta_{\nu\lambda}M_{\mu\rho}+\eta_{\mu\rho}M_{\nu\lambda}-\eta_{\mu\lambda}M_{\nu\rho}-\eta_{\nu\rho}M_{\mu\lambda})$

$[K_{\mu},K_{\nu}] = [P_{\mu},P_{\nu}] = [D,M_{\mu\nu}] = 0$


## Cartan部分環、ルート分解、最低ウェイト条件
以下、$m=[(n+3)/2]=\mathrm{rank}(so(n+1,2))$

$\mathfrak{g}_{\mathbf{C}} = so(n+1,2)_{\mathbf{C}} \simeq so(n+3,\mathbf{C})$

$j=0, \cdots , m-1$に対して、$\mathfrak{g}_{\mathbf{C}}$のCartan部分環$\mathfrak{h}$の基底を

$h_j = i Y_{j,n+2-j}$

に取る。


$Y_{0,n+2} \cdot f = i\dfrac{n-1}{2} f$

$Y_{1,n+1} \cdot f = 0$

$Y_{j,n+2-j} \cdot f= 0 \space ( j =2, \cdots , m-1)$

$\mathfrak{g}_{\mathbf{C}}$を、Cartan部分環の作用でルート分解する。

$\epsilon,\epsilon'=\pm 1$、$0 \le j \lt k \le m-1$に対して

$X_{jk}^{(\epsilon,\epsilon')} =Y_{jk} + \epsilon Y_{n+2-j,n+2-k} + i\epsilon \epsilon' Y_{j,n+2-k} - i \epsilon' Y_{n+2-j,k}$

を定義すると、
$\eta_{jj}=\eta_{n+2-j,n+2-j}$,$\epsilon^2=\epsilon'^2=1$
に注意して

$[Y_{j,n+2-j},X_{jk}^{(\epsilon\epsilon')}] = -i \epsilon' \eta_{jj} X_{jk}^{(\epsilon\epsilon')}$

$[Y_{k,n+2-k},X_{jk}^{(\epsilon\epsilon')}] = i \epsilon \epsilon' \eta_{kk} X_{jk}^{(\epsilon \epsilon')}$

また、$n$が偶数の時は

$W_{j}^{(\epsilon)} = Y_{j,m} - i \epsilon Y_{n+2-j,m}$

として

$[Y_{j,n+2-j} , W_{j}^{(\epsilon)}] = -i \epsilon \eta_{jj} W_{j}^{(\epsilon)}$

添字$a=1,\cdots,n$に対して、簡単な計算で

$M_{0a} \cdot f = -k_a \cdot f$

$Y_{a,n+1} \cdot f = 0$

$Y_{a,n+2} \cdot f = -ik_a \cdot f$

かつ

$Y_{0,n+1} \cdot f = -i(k - \dfrac{n-1}{2})f$

$Y_{0,n+2} \cdot f = \dfrac{i}{2}(n-1) f$

$Y_{n+1,n+2} \cdot f = -(k - \dfrac{n-1}{2})f$

で、回転対称性から、$a,b=1,\cdots,n$に対しては

$Y_{ab} \cdot f = M_{ab} \cdot f = 0$

なので、

$W_{0}^{(-1)} \cdot f =0$

$W_{k}^{(\pm 1)} \cdot f = 0$

$(X_{0k}^{(+1,+1)} +X_{0k}^{(-1,+1)})\cdot f = 2(Y_{0k} + i Y_{k,n+2})f = 0$

$(X_{0k}^{(+1,+1)} - X_{0k}^{(-1,+1)})\cdot f=-2i(Y_{0,n+2-k}+iY_{n+2-k,n+2})f = 0$

$X_{0k}^{(\epsilon,+1)} \cdot f = 0$

$X_{1k}^{(\epsilon,\epsilon')} \cdot f = 0$

$X_{jk}^{(\epsilon,\epsilon')} \cdot f = 0$
