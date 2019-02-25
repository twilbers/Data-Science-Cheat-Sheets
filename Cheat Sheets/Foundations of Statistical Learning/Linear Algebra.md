# Linear Algebra

### Vector operations


[comment]: <> (##### Properties of vector operators)
[comment]: <> (Communitivity: $\mathbf{r}+\mathbf{s}=\mathbf{s}+\mathbf{r}$)
[comment]: <> ($2\mathbf{r} = \mathbf{r} + \mathbf{r}$)

#### Magnitude
$\Vert\textbf{r}\Vert = \overset{n}{\underset{i}{\sum}}\sqrt{{r^{2}_{i}}}$
$\Vert\textbf{r}\Vert^{2} = \underset{i}{\sum}{r^{2}_{i}}$

##### Example:
$\mathbf{a} = \begin{bmatrix}{3}\\{4}\end{bmatrix}$
$\Vert\mathbf{a}\Vert = \sqrt{3^{2}+4^{2}} = \sqrt{9+16} = \sqrt{25} = 5$
$\Vert\mathbf{a}\Vert^{2} = {3^{2}+4^{2}} = {9+16} = {25}$


#### Dot product
##### Algrbraic definition
$\mathbf{r}\cdot\mathbf{s} = \underset{i}{\sum}{r_{i}s_{i}}$

$\mathbf{r}\cdot\mathbf{r} = \Vert\mathbf{r}\Vert^{2} = \underset{i}{\sum}{r^{2}_{i}}$

##### Geometric Definition
$\mathbf{r}\cdot\mathbf{s}= \Vert\mathbf{r}\Vert\Vert\mathbf{s}\Vert \cos{\theta}$,

where $\theta$ is the angle between $\mathbf{r}$ and $\mathbf{s}.$
when $\mathbf{r}\cdot\mathbf{s}=0$ $\mathbf{r}$ and $\mathbf{s}$ are orthoganal because $\cos({90\degree}) = 0$

##### Properties of dot product
Communitivity:$\hspace{.5cm}$ $r \cdot s = s \cdot r$
Distributive over addition: $\hspace{.5cm}$ $r \cdot (s + t) = r \cdot s + r \cdot t$
Associative over multiplication: $\hspace{.5cm}$ $r \cdot (as) = a(r \cdot s)$

#### Scalar Projection

##### Geometric definition


$a_{b} = \Vert\mathbf{a}\Vert\cos{\theta}$

If $0\degree ≤ \theta ≤ 90\degree$, as in this case, the scalar projection of $\mathbf{a}$ on $\mathbf{b}$ coincides with the length of the vector projection.


![scalar projection](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Dot_Product.svg/300px-Dot_Product.svg.png)

When $\theta$ is not known,

$\dfrac{\mathbf{a}\cdot\mathbf{b}}{\Vert\mathbf{a}\Vert\Vert\mathbf{b}\Vert} = \cos{\theta}$

##### Algebraic  definition
$a_{b} = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\Vert\mathbf{b}\Vert}$ and $b_{a} = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\Vert\mathbf{a}\Vert}$

$a_{b} =\mathbf{a} \cdot \mathbf{\hat{b}}$,
where $\hat{\mathbf{b}}$ is the unit vector in the direction of $\mathbf{b}$

$\mathbf{\hat{b}} = \dfrac{\mathbf{b}}{\Vert\mathbf{b}\Vert}$


#### Vector Projection

Vector projection of $\mathbf{a}$ on $\mathbf{b}$:
$a_{b} = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\Vert\mathbf{b}\Vert^{2}}\mathbf{b}$



#### Linear independence
