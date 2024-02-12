### Direction 1: $O(\log_{2} n) \subseteq O(\log_{5} n)$

Assume $T(n) \in O(\log_{2} n)$. By definition, there exist constants $c_1$ and $n_1$ such that for all $n \geq n_1$,

$$
T(n) \leq c_1 \cdot \log_{2} n.
$$

We want to show that $T(n) \in O(\log_{5} n)$, i.e., there exist constants $c_2$ and $n_2$ such that for all $n \geq n_2$,

$$
T(n) \leq c_2 \cdot \log_{5} n.
$$

Taking the logarithm base 5 on both sides of the inequality, we get:

$$
\log_{5} T(n) \leq \log_{5} (c_1 \cdot \log_{2} n).
$$

Using the logarithmic properties, we have:

$$
\log_{5} T(n) \leq \frac{\log_{2} n}{\log_{2} 5} + \log_{5} c_1.
$$

Let $c_2 = \frac{c_1}{\log_{2} 5}$ and $n_2 = n_1$. Then for all $n \geq n_2$, we have $T(n) \leq c_2 \cdot \log_{5} n$, thus showing that $T(n) \in O(\log_{5} n)$.
