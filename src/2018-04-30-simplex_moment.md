---
title: 単体の幾何学的モーメントの計算
---
# 単体の幾何学的モーメントの計算

二次元平面上の3点$P=(x_0,y_0) , Q=(x_1,y_1) , R=(x_2 , y_2)$を頂点とする三角形を$S$とする
$$S = \{ ((1-u-v)x_0 + u x_1 + vx_2,(1-u-v)y_0 + u y_1 + v y_2) \in \mathbf{R}^2 | 0 \leq u,v,u+v \leq 1 \}$$
$$S_0 = \{(u,v) \in \mathbf{R}^2 |  0 \leq u,v,u+v \leq 1 \}$$



この時、以下の量を計算する
$$M_{ij} = \displaystyle \int_S x^i y^j dx dy$$
$i=j=0$の時は、面積で
$$M_{00} = \displaystyle \int_{S_0} \left(\displaystyle \frac{\partial x}{\partial u}\displaystyle \frac{\partial y}{\partial v} - \displaystyle \frac{\partial x}{\partial v}\displaystyle \frac{\partial y}{\partial u} \right)dudv = \displaystyle \int_{S_0} \left( (x_1-x_0)(y_2-y_0) - (x_2-x_0)(y_1-y_0) \right)dudv $$
$$ = \displaystyle \frac{1}{2} \left( (x_1-x_0)(y_2-y_0) - (x_2-x_0)(y_1-y_0)  \right)$$



以下、ヤコビアン$J= (x_1-x_0)(y_2-y_0) - (x_2-x_0)(y_1-y_0)$を定めておくと同様に
$$M_{10} = \displaystyle \int_{S_0} \left( (1-u-v)x_0 + u x_1 + vx_2 \right) \left( \displaystyle \frac{\partial x}{\partial u}\displaystyle \frac{\partial y}{\partial v} - \displaystyle \frac{\partial x}{\partial v}\displaystyle \frac{\partial y}{\partial u} \right)dudv$$
$$= J \displaystyle \int_{0}^{1} du \int_{0}^{1-u} dv \left( (1-u-v)x_0 + u x_1 + vx_2\right) = 
J \displaystyle \int_{0}^{1} du \left( (1-u) x_0 + u(1-u)(x_1-x_0)+ \displaystyle \frac{1}{2}(1-u)^2 (x_2-x_0) \right)$$
$$= \displaystyle \frac{J}{6} (x_0 + x_1 + x_2)$$
を得る



Stokesの定理によって、境界線上の積分に置き換えることもできる。再び、$i=j=0$の時を考えると
$$M_{00} = \displaystyle \int_S dx dy = \displaystyle \int_{\overline{PQ}} x dy + \displaystyle \int_{\overline{QR}} x dy + \displaystyle \int_{\overline{RP}} x dy$$
で、例えば$x(t)=x_0+t(x_1-x_0) , y(t)=y_0+t(y_1-y_0)$として
$$\displaystyle \int_{\overline{PQ}} x dy = \displaystyle \int_{0}^{1} x(t) \displaystyle \frac{dy}{dt}dt = x_0(y_1-y_0) + \displaystyle \frac{1}{2} (x_1 - x_0)(y_1 - y_0)$$
を得る。同様に
$$\displaystyle \int_{\overline{QR}} x dy = x_1(y_2-y_1) + \displaystyle \frac{1}{2} (x_2 - x_1)(y_2 - y_1)$$
$$\displaystyle \int_{\overline{RP}} x dy = x_2(y_0-y_2) + \displaystyle \frac{1}{2} (x_0 - x_2)(y_0 - y_2)$$
から
$$M_{00} = \displaystyle \frac{1}{2} \left( (x_1-x_0)(y_2-y_0) - (x_2-x_0)(y_1-y_0)  \right)$$
一般には
$$M_{ij} = \displaystyle \frac{1}{i} \displaystyle \int_{\partial S} x^{i+1} y^j dy$$
なので、機械的に計算すればいい





三次元の場合に、同様のことを考える。四面体$V$の4頂点を$P_0=(x_0,y_0) , P_1=(x_1,y_1) , P_2=(x_2 , y_2) , P_3=(x_3,y_3)$として以下の量を計算する
$$M_{ijk} = \displaystyle \int_V x^i y^j z^k dx dy dz$$
Stokesの定理によって、境界上の積分に置き換えることができる
$$\displaystyle \int_{\triangle{P_0 P_1 P_2}} x dy dz = \displaystyle \int_{0}^{1} du \int_{0}^{1-u} dv \left( (1-u-v)x_0 + u x_1 + vx_2\right) \left[ (y_1 - y_0)(z_2 - z_0) - (y_2 - y_0)(z_1 - z_0) \right]$$
$$=  \left[ (y_1 - y_0)(z_2 - z_0) - (y_2 - y_0)(z_1 - z_0) \right] \displaystyle \int_{0}^{1} du \left( x_0(1-u) + \displaystyle \frac{1}{2} u(1-u)(x_1-x_0) + \displaystyle \frac{1}{2}(1-u)^2 (x_2 - x_0) \right)$$ 
$$= \displaystyle \frac{x_0+x_1+x_2}{6} \left[ (y_1 - y_0)(z_2 - z_0) - (y_2 - y_0)(z_1 - z_0) \right]$$


面の向きを考慮すると
$$M_{000} = -\displaystyle \int_{\triangle{P_0 P_1 P_2}} x dy dz + \displaystyle \int_{\triangle{P_1 P_2 P_3}} x dy dz -\displaystyle \int_{\triangle{P_2 P_3 P_0}} x dy dz + \displaystyle \int_{\triangle{P_3 P_0 P_1}} x dy dz$$
で、頑張って多項式の足し算を行うと
$$M_{000} = \displaystyle \frac{1}{6} \left| \begin{matrix} x_1 - x_0 & x_2 - x_0 & x_3 - x_0 \\ y_1 - y_0 & y_2-y_0 & y_3-y_0 \\ z_1-z_0 & z_2 -z_0 & z_3 -z_0 \end{matrix} \right|$$
というよく知られた公式を得る


以下、同様の計算であるので、sympyを使って、いくつか計算した結果を掲載しておく

$$M_{100} = \frac{1}{4} \left(x_{0} + x_{1} + x_{2} + x_{3}\right) M_{000}$$

$$M_{200} = \frac{1}{10} \left(x_{0}^{2} + x_{0} x_{1} + x_{0} x_{2} + x_{0} x_{3} + x_{1}^{2} + x_{1} x_{2} + x_{1} x_{3} + x_{2}^{2} + x_{2} x_{3} + x_{3}^{2}\right) M_{000}$$

$$M_{110} = \frac{1}{20} \left(2 x_{0} y_{0} + x_{0} y_{1} + x_{0} y_{2} + x_{0} y_{3} + x_{1} y_{0} + 2 x_{1} y_{1} + x_{1} y_{2} + x_{1} y_{3} + x_{2} y_{0} + x_{2} y_{1} + 2 x_{2} y_{2} + x_{2} y_{3} + x_{3} y_{0} + x_{3} y_{1} + x_{3} y_{2} + 2 x_{3} y_{3}\right) M_{000}$$

$$M_{300} = \frac{1}{20} \left(x_{0}^{3} + x_{0}^{2} x_{1} + x_{0}^{2} x_{2} + x_{0}^{2} x_{3} + x_{0} x_{1}^{2} + x_{0} x_{1} x_{2} + x_{0} x_{1} x_{3} + x_{0} x_{2}^{2} + x_{0} x_{2} x_{3} + x_{0} x_{3}^{2} + x_{1}^{3} + x_{1}^{2} x_{2} + x_{1}^{2} x_{3} + x_{1} x_{2}^{2} + x_{1} x_{2} x_{3} + x_{1} x_{3}^{2} + x_{2}^{3} + x_{2}^{2} x_{3} + x_{2} x_{3}^{2} + x_{3}^{3}\right) M_{000}$$

$$M_{210} = \frac{1}{60} \left(3 x_{0}^{2} y_{0} + x_{0}^{2} y_{1} + x_{0}^{2} y_{2} + x_{0}^{2} y_{3} + 2 x_{0} x_{1} y_{0} + 2 x_{0} x_{1} y_{1} + x_{0} x_{1} y_{2} + x_{0} x_{1} y_{3} + 2 x_{0} x_{2} y_{0} + x_{0} x_{2} y_{1} + 2 x_{0} x_{2} y_{2} + x_{0} x_{2} y_{3} + 2 x_{0} x_{3} y_{0} + x_{0} x_{3} y_{1} + x_{0} x_{3} y_{2} + 2 x_{0} x_{3} y_{3} + x_{1}^{2} y_{0} + 3 x_{1}^{2} y_{1} + x_{1}^{2} y_{2} + x_{1}^{2} y_{3} + x_{1} x_{2} y_{0} + 2 x_{1} x_{2} y_{1} + 2 x_{1} x_{2} y_{2} + x_{1} x_{2} y_{3} + x_{1} x_{3} y_{0} + 2 x_{1} x_{3} y_{1} + x_{1} x_{3} y_{2} + 2 x_{1} x_{3} y_{3} + x_{2}^{2} y_{0} + x_{2}^{2} y_{1} + 3 x_{2}^{2} y_{2} + x_{2}^{2} y_{3} + x_{2} x_{3} y_{0} + x_{2} x_{3} y_{1} + 2 x_{2} x_{3} y_{2} + 2 x_{2} x_{3} y_{3} + x_{3}^{2} y_{0} + x_{3}^{2} y_{1} + x_{3}^{2} y_{2} + 3 x_{3}^{2} y_{3}\right) M_{000}$$

$$M_{111} = \frac{1}{120} \left(6 x_{0} y_{0} z_{0} + 2 x_{0} y_{0} z_{1} + 2 x_{0} y_{0} z_{2} + 2 x_{0} y_{0} z_{3} + 2 x_{0} y_{1} z_{0} + 2 x_{0} y_{1} z_{1} + x_{0} y_{1} z_{2} + x_{0} y_{1} z_{3} + 2 x_{0} y_{2} z_{0} + x_{0} y_{2} z_{1} + 2 x_{0} y_{2} z_{2} + x_{0} y_{2} z_{3} + 2 x_{0} y_{3} z_{0} + x_{0} y_{3} z_{1} + x_{0} y_{3} z_{2} + 2 x_{0} y_{3} z_{3} + 2 x_{1} y_{0} z_{0} + 2 x_{1} y_{0} z_{1} + x_{1} y_{0} z_{2} + x_{1} y_{0} z_{3} + 2 x_{1} y_{1} z_{0} + 6 x_{1} y_{1} z_{1} + 2 x_{1} y_{1} z_{2} + 2 x_{1} y_{1} z_{3} + x_{1} y_{2} z_{0} + 2 x_{1} y_{2} z_{1} + 2 x_{1} y_{2} z_{2} + x_{1} y_{2} z_{3} + x_{1} y_{3} z_{0} + 2 x_{1} y_{3} z_{1} + x_{1} y_{3} z_{2} + 2 x_{1} y_{3} z_{3} + 2 x_{2} y_{0} z_{0} + x_{2} y_{0} z_{1} + 2 x_{2} y_{0} z_{2} + x_{2} y_{0} z_{3} + x_{2} y_{1} z_{0} + 2 x_{2} y_{1} z_{1} + 2 x_{2} y_{1} z_{2} + x_{2} y_{1} z_{3} + 2 x_{2} y_{2} z_{0} + 2 x_{2} y_{2} z_{1} + 6 x_{2} y_{2} z_{2} + 2 x_{2} y_{2} z_{3} + x_{2} y_{3} z_{0} + x_{2} y_{3} z_{1} + 2 x_{2} y_{3} z_{2} + 2 x_{2} y_{3} z_{3} + 2 x_{3} y_{0} z_{0} + x_{3} y_{0} z_{1} + x_{3} y_{0} z_{2} + 2 x_{3} y_{0} z_{3} + x_{3} y_{1} z_{0} + 2 x_{3} y_{1} z_{1} + x_{3} y_{1} z_{2} + 2 x_{3} y_{1} z_{3} + x_{3} y_{2} z_{0} + x_{3} y_{2} z_{1} + 2 x_{3} y_{2} z_{2} + 2 x_{3} y_{2} z_{3} + 2 x_{3} y_{3} z_{0} + 2 x_{3} y_{3} z_{1} + 2 x_{3} y_{3} z_{2} + 6 x_{3} y_{3} z_{3}\right) M_{000}$$



```
import sympy
x0,y0,z0 = sympy.symbols("x0 y0 z0")
x1,y1,z1 = sympy.symbols("x1 y1 z1")
x2,y2,z2 = sympy.symbols("x2 y2 z2")
x3,y3,z3 = sympy.symbols("x3 y3 z3")


def m3(i,j,k):
   u,v = sympy.symbols("u v")
   J=(y1-y0)*(z2-z0)-(y2-y0)*(z1-z0)
   f = ( (x0 + u*(x1-x0) + v*(x2-x0))**(i+1)/(i+1) )*( (y0 + u*(y1-y0) + v*(y2-y0))**j )*( (z0 + u*(z1-z0) + v*(z2-z0))**k )
   g012 = sympy.integrate(sympy.integrate(f , (v,0,1-u)) , (u,0,1))*J
   g123 = g012.subs({x0:x1,x1:x2,x2:x3,y0:y1,y1:y2,y2:y3,z0:z1,z1:z2,z2:z3} , simultaneous=True)
   g230 = g123.subs({x1:x2,x2:x3,x3:x0,y1:y2,y2:y3,y3:y0,z1:z2,z2:z3,z3:z0} , simultaneous=True)
   g301 = g230.subs({x2:x3,x3:x0,x0:x1,y2:y3,y3:y0,y0:y1,z2:z3,z3:z0,z0:z1} , simultaneous=True)
   return sympy.factor(-g012+g123-g230+g301)


if __name__=="__main__":
   print(sympy.latex( sympy.factor(m3(1,0,0)/m3(0,0,0)) ))
   print(sympy.latex( sympy.factor(m3(2,0,0)/m3(0,0,0)) ))
   print(sympy.latex( sympy.factor(m3(1,1,0)/m3(0,0,0)) ))
   print(sympy.latex( sympy.factor(m3(3,0,0)/m3(0,0,0)) ))
   print(sympy.latex( sympy.factor(m3(2,1,0)/m3(0,0,0)) ))
   print(sympy.latex( sympy.factor(m3(1,1,1)/m3(0,0,0)) ))


```

