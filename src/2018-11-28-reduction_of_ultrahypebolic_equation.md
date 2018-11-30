---
title: 超双曲方程式から超幾何型関数への簡約
---

# 超双曲方程式から超幾何型関数への簡約

## 参考文献

Twistor Theory of the Airy Equation

https://arxiv.org/abs/1401.0025


## Airy関数の場合
論文の座標との対応は
$(x_1,x_2,x_3,x_4) = (\tilde{z},\tilde{w},w,z)$

$\phi(x_1,x_2,x_3,x_4) = \exp \left( x_3-x_2(x_4-x_1)-\dfrac{2}{3}x_2^3 \right)F(z)$

$z = x_1 - x_4 - x_2^2$

$\begin{cases} X=\partial_3 \\ Y=\partial_1+\partial_4 \\ Z=(x_4-x_1)\partial_3 + x_2(\partial_1-\partial_4) + \partial_2 \end{cases}$

$(\partial_2 \partial_3 - \partial_1\partial_4)\phi = \exp \left( x_3-x_2(x_4-x_1)-\dfrac{2}{3}x_2^3 \right)(F''(z)+zF(z))$

なので、$\phi$が超双曲方程式を満たすことと、$F$がAiry微分方程式を満たすことは同値。
加えて、$\phi$を上の形に取るために、付加的な条件が付く。

$X(\phi)=\phi$,$Y(\phi)=0,Z(\phi)=0$

[__計算__]
$\phi_1 = \exp \left( x_3-x_2(x_4-x_1)-\dfrac{2}{3}x_2^3 \right)F'(z)$ ,
$\phi_2 = \exp \left( x_3-x_2(x_4-x_1)-\dfrac{2}{3}x_2^3 \right)F''(z)$

とすると

$(\partial_2\partial_3)\phi = \partial_2\phi=-(x_4-x_1)\phi-2x_2^2\phi-2x_2\phi_1$

$(\partial_1\partial_4)\phi =\partial_1(-x_2\phi - \phi_1) =-(x_2^2\phi+x_2\phi_1)-(x_2\phi_1+\phi_2)=-x_2^2\phi-2x_2\phi_1-\phi_2$

などから、分かる

[__簡約の直接計算による導出__]
$Z(\psi)=0 \Rightarrow \psi(x_1, x_2, x_3, x_4) = P(x_2^2 - 2 x_1, x_1 + x_4, x_1 x_2 - 2 x_2^3/3 - x_2 x_4 + x_3)$

$P=P(t_1,t_2,t_3)$
について
$X(\psi)=\psi,Y(\psi)=0$
から

$\dfrac{\partial P}{\partial t_1}=\dfrac{\partial P}{\partial t_2}$

$\dfrac{\partial P}{\partial t_3} = P$

となって、$P(t_1,t_2,t_3)= e^{t_3}F(t_1+t_2)$

$t_1,t_2=x_2^2-2x_1,x_1+x_4$
に対して、$t_1+t_2=z$
に注意して、$\psi$が超双曲方程式を満たすという条件から、Airyの微分方程式が出る

## Gauss超幾何関数の場合
$\phi(x_1,x_2,x_3,x_4) = x_1^{c-1}x_2^{-a} x_3^{-b} F\left(\dfrac{x_1x_4}{x_2x_3}\right)$

$z = \dfrac{x_1x_4}{x_2x_3}$
として

$(\partial_2 \partial_3 - \partial_1\partial_4)\phi = x_1^{c-1}x_2^{-a-1}x_3^{-b-1}\left( (z-z^2)F''(z)-(a+b+1)zF'(z)+cF'(z)-abF(z) \right)$

$\phi$が超双曲方程式の解であることと、$F$がGauss超幾何微分方程式の解であることは同値

$\begin{cases} X= -x_3\partial_3-x_4\partial_4 \\ Y=-x_1\partial_1-x_2\partial_2 \\ Z=x_2\partial_2+x_4\partial_4 \end{cases}$



## Kummer合流型超幾何関数の場合
$\phi(x_1,x_2,x_3,x_4) = e^{x_1/x_2}x_2^{\alpha-1}x_4^{\gamma-\alpha-1} z^{\gamma-1}F(z)$

$z = \dfrac{x_3}{x_4} - \dfrac{x_1}{x_2}$

に対して、$F(z)$がKummerの超幾何微分方程式

$z F''(z) + (\gamma-z)F'(z) - \alpha F(z) = 0$

を満たすことと、$\phi$が超双曲方程式を満たすことは同値。

$\begin{cases} X=x_2 \partial_1+x_4\partial_3 \\ Y=x_1 \partial_1+x_2\partial_2+x_3\partial_3+x_4\partial_4 \\ Z=-x_1\partial_1-x_2\partial_2 \end{cases}$

簡単な計算で、

$X(\psi) = a \psi \Rightarrow \psi(x_1,x_2,x_3,x_4)=e^{a x_1/x_2}f(x_2,x_4,\dfrac{x_2x_3-x_1x_4}{x_2})$

$Z(\psi)=c\psi \Rightarrow f(t_1,t_2,t_3) = t_2^{-c}g(t_1,t_3)$

$(Y+Z)(\psi)=(b+c)\psi \Rightarrow g(u_1,u_2) = u_1^{b+c} h(u_2/u_1)$

が分かる。従って、

$\psi(x_1,x_2,x_3,x_4) = e^{-ax_1/x_2} x_2^{b+c} x_4^{-c} h(z)$

$(a,b,c)=(-1,\gamma-2,1-\gamma)$
として、
$F(z) = z^{1-\gamma} h(z)$
とすればいい

## Bessel関数の場合
簡約する群の無限小生成子は

$\begin{cases} X = -x_1 \partial_{3} - x_2 \partial_{4} \\ Y=x_2 \partial_1 + x_4 \partial_3 \\ Z=-x_1\partial_1-x_2\partial_2-x_3\partial_3-x_4\partial_4 \end{cases}$


$Z(\psi) = c\psi \Rightarrow \psi(x_1,x_2,x_3,x_4) = x_2^{-c} f(\dfrac{x_1}{x_2},\dfrac{x_3}{x_2},\dfrac{x_4}{x_2})$

$f=f(t_1,t_2,t_3)$
に対しては

$X(\psi) = a \psi \Rightarrow t_1 \dfrac{\partial f}{\partial t_2} + \dfrac{\partial f}{\partial t_3} = -a f \Rightarrow f(t_1,t_2,t_3)=e^{-at_2/t_1}g(t_1,t_3-\dfrac{t_2}{t_1})$

従って、
$\psi(x_1,x_2,x_3,x_4) = x_2^{-c} e^{-ax_3/x_1} g(\dfrac{x_1}{x_2},\dfrac{x_4}{x_2}-\dfrac{x_3}{x_1})$

$g=g(u_1,u_2)$
に対して

$Y(\psi)=b\psi \Rightarrow -a u_2 g + u_1\dfrac{\partial g}{\partial u_1}-u_2\dfrac{\partial g}{\partial u_2} = bg \Rightarrow g(u_1,u_2)=\exp(bu_1-au_2) h(u_1u_2)$

$z=u_1u_2=\dfrac{x_1x_4-x_2x_3}{x_2^2}$
として、結果をまとめると

$\psi(x_1,x_2,x_3,x_4) = x_2^{-c}e^{-ax_3/x_1}\exp(-ax_4/x_2 + ax_3/x_1 + bx_1/x_2)h(z)=x_2^{-c}e^{(-ax_4+bx_1)/x_2}h(z)$

で、$h(z)$の満たす微分方程式は

$z h''(z) + c h'(z) + ab h(z)==0$

となる。
$(a,b,c)=(1,1,1+\alpha)$
の時、$x^2 = 4 z$と変数変換すると、微分方程式は以下の形に変換される。

$y'' + \dfrac{1+2 \alpha}{x} y' + y=0$

この微分方程式の解$y=y(x)$に対して、$x^{\alpha} y$は、Bessel微分方程式の解となる。



## Hermite-Weber関数の場合
簡約する群の無限小生成子は

$\begin{cases} X=\partial_1 \\ Y=x_4\partial_3+x_2\partial_1+\partial_2 \\ Z=x_3\partial_3+x_4\partial_4 \end{cases}$

明らかに
$z = \dfrac{x_3}{x_4} - x_2$
とすればいい。

$Y({\psi}) = b \psi \Rightarrow \psi(x_1,x_2,x_3,x_4) = e^{\pm b x_2} f(x_4,x_2^2-2x_1,x_3-x_2x_4)$

$X(\psi)=a \psi \Rightarrow -2 \dfrac{\partial f}{\partial t_2} = a f- \Rightarrow \psi = e^{\pm bx_2}g(x_4,x_3-x_2x_4)\exp\left(-\dfrac{a}{2}(x_2^2-2x_1)\right)$

$Z(\psi)=c\psi \Rightarrow g(t_1,t_2) = t_1^c h(\dfrac{t_2}{t_1}) \Rightarrow \psi=e^{\pm b x_2} x_4^c\exp\left(-\dfrac{a}{2}(x_2^2-2x_1)\right) h(z)$

$\psi$が超双曲方程式を満たすとして、$h$が満たすべき微分方程式は

$h''(z) -(a z + b)h'(z) - a c h(z) = 0$

となる。

$(a,b,c)=(1,0,-\gamma)$
とすると

$h''(z) - z h'(z) + \gamma h(z) = 0$

で、Hermite-Weber関数の満たす微分方程式を得る。


## メモ:線形微分方程式と積分変換

#### Laplace equation in $\mathbb{R}^3$ (Whittaker,1903)

$\phi(x,y,z) = \displaystyle \int_{0}^{2\pi} f(z+ix \cos \alpha+iy\sin \alpha,\alpha)d\alpha$

$\Rightarrow \dfrac{\partial^2\phi}{\partial x^2} + \dfrac{\partial^2\phi}{\partial y^2} + \dfrac{\partial^2\phi}{\partial z^2} = 0$

#### Laplace equation in $\mathbb{R}^4$ (Bateman,1904)

$\phi(x,y,z,\tau) = \displaystyle \oint_{\Gamma \subset \mathbb{CP}^1} f((z+ i \tau) +　(x+iy)\lambda,(x-iy)-(z-i\tau)\lambda,\lambda)d\lambda$

$\Rightarrow \dfrac{\partial^2\phi}{\partial \tau^2} + \dfrac{\partial^2\phi}{\partial x^2} + \dfrac{\partial^2\phi}{\partial y^2} + \dfrac{\partial^2 \phi}{\partial z^2} = 0$

#### ultrahyperbolic equation in $\mathbb{R}^4$ (Fritz John,1938)

for $f:\mathbb{R}^3 \to \mathbb{R}$, oriented line $L \subset \mathbb{R}^3$
$, \phi(L) = \int_L f ds$

$\phi(\alpha_1,\alpha_2,\beta_1,\beta_2) = \displaystyle \int_{-\infty}^{\infty}f(\alpha_1 s+ \beta_1 , \alpha_2 s+\beta_2,s)ds$

$\Rightarrow \dfrac{\partial^2 \phi}{\partial \alpha_1 \beta_2} - \dfrac{\partial^2 \phi}{\partial \alpha_2 \beta_1} = 0$

$\Leftrightarrow \dfrac{\partial^2\phi}{\partial x^2} + \dfrac{\partial^2\phi}{\partial z^2} - \dfrac{\partial^2\phi}{\partial y^2} - \dfrac{\partial^2 \phi}{\partial t^2} = 0$

$(\alpha_1=x+y,\alpha_2=t+z,\beta_1=t-z,\beta_2=x-y)$

#### massless Klein-Gordon equation (Penrose,1967)
$\phi(x,y,z,t) = \displaystyle \oint_{\Gamma \subset \mathbb{CP}^1} f((z+t) +(x+iy)\lambda,(x-iy)-(z-t)\lambda,\lambda)d\lambda$

$\Rightarrow \dfrac{\partial^2\phi}{\partial t^2} - \dfrac{\partial^2\phi}{\partial x^2} - \dfrac{\partial^2\phi}{\partial y^2} - \dfrac{\partial^2 \phi}{\partial z^2} = 0$
