---
title: Lorentz変換の代数的導出
---
# Lorentz変換の代数的導出

1910年に、Ignatowskiが、光速度不変の原理を仮定しないで、Lorentz変換を導出する方法を考えた。そのvariation。



互いに等速運動する座標系$S,S'$を考え、座標系$S$に対して、$S'$が$x$方向に速度$v$で動いているとする。この時、座標$(t,x)$と座標$(t',x')$が線形変換$A(v)$で結ばれるとする。
$$\begin{pmatrix} t' \\ x' \end{pmatrix} = A(v) \begin{pmatrix} t \\ x \end{pmatrix}$$
自然な条件として、以下が成立すると仮定する

1. $A(0) = A(v) \circ A(-v) = A(-v) \circ A(v) = I$

2. $A(u) \circ (A(v) \circ A(w)) = (A(u) \circ A(v)) \circ A(w)$

自明なケースとして、全ての$v$に対して、$A(v)=I$があるが、除いておく

一般に、$A(u) \circ A(v) = A(f(u,v))$を満たす関数$f(u,v)$は(存在すれば)速度合成則と呼ぶ。

$f(u,v)$は存在し、$u=0,v=0$でTaylor展開できると仮定すると、$f(u,v)$は実数係数の形式的べき級数として、一次元formal group lawとなる。

実際、$f(u,v) = f_{10} u + f_{01} v + \cdots$とすると、条件(1)から、$f(v,0) = f(0,v) = v$なので$f_{10} = f_{01} = 1$となる。従って、
$$f(u,v) = u + v + \cdots$$
で、これは条件(1)から従う$f(v,-v) = f(-v,v) = 0$とも矛盾しない

また、条件(2)は、結合則なので、そのまま、formal group lawの結合則が得られる。そして、formal group lawの一般論から、一次元formal group lawは可換なので、
$$f(u,v) = f(v,u)$$
も得る。




$S$系に於ける速度は、$\dfrac{dx}{dt}$なので、速度合成則は
$$\dfrac{dx}{dt} = f \left(\dfrac{dx'}{dt'} , v\right)$$
を満たす。すると、座標変換を線形変換としているので、
$$f(u,v) = \dfrac{b_{21}(v) + b_{22}(v)u}{b_{11}(v) + b_{12}(v)u}$$
という形になることが分かる。$b_{ij}(v)$は$A(v)$の逆行列=$A(-v)$の行列要素。

まず、
$$f(0,v) = \dfrac{b_{21}(v)}{b_{11}(v)} = v$$
なので、$b_{21}(v) = v \cdot b_{11}(v)$が言える。また、
$$f(-v,v) =  \dfrac{v (b_{11}(v) - b_{22}(v))}{b_{11}(v) - b_{12}(v)v} = 0$$
となるので、$b_{11}(v) = b_{22}(v)$が従う。以上より
$$f(u,v) = \dfrac{(u + v)b_{11}(v)}{b_{11}(v) + b_{12}(v) u}$$
となる。$b_{12}(v)/b_{11}(v) = \alpha(v)$とすると
$$f(u,v) = \dfrac{u + v}{1 + \alpha(v) u}$$
となる。$f$の可換性$f(u,v)=f(v,u)$より、$\alpha(v) = \gamma v$の形でないといけない。$\gamma$は任意の定数


従って、
$$f(u,v) = \dfrac{u + v}{1 + \gamma u v}$$
となる。これは、formal group lawの条件を満たす。これは、Lorentz formal group lawという名前で呼ばれることがある

$\gamma = 0$の場合は、ガリレイ変換に対する速度合成則で、$\gamma = \dfrac{1}{c^2}$がLorentz変換の場合の速度合成則を与える。光速度不変の原理を仮定しなければ、$\gamma$を光速と結びつける理由は何もないし、負の実数であっても問題はない



速度合成則からだけでは、$b_{ij}(v)$には$v$の関数倍だけ不定性があるので、Lorentz変換の形は決まらない。Lorentz変換の形は、今の所、以下の形であることまで決まっている
$$A(v) = c(v)  \begin{pmatrix} 1 & -\gamma v \\ -v & 1 \end{pmatrix} $$
簡単には、鏡映変換$x \mapsto -x , v \mapsto -v$で変換が不変であることを仮定すれば、$c(v) = c(-v)$であることが言えるので、$A(v) \circ A(-v) = I$から、
$$c(v) = \pm \dfrac{1}{\sqrt{1 - \gamma v^2}}$$
と決定できる。また、$A(0)=I$より、
$$c(v) = \dfrac{1}{\sqrt{1 - \gamma v^2}}$$
と一意に決まる





