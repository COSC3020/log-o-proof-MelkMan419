[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

To prove that $O(\log_{2} n)$ is equivalent to $O(\log_{5} n)$, we need to show that there exist constants $c_1$, $c_2$, and $n_0$ such that for all $n \geq n_0$, 

$$
\begin{align*}
\log_{2} n &\leq c_1 \cdot \log_{5} n \\
\text{or}\quad \log_{5} n &\leq c_2 \cdot \log_{2} n
\end{align*}
$$

We will prove both directions separately.

### First way: $O(\log_{2} n) \subseteq O(\log_{5} n)$

Let's prove that $\log_{2} n \leq c_1 \cdot \log_{5} n$.

Taking logarithms with base 5 on both sides:

$$
\log_{5} 2^{\log_{2} n} \leq \log_{5} n^{c_1}
$$

Using the logarithm power rule, we get:

$$
\frac{\log_{5} n}{\log_{5} 2} \leq c_1
$$

Since $\log_{5} 2 > 0$, let $c_1 = \frac{1}{\log_{5} 2}$.

Thus, we have shown that $\log_{2} n \in O(\log_{5} n)$.

### Second way: $O(\log_{5} n) \subseteq O(\log_{2} n)$

Let's prove that $\log_{5} n \leq c_2 \cdot \log_{2} n$.

Taking logarithms with base 2 on both sides:

$$
\log_{2} 5^{\log_{5} n} \leq \log_{2} n^{c_2}
$$

Using the logarithm power rule, we get:

$$
\frac{\log_{2} n}{\log_{2} 5} \leq c_2
$$

Since $\log_{2} 5 > 0$, let $c_2 = \log_{2} 5$.

Thus, we have shown that $\log_{5} n \in O(\log_{2} n)$.

Therefore, we have established that $O(\log_{2} n) = O(\log_{5} n)$.

