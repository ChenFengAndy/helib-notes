# Chinese Reminder Theorem

N.P.Smart and F.Vercauteren gave an observation in this [paper](https://eprint.iacr.org/2011/133.pdf). With the application of the polynomial Chinese Reminder Theorem (CRT), the plain text space of the BGV's scheme can be  divided into smaller parts. We write the equation as
$$
\mathbb{Z}_t[x]/\Phi_m(x) \cong \mathbb{Z}_t[x]/F_1(x)\otimes \cdots \otimes \mathbb{Z}_t[x]/F_\ell(x).
$$
Here, the $$m$$-th cyclotomic polynomial $$\Phi_m(x)$$ is factorized into $$\ell$$ _irreducible_ polynomails $$F_j(x)~1 \le j \le \ell$$. That is
$$
    \Phi_m(X) = \prod_{j=1}^{\ell}F_j(x) \mod t.
$$
Presume all factors $$F_j(x)$$s have the same degree. Thereby, for all $$1 \le j \le \ell$$, the degree of each factor is $$d: = \textrm{deg}(F_j(x)) = \phi(m)/\ell$$. We, thus, can further rewrite the equation above as follow
$$
\mathbb{Z}_t[x]/\Phi_m(x) \cong \mathbb{Z}_{t^d}\otimes \cdots \otimes \mathbb{Z}_{t^d}.
$$
In other words, for each element $$a \in \mathbb{Z}_t[x]/\Phi_m(x)$$, we can uniquely identify $$\ell$$ elements from $$\mathbb{Z}_{t^d}$$ (Or from $$\ell$$ smaller spaces $$\mathbb{Z}_t[x]/F_j(x)$$).

Let's see an example: $$m = 8$$ and $$t = 17$$. The plain text space then becomes $$\mathbb{Z}_{17}[x]/(x^4 + 1)$$. In short, this space is the set of polynomials that with degree less than $$4$$ and coefficients in modulo $$17$$.


[SIMD]: https://eprint.iacr.org/2011/133.pdf