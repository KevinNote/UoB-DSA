# Complexity/复杂度

<center>
<span>24/10/2021</span>
<a style="text-decoration:none; color: black;" href="https://github.com/KevinZonda">KevinZonda</a>
</center>

## Big-O notation

$$
f(n)=O(g(n))\Longleftrightarrow|f(n)|\leq|cg(n)| \\
\text{for positive constants } c, n_0 \text{ where } n \gt n_0.
$$

It is a ***UPPER BOUND***.

**Example:**
$$
2n = O(n)\Longleftrightarrow |2n|\leq|cn| \\
3n^2+n=O(n^2)\Longleftrightarrow |3n^2+n|\leq|cn^2|
$$
Big O is a notation not a function, thus O(f(n)) is not a function.

**Example:**
$3n^2+4=O(n^2)$ is just a shorthand way pf writing $|3n^2+4|\leq|cn^2)|$
for some constant C.

$O(n^2)=3n^2+4$ has no meaning.



Big O notation can be made mathematically precise by defining it to be the **class** of functions with complexity `O(f (n))`. Therefore we can say that the complexity of an algorithm is **"in"** O(f (n)) or, shortening it, simply say that, for an algorithm X, we have that $X \in O(f(n))$.



大 O 符号为上界其存在逻辑为
$$
\forall n \geq n_0, 0 \leq f(n) \leq cg(n)
$$

## Other Measure Ways

- **Big O**: $f(n)=O(g(n))$: g is an upper bound on how fast $f$ grows as $n$ increases.
- **Little o**: $f(n)=o(g(n))$: A stricter upper bound than Big O.
- **Theta**: $f(n)=\Theta(g(n))$: More precise than Big O and Little o, it provides both upper and lower bounds, which are given by the same function, except with different constant factors.  
That is, $f$ and $g$ grow at the same rate.
- **Asymptotically Equal**: $f(n)∼g(n)$: stricter upper and lower bounds
- **Omega**: $f(n)=\Omega (g(n))$: an absolute lower bound (the negation of little o) 

### Little o

$$
f(n)=o(g(n))\Longleftrightarrow \lim_{n\rightarrow\infty}{\cfrac{f(n)}{g(n)}} \ \text{exists and is equal to 0.}
$$

**Example:**
$$
2n^2=O(n^3) \ \text{and} \ 2n^2=O(n^2)
$$

$$
2n^2 =o(n^3)\\
\because\lim_{n\rightarrow\infty}{\cfrac{2n^2}{n^3}}=\lim_{n\rightarrow\infty}{\cfrac{2}{n}}=0\\
\text{Not} \  2n^2=o(n^2)\\
\because\lim_{n\rightarrow\infty}{\cfrac{2n^2}{n^2}}=\lim_{n\rightarrow\infty}{2}=2\ne0\\
\text{Not} \ n^2=o(n^2)\\
\because\lim_{n\rightarrow\infty}{\cfrac{n^2}{n^2}}=\lim_{n\rightarrow\infty}{1}=1\ne0\\
$$

### Theta

$$
f(n)=\Theta(g(n))\Longleftrightarrow c_ig(n) \leq f(n)\leq c_2g(n)\\
\text{positive constants}\ c_1, c_2, n_0 \text{ and } n \gt n_o
$$

也就是说，我们可以找到两个正数 $c_1, c_2$ 把 $f(n)$ 夹在 $c_1g(n)$ 与 $c_2g(n)$ 中间。

### Asymptotically Equal/渐进相等

$$
f(n)\sim g(n) \Longleftrightarrow\lim_{n\rightarrow\infty}{\cfrac{f(n)}{g(n)}} \ \text{exists and is equal to 1.}
$$

也就是说，其在 $n\rightarrow\infty$ 情况下，原函数与渐进函数的比值为 1 。

### Omega

$$
f(n)=\Omega(g(n)) \Longleftrightarrow |f(n)| \geq |cg(n)| \\
\text{for positive constants } c, n_0 \text{ where } n \gt n_0.
$$

It is a ***LOWER BOUND***.

### Little omega

$$
f(n)=\omega(g(n))\Longleftrightarrow \lim_{n\rightarrow\infty}{\cfrac{g(n)}{f(n)}} \ \text{exists and is equal to 0.}
$$

## Different Kinds of Complexities

- **Average Case complexity**  
= average complexity over all possible inputs/situations  
(we need to know the likelihood of each of the input!) 
- **Worst Case complexity**  
= the worst complexity over all possible inputs/situations
- **Best Case complexity**  
= the best complexity over all possible inputs/situations 
- **Amortized complexity**  
= average time taken over a sequence of consecutive operations 

### Amortized Complexity

Chinese: 均摊复杂度

## References

1. "复杂度 - OI Wiki" - <https://oi-wiki.org/basic/complexity/>
