# Primitive Adjacent Sums in Finite Fields

This repository contains **Primitive Adjacent Sums in Finite Fields**, by **Yvkai Zhao**. The paper proves the Hou–Sun conjecture on cyclic orderings of finite fields with primitive adjacent sums and establishes bounds on the number of distinct adjacent sums.

**[Read the paper (PDF)](main.pdf)**

## The Hou–Sun conjecture

The conjecture was proposed jointly by **Qing-Hu Hou and Zhi-Wei Sun**. It appears as **Conjecture 3.5(i)** in Sun's *Some new problems in additive combinatorics*, with the date **September 5, 2013**. [Original statement](https://arxiv.org/html/1309.1679v9)

Let $q=p^n>7$ be a prime power, and let $\mathbb F_q$ be the finite field with $q$ elements. A **primitive element** is a generator of the multiplicative group $\mathbb F_q^\times$, or equivalently a nonzero element of multiplicative order $q-1$.

**Conjecture.** The elements of $\mathbb F_q$ can be arranged in a circle, each appearing exactly once, so that the sum of every pair of adjacent elements is primitive, including the last and first elements.

More precisely, there exists a permutation

$$
A=(a_0,a_1,\ldots,a_{q-1})
$$

of $\mathbb F_q$ such that

$$
a_j+a_{j+1}\in\mathcal P_q
\qquad (0\le j<q),\qquad a_q=a_0,
$$

where $\mathcal P_q$ denotes the set of primitive elements.

Equivalently, the graph on $\mathbb F_q$ in which distinct vertices $x,y$ are joined whenever $x+y$ is primitive has a Hamiltonian cycle.

## Main results

The paper constructs such a cyclic ordering for **every prime power $q>7$**, proving the conjecture. It also bounds the size of the adjacent-sum set

$$
T(A)=\{a_j+a_{j+1}:0\le j<q\},\qquad a_q=a_0.
$$

Theorem 1.1 gives the following results:

| Field parameters | Number of distinct adjacent sums |
| --- | --- |
| Odd characteristic | At most $n+2$ |
| Characteristic two | Exactly $n$, which is optimal |
| $p\ge5$ and $n$ even | Exactly $n+1$ is achievable and optimal |
| $p=3$ and $3\mid n$ | Exactly $n+1$ is achievable and optimal |
| Prime fields $\mathbb F_p$ with $p>7$ | Exactly $3$ is achievable and optimal |

The optimality statements follow from lower bounds valid for every cyclic ordering: in odd characteristic, $\lvert T(A)\rvert\ge\max\{n+1,3\}$; in characteristic two, $\lvert T(A)\rvert\ge n$.

## Proof outline

- **Odd characteristic, $q\ne9$.** A three-term arithmetic progression of primitive elements and the affine spanning property of the primitive-element set provide the parameters for an affine map. Cyclic orderings with prescribed adjacent sums are first constructed in $\mathbb F_p^n$ and then transferred to $\mathbb F_q$. Refined constructions give the $n+1$ bound in the cases listed above.
- **The field of order nine.** An explicit cyclic ordering handles this case.
- **Characteristic two.** A primitive normal basis and a cyclic Gray code produce an ordering whose adjacent sums are exactly the $n$ primitive basis elements.

The paper also studies cyclic orderings with general prescribed adjacent-sum sets in vector spaces. Section 9 gives concrete construction algorithms.

## Files and reference

- [`main.pdf`](main.pdf): the full paper, including the proof, strengthened results, and construction algorithms.
- Z.-W. Sun, *Some new problems in additive combinatorics*, Nanjing University Journal of Mathematics Biquarterly **36** (2019), no. 2, 134–155, Conjecture 3.5(i). [arXiv:1309.1679v9](https://arxiv.org/abs/1309.1679v9)