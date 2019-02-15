---
title: cut-and-join operator
---
# cut-and-join operator
cut-and-join operatorと誰が呼ぶようになったのかは分からない(cut-and-join equationという漸化式があって、それと同等の微分作用素という意味で名付けられたのだと思うけど)けれど、初出は以下の論文らしい

A Differential Operator for Symmetric Functions and the Combinatorics of Multiplying Transpositions

http://www.ams.org/journals/tran/1994-344-01/S0002-9947-1994-1249468-3/

##cut-and-join operatorとSchur多項式

cut-and-join operatorは$W_3$代数の0モードの生成元として定義できる($gl(\infty)$の普遍展開環の中心元と思うのが正しいらしい)。$W_3$代数は、Virasoro代数の一般化で、$L_n,J_n(n \in \mathbf{Z})$を生成元として、やや複雑な関係式で定義される。$L_n$はHeisenberg代数

$[H_n,H_m] = n \cdot \delta_{n+m,0}$

を使って自由場表示

$L_n = \dfrac{1}{2} \displaystyle \sum_{a+b=n} : H_a H_b :$

が存在する。これに対応して、

$J_n = \dfrac{1}{3} \displaystyle \sum_{a+b+c=n} : H_a H_b H_c :$

という自由場表示があり、

$H_n = \dfrac{\partial}{\partial t_n} \quad (n > 0)$

$H_{-n} = n t_n \quad (n > 0)$

$H_0 = 0$

という表現に対して、$J_0$を計算したものが、標準的なcut-and-join operatorと(定数倍を除いて)一致する。直接計算によって

$J_0 = \displaystyle \sum_{a,b=1}^{\infty} \left( ab t_a t_b \dfrac{\partial}{\partial t_{a+b}} + (a+b)t_{a+b} \dfrac{\partial}{\partial t_a} \dfrac{\partial}{\partial t_b} \right)$

を得る。

&nbsp;

cut-and-join operatorの著しい性質として、Schur多項式が固有関数となっていることがある。これは、Virasoro代数の0-モードの生成元

$L_0 = \displaystyle \sum_{n=1}^{\infty} n t_n \dfrac{\partial}{\partial t_n}$

についても成り立つ性質である($L_0$の方は、単に次数作用素に過ぎない)

$s_0 = 1$

$s_1 = t_1$

$s_2 = \dfrac{1}{2}t_1^2 + t_2$

$s_{1,1} = \dfrac{1}{2}t_1^2 - t_2$

$s_3 = \dfrac{1}{6}t_1^3 + t_1t_2 + t_3$

$s_{2,1} = \dfrac{1}{3}t_1^3 - t_3$

$s_{1,1,1} = \dfrac{1}{6}t_1^3 - t_1 t_2 + t_3$

$s_4 = \dfrac{1}{24}t_1^4 + t_1 t_3 + \dfrac{1}{2}t_1^2t_2 + \dfrac{1}{2}t_2^2 + t_4$

$s_{3,1} = \dfrac{1}{8} t_1^4 + \dfrac{1}{2} t_1^2 t_2 - \dfrac{1}{2}t_2^2 - t_4$

$s_{2,2} = \dfrac{1}{12}t_1^4 - t_1t_3 + t_2^2$

$s_{2,1,1} = \dfrac{1}{8}t_1^4 - \dfrac{1}{2}t_1^2 t_2 - \dfrac{1}{2}t_2^2 + t_4$

$s_{1,1,1,1} = \dfrac{1}{24}t_1^4 + t_1 t_3 - \dfrac{1}{2}t_1^2t_2 + \dfrac{1}{2}t_2^2 - t_4$

etc.に対して、計算して見ると、規則性は何となく分かる。証明は、例えば

Generation of Matrix Models by W-operators

http://arxiv.org/abs/0902.2627

あたりを参照。


##　位相的弦理論の分配関数のW-representation
ところで、上記論文”Generation of Matrix Models by W-operators”の主題は、Hermitian Matrix modelの分配関数やHurwitz tau functionが、$W_3$代数の生成元のexponentialを適当な関数に作用させることで得られるという観察にある(“W-representation”とか呼ばれるっぽい)

Kontsevich-Witten τ関数についても同様の表示が知られている。

Cut-and-Join operator representation for Kontsevich-Witten tau-function

http://arxiv.org/abs/1009.4887

ここで使われている、cut-and-join operatorに似た作用素は

$\dfrac{1}{3} \displaystyle \sum_{a+b+c=-3} : H_{2a+1} H_{2b+1} H_{2c+1} : + \dfrac{1}{16} H_{-3}$

という表示を持つ

KdV階層のVirasoro対称性とKontsevich-Witten分配関数

http://formalgroup.tumblr.com/post/55961562768/kdv-virasoro-kontsevich-witten

も参照

現在のところ、位相的極小模型や一般の位相的シグマ模型の分配関数に対して、類似の表現があるかどうかは分かってないらしい

その他

Complete Set of Cut-and-Join Operators in Hurwitz-Kontsevich Theory

http://arxiv.org/abs/0904.4227

&nbsp;

Matrix Models for Random Partitions

http://arxiv.org/abs/1005.5715

## Calogero-Sutherlandハミルトニアンとcut-and-join operator

Calogero-Sutherland模型のハミルトニアンは、Schur多項式の変形であるJack多項式を固有関数に持つことが知られているけれども、それは、cut-and-join operatorの変形を与えていると見なすことができる。自由場表示の導出については、

Collective fields, Calogero-Sutherland model and generalized matrix models

http://arxiv.org/abs/hep-th/9411053

$L_0 = \displaystyle \sum_{n>0} H_{-n} H_n$に比例する項は、比例係数に粒子数$N$に依存する項が入っているけども、全てのJack多項式を扱うためには、$N \to \infty$の極限を取るので、この項を無視する。Jack多項式は$L_0$の固有関数でもあるので、Calogero-Sutherland Hamiltonianから、この項を引いても、作用素は、Jack多項式を固有関数に持つ。具体的に、$t_n$座標で書くと

$H = \displaystyle \sum_{a,b=1}^{\infty} \left( (a+b)t_{a+b} \dfrac{\partial}{\partial t_a} \dfrac{\partial}{\partial t_b} + \beta a b t_a t_b \dfrac{\partial}{\partial t_{a+b}} \right) + \displaystyle \sum_{a=1}^{\infty} (1-\beta)a^2 t_a \dfrac{\partial}{\partial t_a}$

となる。$\beta=1$の時、これはcut-and-join operatorに一致するので、β変形を与えていると見なすことができる(Calogero-Sutherland模型の標準的な座標と、$t_n$座標とは、いわゆる三輪変換で結びついている)


## 2014/9/23追記

この式は

Sekiguchi-Debiard operators at infinity

http://arxiv.org/abs/1212.2781

などに明示的に書いてある。$L_0$と$H$は、それぞれ1階、2階の微分作用素であるが、同様に、自然数$n$に対して、$n$階の微分作用素を具体的に構成し、互いに可換であることを示している。

Integrable Hierarchy of the Quantum Benjamin-Ono Equation

http://arxiv.org/abs/1309.6464

でも、違った形で、”higher order Hamiltonian”を与えている


Calogero-Sutherland HamiltonianはRuijsenaars模型のHamiltonianの極限として得られ、CS模型の波動関数であるJack多項式も、Macdonald多項式の極限として得られる。この場合も、粒子数を無限に持っていくことができ、同様に、全ての次数のHamiltonianを構成しているのが以下の論文。

Macdonald operators at infinity

http://arxiv.org/abs/1212.2960
