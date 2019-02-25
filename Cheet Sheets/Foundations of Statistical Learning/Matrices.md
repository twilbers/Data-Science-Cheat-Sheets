# Matrices
#### Matrix multiplication

$$
\left(\begin{array}{cc}
a & b\\
c & d
\end{array}\right)

\left(\begin{array}{c}
e\\
f
\end{array}\right) =

\left(\begin{array}{c}
ae + bf\\
ce + df
\end{array}\right)
$$

 $({n×m})({m×p})=({n×p})$, 	

where ($\alpha$×$\beta$) denotes a matrix with $\alpha$ rows and $\beta$ columns. Writing out the product explicitly,

$$\left[\begin{array}{cccc}
c_{11} & c_{12} & \cdots & c_{1p}\\
c_{21} & c_{22} & \ldots & c_{2p}\\
\vdots & \vdots & \ddots & \vdots\\
c_{n1} & c_{n2} & c_{n3} & c_{np}
\end{array}\right]=$$

$$\left[\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1m}\\
a_{21} & c_{22} & \ldots & a_{2m}\\
\vdots & \vdots & \ddots & \vdots\\
a_{n1} & a_{n2} & a_{n3} & a_{nm}
\end{array}\right]\left[\begin{array}{cccc}
b_{11} & b_{12} & \cdots & b_{1p}\\
b_{21} & b_{22} & \ldots & b_{2p}\\
\vdots & \vdots & \ddots & \vdots\\
b_{m1} & b_{m2} & b_{m3} & b_{mp}
\end{array}\right]$$


where
$c_{ij}= \overset{m}{\underset{k=1}{\sum}}{a_{ik}b_{kj}}$

#### Identity

$I_1 =[1], I_2 = \left[\begin{array}{cc}1&0\\0&1\end{array}\right], I_3 = \left[\begin{array}{ccc}1&0&0\\0&1&0\\0&0&1\end{array}\right], I_n = \left[\begin{array}{ccccc}1&0&0&\ldots&0\\0&1&0&\ldots&0\\0&0&1&\ldots&0\\\vdots&\vdots&\vdots&\ddots&\vdots\\0&0&0&\dots&1\end{array}\right]$ 

$A\mathbf{r} = \mathbf{r}^{\prime}$

##### Inverse

The inverse of a square matrix A is such that
$\mathbf{A}\mathbf{A}^{-1}=\mathbf{I}$

$$
\left(\begin{array}{cc}
a & b\\
c & d
\end{array}\right)^{-1}
 =
\dfrac{1}{ad-bc}
\left(\begin{array}{cc}
d & -b\\
-c & a
\end{array}\right)
$$

##### Determinate

$$
\vert{A}\vert=\begin{array}{|cc|}
a & b\\
c & d
\end{array} = ad -bc
$$

##### Matrix transformations


#### Gaussian elimination

##### Finding inverse w/ GE

##### Gram-Schmidt Process


&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
