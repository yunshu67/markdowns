#### Table of Contents

- [Die reelle projektive Ebene](#sec1)
  - [Punkte und Geraden im R^2](#sec1.1)
  - [Inzidenz, Join und Meet](#sec1.2)
  - [summary](#sum1)
- [projektive Transformationen](#sec2)
  - [Die Rolle von Matrix](#sec2.1)
- Dualitaet
- Die Projektive Gerade
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

4. 

   


<h3 id = "sum1">Summary</h3>

1. Geraden in der Zeichenebene sind durch Gleichungen der Form
   $$
   a x+b y+c=0
   $$
   X-轴： $y=0  \Rightarrow  0x+1y+0=0  \Leftrightarrow \left(\begin{array}{l}
   0 \\
   1 \\
   0
   \end{array}\right)$

   Y-轴： $x=0  \Rightarrow  1x+0y+0=0  \Leftrightarrow \left(\begin{array}{l}
   1 \\
   0 \\
   0
   \end{array}\right)$


2. 