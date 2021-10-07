# Analysis and Topology

## Lecture 1 (Thu Oct 7)

Recall from IA Analysis that if we had a sequence $(x_n)$, we say $x_n \to x$ as $n \to \infty$ if

$$\forall \varepsilon > 0, \exist N, \forall n \ge N, |x_n - x| < \varepsilon$$

In the above, we take the sequence to be in $\R$ or $\mathbb C$. However, in many different applications, it makes sense for us to consider the convergence of functions instead. However, it is not immediately clear how we could formalise convergence of functions. Let's look at two related, but different notions of convergence.

In what follows, we have the codomain of the functions being $\R$, but this could equally be $\mathbb C$.

### Pointwise convergence

Let $S$ be a set, $f_n : S \to \R$ be a sequence of functions, and $f : S \to \R$ be a function. Then we say $f_n \to f$ pointwise on $S$, if

$$\forall x \in S, \forall \varepsilon > 0, \exists N, \forall n \ge N, |f_n(x) - f(x)| < \varepsilon$$

Intuitively, we have that given $x \in S$, $f_n(x)$ describes a sequence in $\R$, and we can consider the limit of this sequence.

### Uniform convergence

Let $S$, $f_n$, $f$ be as above. We say that $f_n \to f$ uniformly on $S$ if

$$\forall \varepsilon > 0, \exists N, \forall x \in S, \forall n \ge N, |f_n(x) - f(x)| < \varepsilon$$

The intuition for this is that we can instead consider what happens if we perturb the function by a small amount $\varepsilon$, and we want $f_n$ to be within $\varepsilon$ of $f$ for $n$ sufficiently large.

The difference between the two is subtle, and was not initially appreciated by mathematicians. In this course, we will see that uniform convergence is a lot better behaved, and is what we will study. In particular, we are interested in what properties of the functions will transfer over to the limits.

The first thing we note is that uniform convergence implies pointwise convergence, so anything we prove for pointwise convergence must be true for uniform convergence as well. Let's now look at a property of uniform convergence which is not true for pointwise convergence.

> **Theorem**: Let $S \subseteq \R$, $f_n$, $f$ be as above, and say $f_n \to f$ uniformly on $S$. Suppose further that $f_n$ is continuous for all $n$. Then $f$ is continuous.

> **Proof**: For $n$ large enough, we have that $f(x) \approx f_n(x) \approx f_n(y) \approx f(y)$ for $x \approx y$.

Now let's consider a counterexample to this for pointwise convergence. Let $f_n(x) = x^n$, $S = [0, 1]$. Then $f_n \to f$ pointwise on $S$, where

$$f(x) = \begin{cases} 0 & x < 1 \\ 1 & x = 1\end{cases}$$

but $f$ here is clearly not continuous.
