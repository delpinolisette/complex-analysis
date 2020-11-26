# Table of Contents
1. Fixed points (more info)
    - definition of index of fixed point
    - sum of indices of fixed points of $f$
2. Lemma: Existence of a special fractional linear map
3. Definition :Cross Ratio of Four Distinct Points
4. Proposition: Fractional Linear Maps Preserve Cross Ratio
5. Theorem: For any distinct point triples, there exists a unique fractional linear map sending them to each other. 

Summary: The goal for these notes was to show that for any triples of distinct points there exists a unique map such that these points get mapped to each other. So:

WTS: for any $(z_1, z_2, z_3)(w_1, w_2, w_3), \exists!f\in Aut(\overline C)$ s.t. $f(z_k) = w_k$, for $k=1,2,3$.

---

# More On Fixed Points
Let $f:\mathbb{\overline C} \to \mathbb{\overline C}$, where $\mathbb{\overline C}$ is the extended complex plane. Let $f(z_0) = z_0$ so that $z_0$ is a fixed point under the map $f$.

# Definition: Index of a Fixed Point $z_0$:

index of the fixed point $z_0$ of $f$ is defined by:

if $z_0 \neq \infty$ then $$ind_{z_0}f:= ord_{z_0}[f(z)-z]$$

if $z_0 = \infty$ then set $g(z) = \frac{1}{f(\frac{1}{z})} \to g(0)$ because $f(\infty) = \infty$ so that $$ind_{\infty}f = ind_{0}g$$

# Fact from Geometry, Sum of Indices:
recall that meromorphic functions (analytic when a finite number of singularities are removed) can be written as a ratio of two polynomials:

$$f(z) = \frac{P(z)}{Q(z)}$$ where $P,Q$ have no common roots. 
Then we set $$d = max\{deg P, deg Q\}$$
Then $$\sum_{f(z_0)=z_o, z_0 \in \mathbb{\overline C}} Ind_{z_0}f = 1+d$$

But in particular when $f$ is a fractional linear transformation, then $d = max\{deg P, deg Q\}=1$, so for FL:
$$\sum_{f(z_0)=z_o, z_0 \in \mathbb{\overline C}} Ind_{z_0}f = 2 = \chi(\overline C)$$ 
where $\chi$ is the [Euler Characteristic](https://en.wikipedia.org/wiki/Euler_characteristic) of the extended complex plane considered as the [Reimann Sphere](https://en.wikipedia.org/wiki/Riemann_sphere), which is then considered as tetrahedron. Very very very cool. 

noteL Should verify this fact if time allows. 

# Lemma: Existence of an Important and Unique Fractional Linear Map
$\exists!$ fractional linear map (so $f \in Aut(\overline C)$) sending distinct$z_1 \to \infty, z_2 \to 0, z_3 \to 1$ in $\mathbb{\overline C}$.

Proof: The proof is just explicitly providing the map. In general the transformation $T(z)$ is:

$$T(z) = \frac{(z-z_2)(z_3-z_1)}{(z-z_1)(z_3 - z_2)}$$

if $z_1 = \infty$ then 
$$T(z)=\frac{z-z_2}{z_3-z_2} $$

if $z_2 = \infty$ then 
$$T(z)=\frac{z_3-z_1}{z-z_1} $$

if $z_3 = \infty$ then 
$$T(z)=\frac{z-z_2}{z-z_1} $$

This map $T$ is the map we wanted. 

### Definition: Cross Ratio:
The `cross ratio` of four distinct points $z_1,z_2,z_3,z_4$ is written $(z_1,z_2,z_3,z_4)$. 

It is defined as $T(z_4)$ where T is the transformation shown in the Lemma's proof. 

$$(z_1,z_2,z_3,z_4) := \frac{(z_4-z_2)(z_3-z_1)}{(z_4-z_1)(z_3 - z_2)}$$

# Proposition: Fractional Linear Maps Preserve the Cross Ratio:
Fractional Linear maps preserve the cross ratio.

Proof:
1. Let S be a fractional linear map. $S \in Aut(\overline C)$. WTS that the cross ratio of $z_1,z_2,z_3,z_4$  is equal to the cross ratio of $Sz_1,Sz_2,Sz_3,Sz_4$.
2. Let T be the fractional linear map sending : $$z_1 \to \infty$$ $$z_2 \to 0$$ $$z_3 \to 1$$
3. Then the composition $T \circ S^{-1}$ maps: $$S(z_1) \to \infty$$ $$S(z_2) \to 0$$ $$S(z_3) \to 1$$ $$S(z_4) \to (Sz_1, Sz_2, Sz_3, Sz_4)$$
4. Then we get that: $$(T \circ S^{-1})(Sz_4) = T(x_4) = (z_1, z_2, z_3, z_4)$$
5. Thus, $(z_1, z_2, z_3, z_4)$ is mapped to $(Sz_1, Sz_2, Sz_3, Sz_4)$ under an FL map. This is what we wanted show. 

# Theorem: Triples Map To Each Other Under Unique F.L Map:
This is the crowning jewel of these notes. This is what all the preliminary material was for: 


For any two triples of distinct points $z_1, z_2, z_3$ and $w_1, w_2, w_3$, $\exists! f \in Aut(\mathbb{\overline C})$ s.t. $f(z_k) = w_k$, for $k=1,2,3$

Proof: 

Part 1: Existence

We have shown that there exists a unique map T sending: $$z_1 \to \infty, z_2 \to 0, z_3 \to 1$$ and a map S sending: $$w_1 \to \infty, w_2 \to 0,w_3 \to 1$$ such that $S^{-1} \circ T(z_k) = w_k$

Part 2: Uniqueness

For the uniqueness part, we use the cross ratio. Set $w = f(z)$ and then $(z_1,z_2,z_3,z_4) = (w_1,w_2,w_3,w_4)$, which implies that $$\frac{w-w_2}{w-w_1}\cdot \frac{w_3 - w_1}{w_3 - w_2} = \frac{z-z_2}{z-z_1} \cdot \frac{z_3 - z_1}{z_3 - z_2}$$

Solving for $w$ in terms of $z$, we get the formula for $f(z)$


# Application
We can use the equation outlined in the existence part of the proof of the above theorem to write down an explicit map sending $(z_1,z_2,z_3)$ to $(w_1,w_2,w_3)$


--- 
# TODO on these notes:
1. add formal definition of order as I work
2. get explicit example of unique frac liner map