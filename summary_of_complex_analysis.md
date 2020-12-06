# Reference / Summary Sheet for Complex Analysis

I've attempted to list everything I learned in an upper division course on Complex Analysis here for quick reference:


# Complex Identities for a $z = x+iy$

$$ cos(z) = \frac{e^{iz}+e^{-iz}}{2}$$

$$sin(z) = \frac{e^{i}-e^{-iz}}{2i}$$

and for $x \in R$:

$$sinh(x) = \frac{e^x + e^{-x}}{2}$$

$$cosh(x)= \frac{e^x = e^{-x}}{2}$$

$$cosh^2(x) - sinh^2(x) = 1$$

so we can derive the complex hyperbolic functions:

$$sinh(z) = sinh(x)cos(y) + i cosh(x)sin(y)$$

$$cosh(z) = TODO$$

$$tanh(z) = TODO$$

[more identities of hyperbolic trig functions](https://en.wikipedia.org/wiki/Hyperbolic_functions#Sums_of_arguments)


# List of Important Theorems and Definitions

still in progress, unordered, expanded on below. 

- Rouche's Theorem
- Fundamental Theorem of Algebra
- Type I/II Integrals
- singularities
- zeroes
- residues
- Residue Theorem
- $ord_w{f(z)}$
- meromorphic function
- extended complex plane
- linear fractional
- Cauchy's Residue Theorem
- winding numbers
- Laurent Series
- poles
- order of a pole
- non-isolated singularity
- isolated singularity
- simply connected topological space
- path connected topological space
- hessian matrix and critical points
- Homotopy
- analytic branch of complex log
- principal branch of complex log
- ended hw 5 continue after this


---

# Singular Points

- a singularity of f(z) is a point where it fails to be analytic. You can classify them:

### Non-Isolated Singularities

1. Branch points: functions are not analytic here, so not analytic in a deleted neighborhood of a branch point
    - ex 1: $f(z) = \sqrt{z-3}$ has a branch point at $z = 3$
    - ex 2: $f(z) = ln(z^2 + z - 2)=0$ has branch pts where $f(z) = 0$
2. 

### Isolated Singularities

- a point $z_0$ is an isolated singularity if you can find a deleted delta neighborhood around it with no other singularity. If you can't find a deleted neighborhood s.t. f is analytic around $z_0$, it is an essential / non isolated singularity

1. TYPE 1: **poles/non-essential singularities**: a type of non-essential, isolated singularity. classify its order by : $\lim_{z \to z_0}(z-z_0)^nf(z) \neq 0$ but $\lim_{z \to z_0}(z-z_0)^{n+1}f(z) \neq 0$ then $f$ has a zero of order $n$ at the pole $z_0$. The limit of $f(z)$ at a pole is $\infty$. 
   - pole classification techniques:
    -  if $f(z)$ rational function:
    factor the denominator (here poles are where f is dividing by zero), assured all zeroes of the denominator exist in the complex plane by FTA, if you find simple roots (distinct and constant), poles (the zeroes) have order 1. 
        - ex: $\frac{1}{z^4+16}$
    - factor the denominator. if you ses a double factor, probably a pole of order 2 (double pole)
        - ex: $\frac{1}{x^2 + 4x + 4}$
    - check your order guesses with limit definition
    - use quadratic equation when you can't easily factor (valid for complex numbers): $z =\frac{-b \pm \sqrt{b^2 - 4ac}}{2}$
        - ex: $\frac{1}{z^2 - z + 1}$


2. TYPE 2: **Removable Singularities**: isolated / non essential singularity $z_0$ is removable if $\lim_{z \to z_0}$ exists and is not $\infty$. By this fact, $f$ remains continuous and analytic at $z_0$

3. TYPE 3: **Essential Singularities** Any singular point that is not a pole or a removable singularity is an essential singularity. The limits of the function at essential singularities truly do not exist. (they're not $\infty$). Also, we cannot find an $n$ s.t. $\lim_{z \to z_0}(z-z_0)^nf(z) \neq 0$
     - ex: $f(z) = e^{\frac{1}{z-2}}$ has an essential singularity at $z =2$. 

# Laurent Series Expansion
