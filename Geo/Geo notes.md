#### Table of Contents

- [Die reelle projektive Ebene](#sec1)
  - [Punkte und Geraden im R^2](#sec1.1)

- projektive Transformationen
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

11. 

    

