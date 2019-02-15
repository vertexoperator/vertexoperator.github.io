---
title: KdV階層のViraosoro対称性とKontsevich-Witten分配関数
---
#KdV階層のVirasoro対称性とKontsevich-Witten分配関数

KdV方程式は、ガリレイ対称性やスケール対称性を持っている。つまり、$u(x,t)$がKdV方程式

$u_t = \dfrac{1}{4}u_{xxx} + \dfrac{3}{2}u u_x$

の解であるとすると、

$w_1(x,t)=u(x+ct , t) + \dfrac{2}{3}c$

$w_2(x,t)=\lambda^2 u(\lambda x , \lambda^3 t)$

などは再びKdV方程式の解となる($\lambda$,$c$は定数)。タウ関数の方で見ると、無限小変換は

$L_{-1} = \dfrac{3}{2} t \dfrac{\partial}{\partial x} + \dfrac{x^2}{4}$

$L_{0} = \dfrac{1}{2} x \dfrac{\partial}{\partial x} + \dfrac{3}{2} t \dfrac{\partial}{\partial t} + \dfrac{1}{16}$

$u(x,t) = 2 \dfrac{\partial^2}{\partial x^2} \log \tau$

となる(これらの変換によって、タウ関数がタウ関数に移ることは計算問題)。容易に

$[L_0 , L_{-1}] = L_{-1}$

を計算できる。この対称性は、KdV階層に拡張することができ、そうするとnon-isospectral symmetryと呼ばれる無限個の対称性の一部であることが分かる。その無限小変換全体は、$n \geq -1$に対するVirasoro代数の部分代数と同型になる

Nonisospectral symmetries of the KdV equation and the corresponding symmetries of the Whitham equations

http://arxiv.org/abs/solv-int/9509004

一方で、KdV階層のVirasoro対称性は、Virasoro代数の表現を定めることになる。この表現空間で、ウェイト0の既約最高ウェイト表現を与える最高ウェイトベクトルを考えると、Kontsevich-Witten分配関数と一致することが証明されている。一般に、Topological conformal field theoryを一つ固定して、種数$g$のGromov-Wittenポテンシャル$F_g$(種数0の場合はprepotentialという名前が付いている)に対して、

$Z = exp(\sum_{g=0}^{\infty} \lambda^{2g-2} F_g)$

で定義される量を、数学では、(total) descendant potentialと呼んだりする。物理の人は、(string) partition functionと呼ぶことが多い。$\lambda$は、物理的には、結合定数と解釈されるっぽい。$\lambda$を動かして適当な極限を取ったりする場合もあるけど、そういうことを考えない場合には、$\lambda = 1$としている場合もある。このような分配関数に対して、Virasoro条件(Virasoro代数の作用があって$n \geq -1$の$L_n$によって消える)が成立するということが、観察されている

Heisenberg代数

$[H_n , H_m] = n \cdot \delta_{n+m,0} \quad (n \in \mathbf{Z})$

から、以下のVirasoro代数の自由場表示

$L_n = \dfrac{1}{4} \displaystyle \sum_{k \in 2\mathbf{Z}+1} : H_{2n-k} H_k : + \dfrac{1}{16} \delta_{n,0} \quad (n \in \mathbf{Z})$

を考える。これが、central charge 1のVirasoro代数を生成することは、通常のFeigin-Fuchs表現の時と同様の計算をすればいい。まずWickの定理から

$:H_k H_l : : H_m H_n : = \langle H_k H_m \rangle \langle H_l H_n \rangle + \langle H_k H_n \rangle \langle H_l H_m \rangle +
\langle H_k H_m \rangle : H_l H_n : + \langle H_k H_n \rangle : H_l H_m : + \langle H_l H_m \rangle : H_k H_n : + \langle H_l H_n \rangle : H_k H_m : + : H_k H_l H_m H_n :$

なので

$\dfrac{1}{16} \displaystyle \sum_{k,l : odd} : H_{n-k} H_k : :H_{m-l} H_l: = \\
 \dfrac{1}{16} \displaystyle \sum_{k,l : odd} \left(
              \langle H_{n-k} H_{m-l} \rangle \langle H_k H_l \rangle +
              \langle H_{n-k} H_{l} \rangle \langle H_k H_{m-l} \rangle +
              \langle H_{n-k} H_{m-l} \rangle : H_k H_l : +  
              \langle H_{n-k} H_{l} \rangle : H_k H_{m-l} : +
              \langle H_{k} H_{m-l} \rangle : H_{n-k} H_l : +
              \langle H_{k} H_l \rangle : H_{n-k} H_{m-l} : +
              : H_{n-k} H_k H_{m-l} H_l : \right)
= \\
\dfrac{1}{16} \left(
\displaystyle \sum_{k :odd , 0 \verb|| 0} 2k : H_{2n-k} H_{2m+k} : + \displaystyle \sum_{k,l :odd}: H_{2n-k} H_k H_{2m-l} H_{l} : \right)$

となって

$L_n L_m - L_m L_n = (n-m)L_{n+m} + \delta_{n+m,0} \left(\displaystyle \sum_{k:odd , 0 < k < |2n|} \dfrac{(2n-k)k}{8} - \dfrac{n-m}{16} \right) = (n-m)L_{n+m} + \dfrac{n(n^2-1)}{12} \delta_{n+m,0}$

Heisenberg代数は、無限変数$t_1,t_2,t_3,\cdots$の微分作用素として

$H_n = \lambda \dfrac{\partial}{\partial t_n} \quad (n>0)$

$H_{-n} = \lambda ^{-1} n t_n \quad (n>0)$

と書ける。$H_0$はFock表現に対しては、定数倍で作用するけど、上の自由場表示には現れない

これで、Virasoro代数は、$n > 0$について

$L_n = \displaystyle \sum_{k=0}^{\infty} (k+\dfrac{1}{2})t_{2k+1} \dfrac{\partial}{\partial t_{2n+2k+1}} + \dfrac{1}{4} \lambda^2 \displaystyle \sum_{k=0}^{n} \dfrac{\partial^2}{\partial t_{2k+1} \partial t_{2n-2k-1}}$

$L_0 = \displaystyle \sum_{k=0}^{\infty} (k+\dfrac{1}{2})t_{2k+1} \dfrac{\partial}{\partial t_{2k+1}} + \dfrac{1}{16}$

$L_{-n} = \displaystyle \sum_{k=0}^{\infty} (n+k+\dfrac{1}{2})t_{2n+2k+1} \dfrac{\partial}{\partial t_{2k+1}} + \dfrac{1}{4} \lambda^{-2} \displaystyle \sum_{k=1}^{n} (2k-1)(2n-2k+1) t_{2k-1} t_{2n-2k+1}$

という微分作用素で書ける。これがKdV階層のVirasoro対称性になっている

これらの微分作用素について

$L_n \cdot Z = 0 \quad (n \geq -1)$

を要請する($n>0$は最高ウェイトベクトル条件で、$n=0$はウェイト0という条件、$n=-1$は特異ベクトルが消えるための条件)とKontsevich-Witten分配関数を得るのだけど、そのままでは、原点で正則な解を持たない(つまり、Schur関数の線形結合で書ける解はない)ので、通常、適当に平行移動して、原点で正則になるようにする。実際には、$t_3 \mapsto t_3 + \dfrac{2}{3}$のようにする。この操作は、dilaton shiftと呼ばれているけども、表現論的意味はよく分からない。この操作をしておかないと、Gromov-Witten不変量の母関数と見ることもできない

(多成分/multi-colorの)free boson代数のoddな部分を取ってきて、Virasoro対称性を作るというのは、Dubrovinの構成によれば、位相的シグマ模型で一般的に通用する手法らしい

Normal forms of hierarchies of integrable PDEs, Frobenius manifolds and Gromov - Witten invariants

http://arxiv.org/abs/math/0108160

の3.10.2などを参照

&nbsp;

一方で、位相的極小模型のような場合には、N-KdV階層/Gelfand-Dikii階層のようなものを考える必要があって、やはりfree bosonから作るのだけど、oddな部分を取ってくるという形にはなっていない

Loop Equations and Virasoro Constraints in Non-perturbative 2-D Quantum Gravity

http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.49.3758

&nbsp;

また、cut-and-join operatorというものを使って、Kontsevich-Witten分配関数を表示する方法が発見されて、計算は簡単になった

Cut-and-Join operator representation for Kontsevich-Witten tau-function

http://arxiv.org/abs/1009.4887
