[comment]: render

# Day 3 Notes MA660
## More Shifting and Heaviside Function

### Practice 1

Solve the following problem using L.T.

$u'' +2u'+2u=t$ when $u(0)=1$ and $u'(0)=-1$

Final Answer: 
$u(t) = 1/2 (t + 3 e^(-t)\cos(t) - 1)$

### Introduction to the Heaviside Function

Let's look at a problem with a discontinuity.

Students solve: 

Find the Laplace Transform of:

$$f(t) = \left\{ \begin{matrix}
    t & 0< t < 5 \\
    t+10 & t \geq 5 \\
    \end{matrix} \right.\ $$

The answer to this $F(s)=\frac{1}{s^2} + \frac{10e^{-5s}}{s}$

Define the Heaviside function

$$H(t)=\left\{ \begin{matrix}
    0 &  t < 0 \\
    1 &  t \geq 0 \\
    \end{matrix} \right.\ $$

Then find the Laplace Transform for $H(t)$.

Then find the Laplace Transform for $H(t-c)$.



#### Second shifting Lemma

$$\mathcal{L}(H(t-c)f(t-c))=e^{-cs}\cdot F(s)$$



