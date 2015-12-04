# Chinese Reminder Theorem

N.P.Smart and F.Vercauteren gave an observation in this [paper](https://eprint.iacr.org/2011/133.pdf). With the application of the polynomial Chinese Reminder Theorem (CRT), the plain text space of the BGV's scheme can be  divided into smaller parts. We write the equation as
$$
\mathbb{Z}_t[x]/\Phi_m(x) \cong \mathbb{Z}_t[x]/F_1(x)\otimes \cdots \otimes \mathbb{Z}_t[x]/F_\ell(x).
$$
Here, the $$m$$-th cyclotomic polynomial $$\Phi_m(x)$$ is factorized into $$\ell$$ _irreducible_ polynomails $$F_j(x)~1 \le j \le \ell$$. That is
$$
    \Phi_m(X) = \prod_{j=1}^{\ell}F_j(x) \mod t.
$$
Presume all factors $$F_j(x)$$s have the same degree. There by $$\forall j~\textrm{deg}(F_j(x)) = \phi(m)/\ell$$/
[SIMD]: https://eprint.iacr.org/2011/133.pdf