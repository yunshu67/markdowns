$\forall P: P \times P = 0$

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
  - [Doppelverhältnisse](#sec4.3)
  - [Projektive Skalen](#sec4.4)
  - [Harmonische Lage](#sec4.5)
  
- [KegelSchinitte](#sec5)
  
  - [Quadriken](#sec5.1)
  - [Kegelschnitt durch 5 Punkte](#sec5.2)
  - [Wo stand der Fotograph](#sec5.3)
  - [rojektive Klassifikation](#sec5.4)
  - [Polarität](#sec5.5)
  
- [Komplexe Zahlen und Geometrie](#sec6)

  - [Geometrie komplexer Zahlen](#sec6.1)
  - [Geometrie komplexer Rechenoperationen](#sec6.2)
  - [Die Punlte I und j](#sec6.3)
  - [Kozirkularitaet testen](#sec6.4)
  - [Kreise und I und J](#sec6.5)
  
- [Euklidische Geometrie](#sec7)
  
  - [senkrecht stehen und Winkel](#sec7.1)
  - [Elementargeometrie](#sec7.2)
  - [Transformationen](#sec7.3)
  - [Ausblick: Cayley-Klein Geometrien](#sec7.4)
  
  



<h1 style="color:green" id="sec1">Die reelle projektive Ebene</h1>

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

    

<h1 style="color:green" id = "sec2">Projektive Transformationen</h1>

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



<h1 style="color:green" id = "sec3">Dualitaet</h1>

<h3 id ="sec3.1">Symmetrie zwischen Punkten und Geraden</h3>

1. Wörterbuch der Dualität

   ![image-20210205101102302](https://i.loli.net/2021/02/05/VTCz9X2mLyhbWoe.png)

2.  Satz von Pappos und sein Duales

   ![image-20210205103157163](https://i.loli.net/2021/02/05/CQNcdWmYsHfyqD1.png)

3. Satz von Pascal und dein Duales, der Satz von Brianchon

   ![image-20210205103827033](https://i.loli.net/2021/02/05/Fygf9THpVd1icYj.png)

4. 

<h1 style="color:green" id = "sec4">Die Projektive Gerade</h1>

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

<h3 id = "sec4.3">Doppelverhaeltnisse</h3>

> **Schreibweise:**
> $$
> 1.[X, Y]:=\operatorname{det}\left(\begin{array}{ll}
> x_{1} & y_{1} \\
> x_{2} & y_{2}
> \end{array}\right)
> $$
>
> $$
> \begin{aligned}
> &2.[M X, M Y] \\
> =& \operatorname{det}\left(\begin{array}{cc}
> \mid & \mid \\
> M X & M Y \\
> \mid & \mid
> \end{array}\right) \\
> =& \operatorname{det}\left(M \cdot\left(\begin{array}{cc}
> \mid & \mid \\
> X & Y \\
> \mid & \mid
> \end{array}\right)\right) \\
> =& \operatorname{det}(M) \cdot[X, Y]
> \end{aligned}
> $$

1. Definition

   **Definition**: Seien $A, B, C, D \in \mathbb{R}^{2}-\{\mathbf{0}\}$, deren Doppelverhältnis ist definiert als:
   $$
   (A, B ; C, D):=\frac{[A, C][B, D]}{[A, D][B, C]}
   $$
   **Lemma1:** Für $\alpha, \beta, \gamma, \delta \neq 0$ ist
   $$
   (A, B ; C, D)=(\alpha A, \beta B ; \gamma C, \delta D)
   $$

   $$
   \rightarrow \text { unabhängig von Repräsentanten }
   $$
   Beweis:
   $(\alpha A, \beta B ; \gamma C, \delta D)=\frac{[\alpha A, \gamma C][\beta B, \delta D]}{[\alpha A, \delta D][\beta B, \gamma C]}=\frac{\alpha \beta \gamma \delta \cdot[A, C][B, D]}{\alpha \beta \gamma \delta \cdot[A, D][B, C]}=(A, B ; C, D)$

   ---

   **Lemma2:** Für $M \in \mathbb{R}^{2 \times 2} ; \operatorname{det}(M) \neq 0$ ist
   $$
   (A, B ; C, D)=(M \cdot A, M \cdot B ; M \cdot C, M \cdot D)
   $$

   $$
   \rightarrow \text { invariant unter Transformationen }
   $$

   Beweis:
   $(M \cdot A, M \cdot B ; M \cdot C, M \cdot D)=\frac{[M A, M C][M B, M D]}{[M A, M D][M B, M C]}=\frac{\operatorname{det}(M)^{2} \cdot[A, C][B, D]}{\operatorname{det}(M)^{2} \cdot[A, D][B, C]}=(A, B ; C, D)$

   

2. 

   ![image-20210206212300239](https://i.loli.net/2021/02/07/SYJkmI6PUlft2c8.png)
   $$
   \text{where: } x-y=\operatorname{det}\left(\begin{array}{ll}
   x & y \\
   1 & 1
   \end{array}\right)
   $$

3. 四条交于一点的直线的`Doppelverhaeltnis`: 

   ![image-20210206213121571](https://i.loli.net/2021/02/07/V8O5xfnQX9BGZm3.png)

   **Definition:** $(a, b ; c, d)$ ist das Doppelverhältnis von vier Geraden durch einen Punkt.

   ​					Vier kollineare Punkte haben ein Doppelverhältnis
$$
\begin{aligned}
   (A, B ; C, D) &=\left(A^{\prime}, B^{\prime} ; C^{\prime}, D\right) \\
   &=:(a, b ; c, d)
   \end{aligned}
$$

​		**Definition:** $(A, B ; C, D)_{X}$ ist das Doppelverhältnis von vier Punkten "gesehen von $X^{\prime \prime}$

$$
=\frac{[X, A, C][X, B, D]}{[X, A, D][X, B, C]}
$$

​		**==Satz==:**
$$
(A, B ; C, D)_{X}=\left(A^{\prime}, B^{\prime} ; C^{\prime}, D\right)_{X}
$$

4. Umgang mit $\infty$ - einige Rechenregeln
   $$
   \text { Rechenregeln: }\\
   \begin{aligned}
   &
   &\frac{1}{0}=\infty \quad \frac{1}{\infty}=0 \quad \infty+1=\infty \quad \infty+\infty=\infty \quad a \cdot \infty=\infty
   \end{aligned}
   $$
   
   $$
   \text{Nicht erlaubt:}\\
   \frac{0}{0}=\text { undef } \quad \frac{\infty}{\infty}=\text { undef } \quad 0 \cdot \infty=\text { undef }
   $$


<h3 id = "sec4.4">Projektive Skalen</h3>

> $(A, B ; C, D):=\frac{[A, C][B, D]}{[A, D][B, C]}$

1. Spezielle Doppelverhältnisse
   $$
   \begin{aligned}
   (A, B ; C, D)=0 & \Longrightarrow[A, C][B, D]=0 \\
   & \Longrightarrow[A, C]=0 \text { oder }[B, D]=0 \\
   & \Longrightarrow[A]=[C] \text { oder }[B]=[D]
   \end{aligned}
   $$

   ---

   $$
   (A, B ; C, D)=\infty \Longrightarrow[A]=[D] \text { oder }[B]=[C]
   $$

   ---

   $$
   (A, B ; C, D)=1 \Longrightarrow[A]=[B] \text { oder }[C]=[D]
   $$

   ---

   $$
   (0, \infty ; x, 1)=x
   $$



<h3 id ="sec4.5">Harmonische Lage</h3>

1. Vertauschen von Punkten im Doppelverhältnis
   $$
   \begin{aligned}
   &(A, B ; C, D):=\frac{[A, C][B, D]}{[A, D][B, C]}\\
   &(A, B ; C, D)=\lambda\\
   &(\mathbf{B}, \mathbf{A} ; C, D)=1 / \lambda\\
   &(A, B ; \mathbf{D},\mathbf{ C})=1 / \lambda\\
   &(A, \mathbf{C} ; \mathbf{B}, D)=1-\lambda\\
   &[A, B][C, D]-[A, C][B, D]+[A, D][B, C]=0\\
   &\text { Grassmann-Plücker-Relation }\\
   &(\underline{C, D} ; \underline{A, B})=\lambda
   \end{aligned}
   $$
   
   ---
   
2. 

$$
\begin{aligned}
&6 \text { mögliche Werte: }\\
&\begin{array}{llllll}
\underbrace{\lambda}_{id} &\underbrace{ \frac{1}{\lambda}}_{a} & \underbrace{1-\lambda}_{b} &\underbrace{ 1-\frac{1}{\lambda}}_{ab} &\underbrace{ \frac{1}{1-\lambda}}_{ba} &\underbrace{ \frac{\lambda}{\lambda-1}}_{aba/bab}
\end{array}\\

\end{aligned}
$$

2. Definition von Harmonischer Lage

   $(A, B ; C, D)=-1$
   $(A, B ; D, C)=-1$
   $(B, A ; C, D)=-1$
   $(C, D ; A, B)=-1$

   **==Definition==**: Das Paar von Paaren $\{\{A, B\},\{C, D\}\}$ heißt in harmonischer Lage, wenn $(A, B ; C ; D)=-1$.

3. Example

   ![image-20210208110747900](https://i.loli.net/2021/02/08/Pztiw7yLbje5Qdx.png)

<h1 style="color:green" id ="sec5">Kegelschnitte 圆锥曲线</h1>

<h3 id = "sec5.1">Quadriken 四边形</h3>

Lösungsgebilde 2-dimensionaler quadratischer Gleichungen:

Sei $a, b, c, d, e, f \in \mathbb{R}$ gegeben. Betrachte
$$
\begin{array}{l}
\qquad a x^{2}+b y^{2}+2 c x y+2 d x+2 e y+f=0 \\
\textbf  {etwas kompakter: } \left(\begin{array}{lll}
x & y & 1
\end{array}\right)\left(\begin{array}{lll}
a & c & d \\
c & b & e \\
d & e & f
\end{array}\right)\left(\begin{array}{l}
x \\
y \\
1
\end{array}\right)=0 \\
\quad\quad\quad\quad\quad\quad\quad \iff\quad\quad\quad\quad p^{T} \cdot A \cdot p=0
\end{array}
$$


定义: 
$$
\begin{aligned}
&\textbf{quadratische Form: }\quad Q_{A}(p):=p^{T} \cdot \underbrace{A}_{\begin{array}{c}
\text {kann symmetrisch} \\
\text {gewahlt werden}
\end{array}} \cdot p=0

\end{aligned}
$$
**Für nicht-symmetrische** $A$:
$$
Q_{\frac{A+A^{T}}{2} }(p)=Q_{A}(p)
$$
**homogen:** 
$$
\left(\begin{array}{lll}x & y & z\end{array}\right)\left(\begin{array}{lll}a & c & d \\ c & b & e \\ d & e & f\end{array}\right)\left(\begin{array}{l}x \\ y \\ z\end{array}\right)=0
$$

1. Definition von Quadriken

   **Definition**: Die Menge aller Punkte $p^{T}=(x, y, z)^{T}$, die die Gleichung
   $$
   \begin{aligned}
   &\iff a x^{2}+b y^{2}+2 c x y+2 d x z+2 e y z+f z^{2}=0\\
   &\iff \begin{array}{c}
   \left(\begin{array}{lll}
   x & y & z
   \end{array}\right)\left(\begin{array}{lll}
   a & c & d \\
   c & b & e \\
   d & e & f
   \end{array}\right)\left(\begin{array}{l}
   x \\
   y \\
   z
   \end{array}\right)=0 \end{array}\\
   &\iff Q_{A}(p):=p^{T} \cdot A \cdot p=0
   
   \end{aligned}
   $$
   erfüllen, nennt man eine Quadrik.




<h3 id = "sec5.2">Kegelschnitt durch 5 Punkte</h3>

![截屏2021-02-0910.20.10](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhem0qq5nj30wq098whg.jpg)

**==Satz==**: Durch 5 verschiedene Punkte $A, B, C, D, E$ im $\mathbb{R} \mathbb{P}^{2},$ von denen keine 4 auf einer Geraden liegen, geht immer (genau ein) Kegelschnitt.

![截屏2021-02-0910.46.58](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhfdqya5ej30x80c047x.jpg)

1. Degenerierter Kegelschnitt

   - der in zwei Geraden zerfällt:

     ![截屏2021-02-0910.24.10](https://tva1.sinaimg.cn/large/008eGmZEgy1gnheq07fqoj30dk0demzb.jpg)
     $$
     \begin{array}{l}
     \left(x r_{1}+y s_{1}+z t_{1}\right)=0 \text { oder }\left(x r_{2}+y s_{2}+z t_{2}\right)=0 \\
     \Longleftrightarrow\left(x r_{1}+y s_{1}+z t_{1}\right) \cdot\left(x r_{2}+y s_{2}+z t_{2}\right)=0 \\
     \Longleftrightarrow\langle P, l\rangle \cdot\langle P, m\rangle=0 \\
     \Longleftrightarrow\langle P, A \times B\rangle \cdot\langle P, C \times D\rangle=0 \\
     \Longleftrightarrow[P, A, B] \cdot[P, C, D]=0
     \end{array}
     $$
     

2. Bedingung für 6 Punkte auf einem gemeinsamen Kegelschnitt
   $$
   \begin{aligned}
   &[A C E][B D E][A D P][B C P]\\
   &-[A D E][B C E][A C P][B D P]=0\\
   &\frac{[A C E][B D E]}{[A D E][B C E]}=\frac{[A C P][B D P]}{[A D P][B C P]}
   \end{aligned}
   $$

   $$
   (A, B ; C, D)_{E}=(A, B ; C, D)_{P}
   $$

   > Der Punkt $P$ sieht $A, B, C, D$ unter dem selben Doppelverhältnis wie $E$.

   > Ein Kegelschnitt ist charakterisiert durch vier Punkte $A, B, C, D$ und ein Doppelverhältnis $\lambda$.

3. Eindeutigkeit eines Kegelschnitts durch 5 Punkte

   **==Satz==**: Durch 5 Punkte $A, B, C, D, E$ im $\mathbb{R} \mathbb{P}^{2},$ von denen keine **drei** auf
   einer Geraden liegen, geht immer (genau ein) Kegelschnitt



<h3 id = "sec5.3">Wo stand der Fotograph</h3>

<h3 id = "sec5.3">Projektive Klassifikation</h3>

1. Projektive Transformation eines Kegelschnitts

   Transformationen: $p \stackrel{\tau}{\longmapsto} M \cdot p$
   $$
   \begin{array}{l}
   l \stackrel{\tau}{\longrightarrow}\left(M^{-1}\right)^{T} \cdot l \leftarrow \text { erhält Inzidenz 投影后的点在投影后的直线上} \\
   A \stackrel{\tau}{\longrightarrow}\left(M^{-1}\right)^{T} \cdot A \cdot M^{-1} \leftarrow \text { erhält Inzidenz 投影后的点在投影后的圆锥曲线上}
   \end{array}
   $$
   ![截屏2021-02-0913.27.13](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhka5z4u8j307m05qjs6.jpg)

2. 点P在圆锥曲线A上：
   $$
   p^{T} \cdot A \cdot p = 0
   $$

3. 



![截屏2021-02-0913.42.17](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhkg4938jj30sc0ggdq6.jpg)

![截屏2021-02-0913.44.26](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhkicqzg5j30wa06cgp1.jpg)![截屏2021-02-0913.49.23](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhkni2rj6j30xi0buahf.jpg)

![截屏2021-02-0913.53.07](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhkrduf2mj30wo0cctgn.jpg)



4. Klassifikation des reellen nicht-degenerierten Kegelschnitts

   ![截屏2021-02-0913.56.01](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhkuk7znuj30vy0fqqb5.jpg)



<h3 id = "sec5.5">Polarity （Exkurs?）</h3>

1. Die Polaritätsabbildung 

<h1 id = "sec6" style="color:green"> Komplexe Zahlen und Geometrie</h1>

<h3 id = "sec6.1">Geometrie komplexer Zahlen</h3>

1. Wiederholung der Grundlagen komplexer Zahlen

   $\mathbb{C}=\mathbb{R}+i \mathbb{R}$

   <img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gnhnsc33w8j30cs0aogmx.jpg" alt="截屏2021-02-0915.37.49" style="zoom:33%;" />

   **Imaginäre Einheit: **
   $$
   i^{2}=-1
   $$
   
   **Komplexe Zahlen:**
   $$
   a, b \in \mathbb{R} \\ 
   a+i b \in \mathbb{C}
   $$

   

   > 1. C ist ein Körper!
   >
   > 2. Elemente aus $\mathbb{C}$ können in $\mathbb{R}^{2}$ interpretiert werden!

2. Wiederholung projektiver Geraden über einem beliebigen Körper

   ![截屏2021-02-0915.44.33](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhnzc98nyj31420jswtm.jpg)

3. RP^1 and CP^1

   ![截屏2021-02-0915.51.55](https://tva1.sinaimg.cn/large/008eGmZEgy1gnho70ajfwj30x60hg49w.jpg)

   ![截屏2021-02-0915.57.02](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhocbyc9fj30ws0ekdoi.jpg)

   **Raum der Punkte:**
   $$
   \mathbb{C P}^{1}:=\frac{\mathbb{C}^{2}-\{\boldsymbol{0}\}}{\mathbb{C}-\{0\}}
   $$
   **Standard Einbettung:**
   $$
   \begin{aligned}
   \mathbb{C} & \rightarrow \mathbb{C} \mathbb{P}^{1} \\
   z & \mapsto\left[\left(\begin{array}{l}
   z \\
   1
   \end{array}\right)\right]
   \end{aligned}
   $$
   **Punkt im Unendlichen:**
   $$
   \infty=\left[\left(\begin{array}{l}
   1 \\
   0
   \end{array}\right)\right]
   $$
   **Zwei Interpretationen von CP^1:**

   - reell 2-dimensionales geometrisches Objekt
   - komplex eindimensionale Projektive Gerade

4. Unterschied von CP^1 und RP^2

   $\mathbb{C P}^{1}$: Ebene $\mathbb{R}^{2}$ plus ein Punkt im Unendlichen

   $\mathbb{R} \mathbb{P}^{2}$: Ebene $\mathbb{R}^{2}$ plus eine Gerade im Unendlichen

5. Projektive Transformationen im CP^1

   $\tau: \mathbb{C} \mathbb{P}^{1} \rightarrow \mathbb{C P}^{1}$
   $\tau:\left[\left(\begin{array}{l}x \\ y\end{array}\right)\right] \rightarrow\left[\left(\begin{array}{ll}a & b \\ c & d\end{array}\right)\left(\begin{array}{l}x \\ y\end{array}\right)\right]$

   <span style="color:gray">(Möbius Transformationen)</span>

   <span style="color:gray">(Sechs reelle Freiheitsgrade)</span>

   $z \mapsto \frac{a z+b}{c z+d}$ 	<span style="color:gray;font-size:13px">nicht-homogene Version</span>



<h3 id ="sec6.2">Geometrie komplexer Rechenoperationen</h3>

1. Polarkoordinaten

   ![截屏2021-02-0919.54.55](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhv7udcyaj30ea0e6ju9.jpg)

   Kartesische Darstellung:
   $$
   z=a+i b
   $$
   Polarkoordinaten:
   $$
   \begin{aligned}  \quad z &=a+i b \\ &=r(\cos (\varphi)+i \sin (\varphi))\\
   &=r e^{i \varphi}\end{aligned}
   $$

2. Komplexe Rechenoperationen geometrisch interpretiert

   - Addition <span style="color:gray;font-size:10px">Verschiebung</span>

   <img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gnhvyy8s6lj30b40aowg6.jpg" alt="截屏2021-02-0920.20.59" style="zoom:33%;" />
   $$
   \begin{aligned}
   z_{1} &=a_{1}+i b_{1} \\
   z_{2} &=a_{2}+i b_{2} \\
   z_{1}+z_{2} &=\left(a_{1}+a_{2}\right)+i\left(b_{1}+b_{2}\right)
   \end{aligned}
   $$

   - Multiplikation <span style="color:gray;font-size:10px">Drehstreckung</span>

     <img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gnhw2lgkmej30bk0aumz8.jpg" alt="截屏2021-02-0920.24.29" style="zoom:33%;" />
     $$
     \begin{aligned}
     z_{1} &=r_{1} e^{i \varphi_{1}} \\
     z_{2} &=r_{2} e^{i \varphi_{2}} \\
     z_{1} \cdot z_{2} &=r_{1} r_{2} e^{i\left(\varphi_{1}+\varphi_{2}\right)}
     \end{aligned}
     $$

   - Konjugation <span style="color:gray;font-size:10px">Spiegelung</span>
     
     <img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gnhw44ah5cj308e09o0tm.jpg" alt="截屏2021-02-0920.25.56" style="zoom:33%;" />
     $$
     \begin{array}{l}
     z=a+i b \\
     \bar{z}=a-i b
     \end{array}
     $$

3. Algebraisches Überprüfen geometrischer Eigenschaften

   ![截屏2021-02-0920.55.11](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhwyjoil6j30x40ggal7.jpg)

4. Satz vom Fasskreisbogen

   Wie kann man testen, ob vier Punkte auf einem Kreis liegen?

   <img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gnhx3xjlgxj30cq0cuady.jpg" alt="截屏2021-02-0921.00.20" style="zoom:33%;" />

5. Test auf Kozirkularität同圆度

   ![截屏2021-02-0921.09.36](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhxdk5jkgj30xa0fatk4.jpg)

   **==Satz==**: Vier Punkte $A, B, C, D$ in $\mathbb{C} \mathbb{P}^{1}$ sind kozirkular oder kollinear g.d.w $(A, B ; C, D) \in \mathbb{R}$

6. Kreise und Transformationen

   **==Satz==**:  $\mathrm{CP}^{1}$ Transformationen bilden  "Kreise und Geraden" in "Kreise und Geraden" ab.

   >  Beweis: $(A, B ; C, D) \in \mathbb{R}$ ist projektiv invariant

<h3 id ="sec6.3">Die Punkte I und J</h3>

![截屏2021-02-0921.30.53](https://tva1.sinaimg.cn/large/008eGmZEgy1gnhxzpjzjlj30wq0hgtmv.jpg)

Nächstes Ziel: Verknüpfung von $\mathbb{R} \mathbb{P}^{2}$ und $\mathbb{C} \mathbb{P}^{1}$
**Vorteile $\mathbb{R} \mathbb{P}^{2}$**：
$$
\text{Punkte, Geraden, Inzidenz, Kegelschnitte sind gut repräsentiert}
$$
**Vorteile** $\mathbb{C} \mathbb{P}^{1}$:
$$
\text { Kozirkularität gut repräsentiert }
$$
Ziel: Überlagerung der beiden Welten

<img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gnhyhr8e2lj30bk0gggon.jpg" alt="截屏2021-02-0921.48.15" style="zoom:50%;" />

将两个坐标系“合并”：

**Die Punkte I und J**
$$
I=\left(\begin{array}{c}
-i \\
1 \\
0
\end{array}\right)， \mathrm{J}=\left(\begin{array}{l}
i \\
1 \\
0
\end{array}\right)
$$

$$
P=\left(\begin{array}{c}
a_{1} \\
b_{1} \\
1
\end{array}\right) \quad Q=\left(\begin{array}{c}
a_{2} \\
b_{2} \\
1
\end{array}\right)
$$

$$
\begin{aligned}
\quad[P, Q, I]=\operatorname{det}\left(\begin{array}{ccc}
a_{1} & a_{2} & -i \\
b_{1} & b_{2} & 1 \\
1 & 1 & 0
\end{array}\right) &=a_{2}-i b_{1}-a_{1}+i b_{2} \\
&=-\left(a_{1}+i b_{1}\right)+\left(a_{2}+i b_{2}\right) \\
&=z_{Q}-z_{p} \\
&=\operatorname{det}\left(\begin{array}{cr}
z_{Q} & z_{P} \\
1 & 1
\end{array}\right)\\
&=-[\widetilde{P}, \widetilde{Q}]
\end{aligned}
$$

$$
\begin{aligned}
&\text { Analog: }\\
&[P, Q, J]=\cdots=-\overline{[\widetilde{P}, \widetilde{Q}]}
\end{aligned}
$$

<h3 id = "sec6.3">Kozirkularitaet testen</h3>

<img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gni3zwwtetj30es0i6tff.jpg" alt="截屏2021-02-1000.58.39" style="zoom:33%;" />
$$
\begin{aligned}
& \widetilde{A}, \widetilde{B}, \widetilde{C}, \widetilde{D} \text { kozirkular } \\
\Longleftrightarrow &(\widetilde{A}, \widetilde{B} ; \widetilde{C}, \widetilde{D}) \in \mathbb{R} \\
\Longleftrightarrow & \frac{[\widetilde{A}, \widetilde{C}][\widetilde{B}, \widetilde{D}]}{[\widetilde{A}, \widetilde{D}][\widetilde{B}, \widetilde{C}]} \in \mathbb{R}\\
\Longleftrightarrow & \frac{[\widetilde{A}, \widetilde{C}][\widetilde{B}, \widetilde{D}]}{[\widetilde{A}, \widetilde{D}][\widetilde{B}, \widetilde{C}]} = \frac{\overline{[\widetilde{A}, \widetilde{C}][\widetilde{B}, \widetilde{D}]}}{\overline{[\widetilde{A}, \widetilde{D}][\widetilde{B}, \widetilde{C}]}}\\
\Longleftrightarrow & \frac{[A, C, I][B, D, I]}{[A, D, I][B, C, I]}=\frac{[A, C, J][B, D, J]}{[A, D, J][B, C, J]}\\
\Longleftrightarrow &(A, B ; C, D)_{I}=(A, B ; C, D)_{J}
\end{aligned}
$$

> Kreise sind Kegelschnitte durch I und J

<h3 id = "sec6.5">Kreise und I und J</h3>



![截屏2021-02-1001.06.59](https://tva1.sinaimg.cn/large/008eGmZEgy1gni48krrutj313w0m0asu.jpg)

<img src="https://tva1.sinaimg.cn/large/008eGmZEgy1gni4971qwtj30mo0b8n2v.jpg" alt="截屏2021-02-1001.07.36" style="zoom: 50%;" />



<h1 style="color: green" id = "sec7">Euklidische Geometrie</h1>

<h3 id = "sec7.1">senkrecht stehen und Winkel</h3>

1. 

   <img src="https://i.loli.net/2021/02/10/qDhF5r4dEVlZ3Y1.png" alt="截屏2021-02-1010.31.47" style="zoom:33%;" />
   $$
   \begin{array}{l}
   A=\left(\begin{array}{c}
   A_{x} \\
   A_{y} \\
   1
   \end{array}\right) \\
   \widetilde{A}=\left(\begin{array}{c}
   A_{x}+i A_{y} \\
   1
   \end{array}\right)=\left(\begin{array}{c}
   z_{A} \\
   1
   \end{array}\right)
   \end{array}
   $$

   $$
   \begin{aligned}
   \textbf{senkrecht stehen: }\quad \frac{z_{A}-z_{B}}{z_{A}-z_{C}} \in i \mathbb{R} &\Longleftrightarrow \frac{z_{A}-z_{B}}{z_{A}-z_{C}}=-\overline{\left(\frac{z_{A}-z_{B}}{z_{A}-z_{C}}\right)}\\
   
   
   &\Longleftrightarrow \frac{[\widetilde{A}, \widetilde{B}]}{[\widetilde{A}, \widetilde{C}]}=-\frac{\overline{[\widetilde{A}, \widetilde{B}]}}{[\widetilde{A}, \widetilde{C}]} \\
   &\Longleftrightarrow=\frac{[A, B, I]}{[A, C, I]}=-\frac{[A, B, J]}{[A, C, J]} \\
   &\Longleftrightarrow \frac{[A, B, I][A, C, J]}{[A, C, I][A, B, J]}=-1 \\
   &\Longleftrightarrow(B, C ; I, J)_{A}=-1
   
   \end{aligned}
   $$
   
    <img src="https://i.loli.net/2021/02/10/5w9WrHeFktUXTRp.png" alt="截屏2021-02-1011.44.19" style="zoom:50%;" />
   $$
   l \perp m \Longleftrightarrow(L, M ; I, J)=-1
   $$
   **Spezialfall der Formel von Laguerre:**
   $$
   \angle(l, m)=\frac{1}{2 i} \ln ((L, M ; I, J))
   $$
   
2. Formel von Laguerre

   ![截屏2021-02-1012.30.36](https://i.loli.net/2021/02/10/sEpAjq4SzHMgWef.png)

3.  Eigenschaften von Winkeln

   ![截屏2021-02-1014.50.39](https://i.loli.net/2021/02/10/WeIHBX7kPD5OuYF.png)

4. Senkrecht stehen als Sonderfall
   $$
   \begin{aligned}{l}
   &\angle(l, m)=\frac{1}{2 i} \ln ((L, M ; I, J)) \\
   &\Longrightarrow \pi / 2=\frac{1}{2 i} \ln ((L, M ; I, J)) \\
   &\Longrightarrow i \pi=\ln ((L, M ; I, J)) \\
   &\Longrightarrow e^{i \pi}=(L, M ; I, J) \\
   &\Longrightarrow -1=(L, M ; I, J)
   \end{aligned}
   $$



<h3 id = "sec7.2">Elementargeometrie</h3>

> ==**Metasatz**==: Euklidische Geometrie ist Projektive Geometrie zusammen mit I und J.

1. Verknüpfung konjugierter Elemente

   ![截屏2021-02-1016.15.41](https://i.loli.net/2021/02/10/tw4NsraVgf7Tld5.png)

2. Komplexe Zahlen und RP^2

   

3. Spiegelung an einer Geraden

   ![截屏2021-02-1016.46.27](https://i.loli.net/2021/02/10/st6YFMkj4XvrScO.png)

4. Mittelpunkt eines Kreises mit Animation

   <img src="https://i.loli.net/2021/02/11/ZM8cKAnjfrUQe1h.png" alt="截屏2021-02-1018.16.17" style="zoom:50%;" />

5. Brennpunkten焦点 eines Kegelschnittes

   <img src="https://i.loli.net/2021/02/11/p9ua6tAeJflLsjO.png" alt="截屏2021-02-1020.16.20" style="zoom:50%;" />

   Konstruktion von Brennpunkte:

   ![截屏2021-02-1020.27.42](https://i.loli.net/2021/02/11/AC4HPTxebRQsSXr.png)

6. Satz von Pascal und sein Duales

   ![截屏2021-02-1020.45.19](https://i.loli.net/2021/02/11/DlyqMWv4PtGj8ON.png)



<h3 id = "sec7.3">Transformation</h3>

1. Wiederholung zur Winkelmessung

   ![截屏2021-02-1021.39.32](https://i.loli.net/2021/02/11/GC9tRuEKg1ixSl7.png)

2. Längen

   ![截屏2021-02-1022.29.03](https://i.loli.net/2021/02/11/moQ253HYRMfAuVC.png)



3. Messe

   ![截屏2021-02-1023.50.28](https://i.loli.net/2021/02/11/fBnR2cVMpGTtJwH.png)

4. Transformationen, unter denen Längen und Winkel erhalten bleiben (不变化)

   **==Satz:==** Transformationen die I und J als Paar festlassen, lassen Absolutbeträge von Winkeln und Längenverhältnissen invariant.

   ![截屏2021-02-1100.24.36](https://i.loli.net/2021/02/11/IHcneD6KEvjMmOL.png)

5. Was sind die Transformationen, die I und J festlassen?

   - Fall 1: $I \mapsto I$ und $J \mapsto J$.
     $$
     \begin{array}{l}
     \left(\begin{array}{lll}
     a & b & p \\
     c & d & q \\
     0 & 0 & r
     \end{array}\right) \cdot\left(\begin{array}{l}
     i \\
     1 \\
     0
     \end{array}\right)=\lambda\left(\begin{array}{l}
     i \\
     1 \\
     0
     \end{array}\right) \\
     i \cdot a+1 \cdot b=i \cdot \lambda \\
     i \cdot c+1 \cdot d=\lambda
     \end{array}
     $$

     $$
     \Longrightarrow a=d ; b=-c
     $$

   <img src="https://i.loli.net/2021/02/11/eNAmz8IwhUgKvpb.png" alt="截屏2021-02-1101.01.42" style="zoom:50%;" />

   - Fall 2: $I \mapsto J$ und $J \mapsto I$.

   <img src="https://i.loli.net/2021/02/13/Rhjo8z6OpUiDTsA.png" alt="截屏2021-02-1101.22.32" style="zoom:50%;" />

<h3 id ="sec7.4">Ausblick: Cayley-Klein Geometrien</h3>

1. Rückblick: Klassifikation von Kegelschnitten

   ![截屏2021-02-1102.47.43](https://i.loli.net/2021/02/11/OQdWjvc5pA1eFki.png)

   ![截屏2021-02-1102.50.54](https://i.loli.net/2021/02/11/ip8nLU6cZTo2xSf.png)

2. Die drei Fälle der Doppelgeraden

   ![截屏2021-02-1103.13.08](https://i.loli.net/2021/02/11/K4QzrEaqS7kceT3.png)

3. Kegelschnittklassifikation

   ![截屏2021-02-1103.22.38](/Users/taoxiang/Library/Application Support/typora-user-images/截屏2021-02-1103.22.38.png)

4. Allgemeine Maßbestimmung bzgl. eines nicht-degenrierten Kegelschnitts

   **Cayley-Klein Geometrien**

   ![截屏2021-02-1108.10.16](https://i.loli.net/2021/02/11/yTZ316FX5CMLsm2.png)

   

5. Drei Faelle der Messung

   ![截屏2021-02-1108.14.19](https://i.loli.net/2021/02/11/6ZYqCHUVcxRWbTB.png)

6. Transformationen von Cayley-Klein Geometrien

   ![截屏2021-02-1108.21.26](https://i.loli.net/2021/02/11/BX3TZxelrz6GA7Q.png)

7. Elementargeometrie in Cayley-Klein Geometrien

   ![截屏2021-02-1108.24.33](https://i.loli.net/2021/02/11/xSYIRd2pvseVFP9.png)

8. 















<span style="color:gray;font-size:10px"></span>

