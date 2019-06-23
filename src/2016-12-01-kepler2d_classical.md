---
title: 古典Kepler系の解析解
---
# 古典Kepler系の解析解

平面座標$(x_1(t),x_2(t))$に対して、複素座標$x(t) = x_1(t) + i x_2(t)$を取る。$r=|x|$として、問題は
$\ddot{x} + k \dfrac{x}{r^3} = 0$,　$\dfrac{1}{2}|\dot{x}|^2 - \dfrac{k}{r} = E < 0$

新しい時間変数$\tau$を$dt = r d\tau$で導入する。以下、$\dot{f} = \dfrac{df}{dt}$,$f' = \dfrac{df}{d\tau}$のこととする。

$\dfrac{d}{dt} = \dfrac{1}{r} \dfrac{d}{d\tau}$ $\space,$ $\dfrac{d^2}{dt^2} = \dfrac{1}{r^2} \dfrac{d^2}{d\tau^2} - \dfrac{r'}{r^3}\dfrac{d}{d\tau}$


新しい空間座標$u = u(t)$によって$x=u^2$とする。
$r = |x| = |u|^2$,$x' = 2u u'$,$x'' = 2(u u'' + u'^2)$

$\ddot{x} + k \dfrac{x}{r^3} = 0 \Rightarrow 2r u'' + (k - 2|u'|^2)u=0$

$\dfrac{1}{2}|\dot{x}|^2 - \dfrac{k}{r} = E  \Rightarrow 2|u'|^2 = k + rE$

$\therefore)u'' - \dfrac{E}{2} u = 0 \Leftrightarrow u'' + \omega^2 u = 0 \space (\omega = \sqrt{\dfrac{-E}{2}})$

$u(\tau) = A \cos(\sqrt{\dfrac{-E}{2}} \tau) + B \sin(\sqrt{\dfrac{-E}{2}} \tau)$ 　　($A,B$は初期条件から決める。$A,B \in \mathbf{C}$に注意)

$t - t_0= \displaystyle \int dt = \displaystyle\int r d\tau = \displaystyle \int \left(|A|^2 \cos^2(\omega \tau) + |B|^2 \sin^2(\omega \tau) +(A\bar{B}+\bar{A}B) \sin(\omega \tau)\cos(\omega \tau) \right) d \tau$

$= \dfrac{1}{2}(|A|^2+|B|^2)\tau + (|B|^2-|A|^2)\dfrac{\sin(2\omega\tau)}{4 \omega} - (A\bar{B}+\bar{A}B) \dfrac{\cos(2\omega \tau)}{4\omega}$　　　


$t-t_0=F(\tau)$の形($F$は$dt/d\tau = r >0$なので逆関数は一価)で$\tau = F^{-1}(t)$を、上の式に放り込んで、$x=u^2$が"解析解"となる。

$F$の逆関数は、簡単には求まらないので
$A = A_r + \sqrt{-1} A_i , B=B_r + \sqrt{-1} B_i \space (A_r,A_i,B_r,B_i \in \mathbf{R})$と置くと、以下が解となる

$\begin{cases} x_1 = \dfrac{1}{2}(A_r^2-A_i^2-B_r^2+B_i^2) \cos(2\omega \tau) + (A_rB_r - A_iB_i)\sin(2\omega\tau) + \dfrac{1}{2}(A_r^2-A_i^2+B_r^2-B_i^2) \\ x_2 = (A_r A_i - B_r B_i) \cos(2\omega\tau) + (A_r B_i + A_i B_r) \sin(2\omega\tau) + (A_r A_i + B_r B_i) \\ t =\dfrac{1}{2}(A_r^2+A_i^2+B_r^2+B_i^2)\tau +(B_r^2+B_i^2-A_r^2-A_i^2)\dfrac{\sin(2\omega\tau)}{4\omega}-(A_rB_r+A_iB_i)\dfrac{\cos(2\omega\tau)}{2\omega}+t_0 \end{cases}$
