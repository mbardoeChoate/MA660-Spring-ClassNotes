[comment]: render
# Day 2 Notes

### Class Goals

* Become more familiar with the Laplace Transform
* Understand how to use tables to compute L.T.
* Know that if two function have the same L.T. then they are basically equal
* Solve D.E. using L.T.
* Intuition about the Inverse Laplace Transform
* Initial Value Theorem for Laplace Transform
* Final Value Theorem for Laplace Transform


#### More with Laplace Transform

Remember that the Laplace Transform is given by:

$$\mathcal{L}(f)(s)=F(s)=\int_0^{\infty} f(t)e^{-st}dt$$

#### What kind of functions have a Laplace Transform

Not every function has a Laplace Transform. Only functions that allow the improper integral to converge will work for the 

**Definition** A function $f(t)$ is defined for $t \geq 0$ is said to be of **exponential order** if for some constant 
$a$ and some constant $M > 0$ the inequality

$$ |f(t)| \leq Me^{at}$$

If a function is of **exponential order** then the function has a Laplace Transform.

One of the nice things about a Laplace transform is that a function that comes from an integral is always continuous 
even if the function that is being integrated isn't continuous. So if $f(t)$ has discontinuity $F(s)$ will not.

#### Dictionary for Laplace Transforms

| Function $f(t)$  | Laplace Transform $F(s)$ | Comment           |
|------------------|--------------------------|-------------------|
| $C$              | $C/s$                    |                   |
| $t^n$            | $n!/s^{n+1}$             | $n$ is an integer |
| $e^{at}$         | $1/(s-a)$                | $s > a$           |
| $t^ne^{at}$      | $n!/(s-a)^{n+1}$         | $n$ is an integer |
| $\sin(bt)$       | $b/(s^2 + b^2)$          |                   | 
| $\cos(bt)$       | $s/(s^2 + b^2)$          |                   | 
| $e^{at}\sin(bt)$ | $b/((s-a)^2 + b^2)$      |                   |
| $e^{at}\cos(bt)$ | $(s-a)/((s-a)^2 + b^2)$  |                   |


#### Laplace Transform of the derivatives

$$ \mathcal{L}(f')(s)= sF(s)-f(0)$$

**Proof:** Use integration by parts.

$$ \mathcal{L}(f'')(s)= s\mathcal{L}(f')-f'(0) $$
$$ \mathcal{L}(f'')(s)= s(sF(s)-f(0))-f'(0) $$
$$ \mathcal{L}(f'')(s)= s^2F(s)-sf(0)-f'(0) $$

**Proof:** Use integration by parts.

#### Example

Solve the following differential equation using the Laplace Transform:

$$u''(t) + 4 u'(t) + 3 u(t) = 0$$ 
$$ u(0)=2 , u'(0)=4$$

#### First Shifting Theorem

$$ \mathcal{L}(e^{at}f(t))=F(s-a)$$


#### Inverse Laplace Transform

The main point here is that if $U_1(s)=U_2(s)$ then $u_1(t)=u_2(t)$ except for a finite number of points where $u_i$ has 
a jump discontinuity.


#### Intuition about the Inverse Laplace Transform

Most of the information about what functions are involved in the Laplace Transform comes from the denominator. If we have
a function in the $s$-domain then we should look at the factors of the denominator to determine what functions are involved.

#### Initial Value Theorem for Laplace Transform

If $\lim_{t \to 0^{+}}$ exists then $\lim_{t \to 0^{+}} f(t)=\lim_{s \to \infty} sF(s)$

#### Final Value Theorem for Laplace Transform

If every pole of $F(s)$ is of the form $a+bi$ with $a<0$ or if $F$ has a pole at $s=0$ then these poles are of 
multiplicity 1.
Then $\lim_{t \to \infty}$ exists and $\lim_{t \to \infty} f(t)=\lim_{s \to 0^+} sF(s)$


#### Practice

**Exercise 5.2.7:** Compute the Laplace transform of $e^{it}$, treating $i$ as a constant by 
taking $a = i$ in Table 5.1. Compare the result to the Laplace transform of $\cos(t)+i\sin(t)$. 
Try simplifying the difference. Do the rules of Table 5.1 seem to work for complex exponents?