We want to show that $O(\log_{2} n)$ and $O(\log_{5} n)$ are equivalent. For any positive function $T(n)$, we need to prove the following:

1. If $T(n) \in O(\log_{2} n)$, then $T(n) \in O(\log_{5} n)$.
2. If $T(n) \in O(\log_{5} n)$, then $T(n) \in O(\log_{2} n)$.

### Direction 1: $O(\log_{2} n) \subseteq O(\log_{5} n)$

Assume $T(n) \in O(\log_{2} n)$. By definition, there exist constants $c_1$ and $n_1$ such that for all $n \geq n_1$,

$$
T(n) \leq c_1 \cdot \log_{2} n.
$$

We want to show that $T(n) \in O(\log_{5} n)$, i.e., there exist constants $c_2$ and $n_2$ such that for all $n \geq n_2$,

$$
T(n) \leq c_2 \cdot \log_{5} n.
$$

Taking the logarithm base 5 on both sides of the equation:

$$
\log_{5} T(n) \leq \log_{5} (c_1 \cdot \log_{2} n).
$$

Using the logarithmic properties:

$$
\log_{5} T(n) \leq \frac{\log_{2} n}{\log_{2} 5} + \log_{5} c_1.
$$

Let $c_2 = \frac{c_1}{\log_{2} 5}$ and $n_2 = n_1$. Then for all $n \geq n_2$, we have $T(n) \leq c_2 \cdot \log_{5} n$, thus showing that $T(n) \in O(\log_{5} n)$.

### Direction 2: $O(\log_{5} n) \subseteq O(\log_{2} n)$

Similarly, assume $T(n) \in O(\log_{5} n)$. By definition, there exist constants $c_3$ and $n_3$ such that for all $n \geq n_3$,

$$
T(n) \leq c_3 \cdot \log_{5} n.
$$

We want to show that $T(n) \in O(\log_{2} n)$, i.e., there exist constants $c_4$ and $n_4$ such that for all $n \geq n_4$,

$$
T(n) \leq c_4 \cdot \log_{2} n.
$$

Following a similar approach as in the first direction, we can choose $c_4 = c_3 \cdot \log_{2} 5$ and $n_4 = n_3$ to establish the desired inequality.

Therefore, we have shown that $O(\log_{2} n) = O(\log_{5} n)$ for any positive function $T(n)$.
