#### Table of Contents

- [Die reelle projektive Ebene](#sec1)
  - [Punkte und Geraden im R^2](#sec1.1)
  - [Inzidenz, Join und Meet](#sec1.2)
- [projektive Transformationen](#sec2)
  - [Die Rolle von Matrix](#sec2.1)
  - [Projektive Transformationen berechnen](#sec2.2)
- [Dualitaet](#sec3)
  - [Symmetrie zwischen Punkten und Geraden](#sec3.1)
- [Die Projektive Gerade](#sec4)
  - [Homogene Koordinaten im RP^1](#sec4.1)
  - [Perspektiven und Transformationen](#sec4.2)
- KegelSchinitte



<h1 id="sec1">Die reelle projektive Ebene</h1>

<h3 id = "sec1.1">Punkte und Geraden im R^2</h3>	

1. Naiver Ansatz

   Punkte im  $R^2$ als $\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$ $\in$  $R^2$ 

2. Homogenisierung
	$\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$ $\rightarrow$  $\begin{bmatrix} x_1 \\ x_2 \\ 1 \end{bmatrix}$ $\sim$ $\begin{bmatrix} \lambda \cdot x_1 \\ \lambda \cdot x_2  \\ \lambda \end{bmatrix}$ , where $\lambda \neq 0$  
  
  - $\lim_{\lambda\to\infty}\begin{bmatrix} \lambda \cdot x_1 \\ \lambda \cdot x_2  \\ 1 \end{bmatrix}$ $\sim \lim_{\lambda\to\infty } \begin{bmatrix} x_1 \\ x_2 \\ 1/\lambda \end{bmatrix} \sim \begin{bmatrix} x_1 \\ x_2 \\ 0 \end{bmatrix} $ ==无限远的点==
  
3. De-Homogenisierung

  $\begin{bmatrix} x_1 \\ x_2 \\ 1 \end{bmatrix}$ $\rightarrow$  $\begin{bmatrix} x_1/z \\ x_2/z \end{bmatrix}$, where $z \neq 0$

4. Menge aller Punkte

  $$
  \mathscr{P}_{\mathbb{R}}:=\frac{\mathbb{R}^{3}-\{\mathbf{0}\}}{\mathbb{R}-\{0\}}
 \\
 [p]:=\{\lambda p \mid \lambda \in \mathbb{R}, \lambda \neq 0\}, p \in \mathbb{R}^{3}-\{\mathbf{0}\}
  $$
  
5. Geraden

   - Naiver Ansatz: $l$ := $\left\{\left(\begin{array}{l}x \\ y\end{array}\right) \in \mathbb{R}^{2} \mid a \cdot x+b \cdot y+c=0\right\}$

     Gerade dargestellt als:

     $$
     \left(\begin{array}{l}a \\ b \\ c\end{array}\right) \sim\left(\begin{array}{l}\lambda \cdot a \\ \lambda \cdot b \\ \lambda \cdot c\end{array}\right) \quad \lambda \neq 0
     $$

     

     ==一个点$(x,y)$在$l$上 <=> $(x,y,1)$垂直于$(a,b,c)$== (满足向量积等于0)
     
     - 由无限远的点构成的直线 **Gerade im Unendlichen** $l_{\infty} = \left(\begin{array}{l}
       0 \\
       0 \\
       1
       \end{array}\right)$ 
       $$
       \left(\begin{array}{l}
       0 \\
       0 \\
       1
       \end{array}\right) \cdot \left[\begin{array}{c}
       x_{1} \\
       x_{2} \\
       0
       \end{array}\right] = 0
       $$
   
6. Menge aller Geraden:
   $$
   \begin{array}{l}
   \mathscr{L}_{\mathbb{R}}:=\frac{\mathbb{R}^{3}-\{\boldsymbol{0}\}}{\mathbb{R}-\{0\}} \\
   \end{array}\\
   {[l]:=\{\lambda l \mid \lambda \in \mathbb{R}, \lambda \neq 0\}}, l \in \mathbb{R}^{3}-\{\mathbf{0}\}
   $$
   
   

7. Inzidenz: Wann liegt ein Punkt auf einer Geraden? ==点位于直线上==
   $$
   [p] \mathscr{F}_{R}[l]: \Longleftrightarrow\langle p, l\rangle=0
   $$

> 点和直线都可以用三维向量表示



8. Die reelle projektive Ebene: $\left(\mathscr{P}_{\mathbb{R}}, \mathscr{L}_{\mathbb{R}}, \mathcal{F}_{\mathbb{R}}\right)$

9. Verbindungsgerade: ==两个点连接成的线==
   $$
   p, q \in \mathscr{P}_{\mathbb{R}} \quad[l]=[p \times q]
   $$

10. Schnittpunkt: ==两条线的交点== 
    $$
    l, m \in \mathscr{L}_{\mathbb{R}} \quad[p]=[l \times m]
    $$



<h3 id ="sec1.2">Inzidenz, Join und Meet</h3>



1. Inzidenz: Wann liegt ein Punkt auf einer Geraden? ==点位于直线上==
$$
\begin{aligned}
\quad[p] \mathscr{I}_{\mathbb{R}}[l]: \Longleftrightarrow\langle p, l\rangle=0 & \Longleftrightarrow \quad \lambda \cdot \mu \cdot\langle p, l\rangle=0 \\
& \Longleftrightarrow \quad\langle\lambda \cdot p, \mu \cdot l\rangle=0 \\
& \Longleftrightarrow[\lambda p] \mathscr{F}_{\mathbb{R}}[\mu l]
\end{aligned}
$$

2. join: Verbindungsgerade
   $$
   \operatorname{join}([p],[q]):=[p \times q]
   $$

3. meet: Schnitt
   $$
   \operatorname{meet}([l],[m]):=[l \times m]
   $$

4. Kollinearität: 共线性

   ==三点位于一条直线==: $[p],[q],[r]$ sind inzident zu einer Geraden $\Longleftrightarrow \operatorname{det}(p, q, r)=0$

   Bew:
   $\left(\begin{array}{ccc}p_{x} & p_{y} & p_{z} \\ q_{x} & q_{y} & q_{z} \\ r_{x} & r_{y} & r_{z}\end{array}\right)\left(\begin{array}{l}a \\ b \\ c\end{array}\right)=\left(\begin{array}{l}0 \\ 0 \\ 0\end{array}\right)$ Hat nicht-triviale Lösungen g.d.w. $\operatorname{det}(p, q, r) \neq 0$

5. Standardeinbettung: **Zeichenebene auf z = 1**

   - die spezielle Rolle der "Ferngeraden" entsteht nur durch die geometrische Interprretation
   - Alle unendlich fernen Punkte liegen auf der "Ferngeraden".
   - Parallelen schneiden sich in Fernpunkten ==平行线相交于Fernpunkten==

   

6. Schnittpunkte in Standardeinbettung

  - Fall1: sich schneidende eindliche Geraden

    ![image-20210201202339565](https://i.loli.net/2021/02/02/6zS1DsiX79BGtyT.png)

    $$
    \left(\begin{array}{l}a_{1} \\ b_{1} \\ c_{1}\end{array}\right) \times\left(\begin{array}{l}a_{2} \\ b_{2} \\ c_{2}\end{array}\right)=\left(\begin{array}{c}. \\ \cdot \\ *\end{array}\right)
    $$

    - $\operatorname{det}\left(\begin{array}{ll}a_{1} & a_{2} \\ b_{1} & b_{2}\end{array}\right) \neq 0$, then "$*$" $\neq 0$

  - Fall2: parallele Geraden

    ![image-20210201203144705](https://i.loli.net/2021/02/02/oxGklObAyFJ7fdt.png)
    $$
    \begin{array}{l}
    \left(\begin{array}{l}
    a_{1} \\
    b_{1} \\
    c_{1}
    \end{array}\right) \times\left(\begin{array}{l}
    a_{2} \\
    b_{2} \\
    c_{2}
    \end{array}\right)=\left(\begin{array}{c}
    . \\
    \cdot \\
    0
    \end{array}\right) \\
    
    \end{array}
    $$
    
    - $\operatorname{det}\left(\begin{array}{ll}
    a_{1} & a_{2} \\
      b_{1} & b_{2}
      \end{array}\right)=0$
    - 交点为无限远的点
    
- Fall3: endliche Geraden und Ferngerade
  
    ![image-20210201203315944](https://i.loli.net/2021/02/02/fbQvEoBWkKS2Ran.png)
    $$
    \left(\begin{array}{l}
    a \\
    b \\
    c
    \end{array}\right) \times\left(\begin{array}{l}
    0 \\
    0 \\
    1
    \end{array}\right)=\left(\begin{array}{c}
    b \\
    -a \\
    0
    \end{array}\right)
    $$
    
>  ==**Zwei verschiedene Garaden haben immer einen Schnittpunkt**==



7. Verbindungsgeraden in Standardeinbettung

   - Fall1: beinde Punkte endlich

     ![image-20210201203633641](https://i.loli.net/2021/02/02/Keynmz5RihqvXEH.png)

   - Fall2: ein Punkt endlich, einer Fernpunkte

     ![image-20210201203800119](https://i.loli.net/2021/02/02/TEgNYV9HFq51SCA.png)

   - Fall3: Zwei Fernpunkte

     ![image-20210201203838497](https://i.loli.net/2021/02/02/725deEmXGDpOs3U.png)

> ==**Zwei verschiedene Punkte haben immer eine Verbindungsgerade**==


8. Axiomatische Sichtweise 公理

   **Axiome der "projektiven Ebene"**:

   > A1: Zwei verschiedene Geraden haben immer einen Schnittpunkt
   > A2: Zwei verschiedene Punkte haben immer eine Verbindungsgerade
   > A3: nicht-Degeneriertsheitsbedingung

   <u>**Satz**</u>: $(\underbrace{\mathscr{P}_{\mathbb{R}}, \mathscr{L}_{\mathbb{R}}, \mathscr{I}_{\mathbb{R}}}_{\mathbb{R} \mathbb{P}^{2}})$ ist eine projektive Ebene!

   - R: real, P: projective, $^{2}$: Ebene
   - Später: $\mathbb{R} \mathbb{P}^{1}, \mathbb{R} \mathbb{P}^{d}, \mathbb{C} \mathbb{P}^{1}, \ldots, \mathbb{K} \mathbb{P}^{d}$

9. Die Parallele zu einer Geraden durch einen Punkt

   ==求与ｌ平行且经过点Ｐ的直线ｇ==

   ![image-20210201205052375](https://i.loli.net/2021/02/02/1J8jTBqHbmgKSOU.png)

10. Satz von Pappos, ein Inzidenzsatz

    In mathematics, Pappus's hexagon theorem (attributed to Pappus of Alexandria) states that

    - given one set of collinear points $A, B, C,$ and another set of collinear points $a, b, c,$ then the intersection points $X, Y, Z$ of line pairs $A b$ and $a B, A c$ and $a C, B c$ and $b C$ are collinear, lying on the Pappus line. These three points are the points of intersection of the "opposite" sides of the hexagon $A b C a B c .$

      <img src="https://i.loli.net/2021/02/02/L9JdFqKiEW8PQgV.png" alt="img" style="zoom: 33%;" />

    

<h1 id = "sec2">Projektive Transformationen</h1>

<h3 id = "sec2.1">Die Rolle von Matrizen</h3>


1. Rotationen und Verschiebungen

   - Rotation im $R^{2}$
     $$
     \left(\begin{array}{l}
     x \\
     y
     \end{array}\right) \mapsto\left(\begin{array}{cc}
     \cos (\alpha) & -\sin (\alpha) \\
     \sin (\alpha) & \cos (\alpha)
     \end{array}\right)\left(\begin{array}{l}
     x \\
     y
     \end{array}\right)
     $$

     - projektiv:
       $$
       \left(\begin{array}{l}
       x \\
       y \\
       1
       \end{array}\right) \mapsto\left(\begin{array}{ccc}
       \cos (\alpha) & -\sin (\alpha) & 0 \\
       \sin (\alpha) & \cos (\alpha) & 0 \\
       0 & 0 & 1
       \end{array}\right)\left(\begin{array}{l}
       x \\
       y \\
       1
       \end{array}\right)
       $$
       
     
       
     
   - Translation im $R^{2}$
     $$
     \left(\begin{array}{l}
     x \\
     y
     \end{array}\right) \mapsto\left(\begin{array}{l}
     x \\
     y
     \end{array}\right)+\left(\begin{array}{l}
     t_{x} \\
     t_{y}
     \end{array}\right)
     $$

     - projektiv:
       $$
       \left(\begin{array}{l}
       x \\
       y \\
       1
       \end{array}\right) \mapsto\left(\begin{array}{lll}
       1 & 0 & t_{x} \\
       0 & 1 & t_{y} \\
       0 & 0 & 1
       \end{array}\right)\left(\begin{array}{l}
       x \\
       y \\
       1
       \end{array}\right)
       $$
     
   - Affine Transformation 仿射变换

     仿射变换（Affine transformation），又称仿射映射，是指在几何中，對一个向量空间进行一次线性变换并接上一个平移，变换为另一个向量空间。
     $$
     \left(\begin{array}{l}
     x \\
     y \\
     1
     \end{array}\right) \mapsto\left(\begin{array}{lll}
     a & b & c \\
     d & e & f \\
     0 & 0 & 1
     \end{array}\right)\left(\begin{array}{l}
     x \\
     y \\
     1
     \end{array}\right)
     $$
     ![image-20210202141835343](https://i.loli.net/2021/02/02/zJ37y6Ub2Q5VDwN.png)

   - Allgemeine projektive Transformation
     $$
     \left[\left(\begin{array}{l}
     x \\
     y \\
     z
     \end{array}\right)\right] \mapsto  \left[\underbrace{\left(\begin{array}{lll}
     a & b & c \\
     d & e & f \\
     g & h & i
     \end{array}\right)}_{\operatorname{det}(M) \neq 0}\left(\begin{array}{l}
     x \\
     y \\
     z
     \end{array}\right)\right]
     $$

     - ist wohldefiniert
     - $\tau_{M}: \mathscr{P}_{\mathbb{R}} \rightarrow \mathscr{P}_{\mathbb{R}}$
     - führt Geraden in Geraden über

     

2.  Projektive Transformationen und Kollinearität

   > **==Satz (2.2): Projektive Transformationen führen kollineare Punktetripel in kollineare Punktetripel über.==**

   Bew:
   Es seien $[p],[q],[r]$ drei kollineare Punkte also $\operatorname{det}(p, q, r)=0$.
   Sei $M \in \mathbb{R}^{3 \times 3}$ mit $\operatorname{det}(M) \neq 0$.
   Betrachte $\operatorname{det}(M p, M q, M r)$
   $\operatorname{det}(M p, M q, M r)=\operatorname{det}(M) \cdot \operatorname{det}(p, q, r)$
   $\Longrightarrow \operatorname{det}(M p, M q, M r)=0$
   $\Longrightarrow[M p],[M q],[M r]$ kollinear.

3. Projektive Transformation "konstruieren"

   ![image-20210202145542629](https://i.loli.net/2021/02/02/eTyAc93gtDMxvUE.png)

   Die Matrix $M$ ist bis auf ein Vielfaches durch Bild und Urbild von vier Punkten bestimmt.



<h3 id="sec2.2">Projektive Transformationen berechnen</h3>

> **==Satz (2.3.): Es seien [A], [B], [C], [D] vier Punkte von denen keine drei auf einer Geraden liegen und $[A^{'}],[B^{'}],[C^{'}],[D^{'}]$ ebenso.==**
>
> **==Dann gibt es genau eine Äquivalenzklasse $[M]$ mit==**
> $$
> [M A]=[A'],[M B]=[B'],[M C]=[C'],[M D]=[D']
> $$


​    变换前后任意三点都不共线，则$M$唯一



1. Wirkungen von Projektiven Transformationen auf Geraden

   Punkte:																	Geraden:
$\begin{aligned} \tau_{M}: \mathscr{P}_{\mathbb{R}} & \rightarrow \mathscr{P}_{\mathbb{R}} \\ &[p] \mapsto[M p] \end{aligned}$											$\begin{aligned} \tau: \mathscr{L}_{\mathbb{R}} & \rightarrow \mathscr{L}_{\mathbb{R}} \\ &[l] \mapsto\left[\left(M^{T}\right)^{-1} l\right] \end{aligned}$						


2.  Freiheitsgrade zählen

   Die Menge der projektiven Transformationen im $\mathbb{R} \mathbb{P}^{2}$ bildet einen 8-dimensionale "Manigfaltigkeit".

3. Ueber den Tellerrand

   Kollineation: Jede bijektive Abbildung auf $\mathscr{P}_{\mathbb{R}}$ ,die Geraden in Geraden überführt
   proj. Trafo.: Multiplikation mit reeller invertierbarer $
   3 \times 3 \text { Matrix }([p] \mapsto[M p])
   $

   - Jede projektive Transformation ist Kollineation
   - Über $\mathbb{R}$ ist iede Kollineation eine projektive Transformation



<h1 id = "sec3">Dualitaet</h1>

<h3 id ="sec3.1">Symmetrie zwischen Punkten und Geraden</h3>

1. Wörterbuch der Dualität

   ![image-20210205101102302](https://i.loli.net/2021/02/05/VTCz9X2mLyhbWoe.png)

2.  Satz von Pappos und sein Duales

   ![image-20210205103157163](https://i.loli.net/2021/02/05/CQNcdWmYsHfyqD1.png)

3. Satz von Pascal und dein Duales, der Satz von Brianchon

   ![image-20210205103827033](https://i.loli.net/2021/02/05/Fygf9THpVd1icYj.png)

4. 

<h1 id = "sec4">Die Projektive Gerade</h1>

<h3 id = "sec4.1">Homogene Koordinaten im RP^1</h3>

1. Geometrie entlang einer Geraden im $\mathbb{R} \mathbb{P}^{2}$

   ![image-20210205165028520](https://i.loli.net/2021/02/05/qF1fjQItTzkSnOB.png)

   Die Punkte auf der Verbindungsgerade von $[A]$ und $[B]$ sind die Punkte der Form
   $$
   [P]=[\lambda A+\mu B] \quad\left(\begin{array}{l}
   \lambda \\
   \mu
   \end{array}\right) \neq\left(\begin{array}{l}
   0 \\
   0
   \end{array}\right)
   $$
   Beweis:
   (i) $[\lambda A+\mu B]$ liegt auf $l=\operatorname{join}(A, B)$.
   $$
   \operatorname{det}(A, B, \lambda A+\mu B)=\operatorname{det}(A, B, \lambda A)+\operatorname{det}(A, B, \mu B)=0
   $$
   (ii) Jeder Punkt auf $\operatorname{join}(A, B)$ hat die Form $[\lambda A+\mu B]$. 

   ​		Sei $[A],[B],[P]$ kollinear. D.h:

   ​		$\left.\left(\begin{array}{lll}| & | & | \\ A & B & P \\ | & | & |\end{array}\right)\left(\begin{array}{l}x_{1} \\ x_{2} \\ x_{3}\end{array}\right)=\left(\begin{array}{l}0 \\ 0 \\ 0\end{array}\right) \begin{array}{l}\text { hat nicht- } \\ \text { triviale Lösung }\end{array}\right\}$

   ​		

   ​		wg. $[A] \neq[B]$, gilt $x_{3} \neq 0$, 

   ​		Also $P=\lambda A+\mu B$ mit $\quad\left(\begin{array}{l}\lambda \\ \mu\end{array}\right) \neq\left(\begin{array}{l}0 \\ 0\end{array}\right)$

   > <u>**Achtung subtil**</u>: die exakte Position von $[P]$ hängt von $A$ und $B$ aber nicht nur von $[A]$ und $[B]$ ab.

   ![image-20210205170454773](https://i.loli.net/2021/02/06/9N8OVrBwIFLplyT.png)

<h3 id = "sec4.2">Perspektiven und Transformationen</h3>

1. Basiswechsel auf der Geraden im $\mathbb{R P}^{2}$

   ![image-20210206151745688](https://i.loli.net/2021/02/06/MfWyp2ARGb6zkuK.png)
   $$
   \begin{array}{ll}
   P=\lambda A+\mu B & A^{\prime}=\lambda_{A} A+\mu_{A} B \\
   P=\lambda^{\prime} A^{\prime}+\mu^{\prime} B^{\prime} & B^{\prime}=\lambda_{B} A+\mu_{B} B
   \end{array}
   $$
   

   =>
   $$
   P=\lambda^{\prime}\left(\lambda_{A} A+\mu_{A} B\right) + \mu^{\prime}\left( \lambda_{B}A+\mu_{B} B\right.)
   $$

   $$
   =\underbrace{\left(\lambda^{\prime} \lambda_{A}+\mu^{\prime} \lambda_{B}\right.}_{\lambda}) A+(\underbrace{\lambda^{\prime} \mu_{A}+\mu^{\prime} \mu_{B}}_{\mu}) B
   $$

   Also:
   $$
   \left(\begin{array}{l}
   \lambda^{\prime} \\
   \mu^{\prime}
   \end{array}\right) \mapsto\left(\begin{array}{l}
   \lambda \\
   \mu
   \end{array}\right)=\left(\begin{array}{ll}
   \lambda_{A} & \lambda_{B} \\
   \mu_{A} & \mu_{B}
   \end{array}\right)\left(\begin{array}{l}
   \lambda^{\prime} \\
   \mu^{\prime}
   \end{array}\right)
   $$

2. Perspektivetaet

   ![image-20210206153318665](https://i.loli.net/2021/02/06/eDcoisBw5qNhmvn.png)
   $$
   \begin{array}{l}
   P=\lambda A+\mu B \\
   P^{\prime}=\lambda^{\prime} A^{\prime}+\mu^{\prime} B^{\prime}
   \end{array}
   $$
   Frage:
   wie hängt $\lambda^{\prime}, \mu^{\prime}$ von $\lambda, \mu$ ab?

   **==Satz==**: Es gibt ein $\tau$ mit:
   $$
   \left(\begin{array}{l}
   \lambda^{\prime} \\
   \mu^{\prime}
   \end{array}\right)=\left(\begin{array}{ll}
   \tau & 0 \\
   0 & 1
   \end{array}\right)\left(\begin{array}{l}
   \lambda \\
   \mu
   \end{array}\right)
   $$
   Beweis: Zeige: Es gibt ein $\tau$ so dass $X, P, P^{\prime}$ kollinear sind
   $$
   \begin{aligned}
   0=\left\langle P \times P^{\prime}, X\right\rangle=&\left\langle(\lambda A+\mu B) \times\left(\lambda^{\prime} A^{\prime}+\mu^{\prime} B^{\prime}\right), X\right\rangle \\
   =& \lambda \lambda^{\prime}\underbrace{\left\langle{A \times A^{\prime}, X}\right\rangle}_{0}+\lambda \mu^{\prime}\left\langle A \times B^{\prime}, X\right\rangle+\mu \lambda^{\prime}\left\langle B \times A^{\prime}, X\right\rangle+\mu \mu^{\prime}\underbrace{\left\langle{\left.B \times B^{\prime}, X\right\rangle}\right.}_{0}\\
   &\Longrightarrow \lambda \mu^{\prime}\left\langle{A \times B^{\prime}, X}\right\rangle=-\mu \lambda^{\prime}\left\langle B \times A^{\prime}, X\right\rangle \Longrightarrow \frac{\lambda^{\prime}}{\mu^{\prime}}=\frac{\lambda}{\mu} \cdot \underbrace{\left(\frac{\left\langle A \times B^{\prime}, X\right\rangle}{-\left\langle A^{\prime} \times B, X\right\rangle}\right)}_{\tau})
   \end{aligned}
   $$

3. Verkettung von Basiswechsel und Perspektivität/Projektion

   ![image-20210206154502433](https://i.loli.net/2021/02/06/Y8LfCwAyaDsS62d.png)

4. Die Projektive Gerade (intrinsische Definition)

   ![image-20210206160129709](https://i.loli.net/2021/02/06/pKxItFqPzGyXCr8.png)
   $$
   \begin{array}{l}
   \text { Homogenisierung: } \lambda \mapsto\left[\left(\begin{array}{l}
   \lambda \\
   1
   \end{array}\right)\right] \\
   \mathbb{R P}^{1}:=\frac{\mathbb{R}^{2}-\{\boldsymbol{0}\}}{\mathbb{R}-\{0\}} & \mathbb{K} \mathbb{P}^{d}:=\frac{\mathbb{K}^{d+1}-\{\boldsymbol{0}\}}{\mathbb{K}-\{0\}}
   \end{array}
   $$
   Projektive Transformationen:
   $$
   \left(\begin{array}{l}
   \lambda \\
   \mu
   \end{array}\right) \mapsto \underbrace{\left(\begin{array}{ll}
   a & b \\
   c & d
   \end{array}\right)}_{\operatorname{det} \neq 0}\left(\begin{array}{l}
   \lambda \\
   \mu
   \end{array}\right)
   $$

   $$
   \tau: \mathbb{R} \mathbb{P}^{1} \rightarrow \mathbb{R} \mathbb{P}^{1}
   $$

   $$
   [P] \mapsto[M \cdot P]
   $$

   

   
   $$
   \begin{array}{l}
   \mathbb{R} \stackrel{\text { hom }}{\rightarrow} \mathbb{R} \mathbb{P}^{1} \stackrel{\tau}{\rightarrow} \mathbb{R} \mathbb{P}^{1} \stackrel{\text { dehom }}{\rightarrow} \mathbb{R} \\
   \begin{aligned}
   x  \mapsto &\left(\begin{array}{l}
   x \\
   1
   \end{array}\right)  \mapsto\underbrace{\left(\begin{array}{ll}
   a & b \\
   c & d
   \end{array}\right)\left(\begin{array}{l}
   x \\
   1
   \end{array}\right)}_{\left(\begin{array}{c}
   a x+b \\
   c x+d
   \end{array}\right)} \mapsto \frac{a x+b}{c x+d} \\
   
   \end{aligned}
   \end{array}
   $$

