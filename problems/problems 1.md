 # Set 1
## Exploration
1. If the integers are defined with as the set of numbers with the properties listed, then those properties should encompass what integers are and therefore adequately describe them. I believe, though have not shown, that WOP can be proved using the order axioms. This is because WOP uses ideas that are introduced in the order axioms such as two numbers having an order to them.
2. 

#### First part
<b>Proof of (1b)</b>

Step | Reason
- | -
$let\;b⋆a=a$ | given
$(b⋆a)⋆a^{-1}=a⋆a^{-1}$ |(2a)
$b⋆(a⋆a^{-1})=a⋆a^{-1}$ |associativity
$b⋆0=0$|substitution
$b⋆0=b$|(1a)
$b=0$|transitivity

<b>Proof of (2b)</b>

Step|Reason
---|---
$let\;ab=0$<br>$let\;bc=0$|given
$\implies b*a*b=b$ | It simplifies to $b=b$
$b*a*b*c=b*c$ | $*$ operator
$b*a=0$ | substitution
$a*b=b*a$ | transitivity ( shows that $*$ is commutative )
$(2b)$ | commutativity.

#### Second part
Given (1b), and (2b), it is likely not possible to prove (1a) and (2a). This is because (1b) coveys relatively little information compared to (1a). Because of this, though (1b) is provable by (1a), (1b) is probably not provable from (1a). Assuming this is true, it is likely even harder to prove (2a) from (2b) and (1b) because if (1a) is not provable, most likely (2a), is also not.
## Numerical
3. $Z[i]$ does satisfy the ring axioms:
- $Z[i]$ satisfy the all the ring axioms. This can be suggested, though not rigorously proven. Integers are really complex numbers with a $0i$ term. Performing addition and multiplication on these complex numbers can be represented by operations on vectors in the complex plain. For example, addition corresponds to the simple adding of two vectors and multiplication is a stretching as well as a rotation. When there is a $0i$ coefficient, this operation can be more simply represented as manipulations on a 1D number line, but are in fact really in 2D space. Note that this same argument as to why they satisfy the ring axioms can also be extended to the quaternions and higher dimensional complex numbers.
- There are not other factors of $2+i$.
- Another non-trivial factor of $3+i$ is $(-2+i)(-1-i)$ 
- There are no non-trivial solutions for $4+i$.
- Another non-trivial factors of $5+i$ is $(-1+1i)(-2-3i)$
4. The solutions are the set of x values such that the parabola, $x^2+5x = 0\;(mod\;6)$. The only solutions to this are $0$, $1$, $3$, $4$. This can be found both through guess and check, as well as through first factoring the polynomial and then looking for the factors $2$, and $3$ within either factor. Similarly, the solutions to $h(x)=0\;(mod\;6)$ are the elements in $\mathbb{Z_6}$.

## PODASIP
5. For all $a$, $b$, $c$ $\in\mathbb{Z}$, if $a|b$, then $a|bc$

Step | Reason
--- | ---
$a \vert b$ | given
$let \; ap_1 = b$ | definition of
$ap_1c = bc$ | multiplication
$let \; p_2 = p_1c$ | definition
$ap_2 = bc$ | substitution
$a\vert bc$ | definition

6. If $k \vert a$ and $k \vert b$, then $k \vert (a+b)$

Step | Reason
--- | ---
$k\vert a$ <br> $k \vert b$ | given
$let\;kp_1 = a$ <br> $let\;kp_2 = b$ | definition 
$kp_1 + kp_2 = a+b$ | addition
$k(p_1 + p_2) = a+b$ | distribution
$let \; p_3 = p_1 + p_2$ | definition
$kp_3 = a+b$ | substitution
$k \vert (a+b)$ | definition

7. For all $a$, $b$, $c\in\mathbb{Z}$, if $a|b$ and $b|c$, then $a|c$.

Step | Reason
---|---
$a\vert b$ <br> $b\vert c$ | Given
$let\;ap_1 = b$ <br> $let\;bp_2 = c$ | Definition
$b(ap_1)=c$ | substitution
$let \; p_3 = ap_1$ | definition
$bp_3 = c$ | substitution
$b\vert c$ | definition

8. $a \cdot 0 = 0$  for every $a$, $b \in \mathbb{Z}$

Step | Reason
--- |---
$a \cdot 1 = a$ | ring axiom
$a \cdot 1 - a = a - a$ | subtraction
$a( 1 - 1 ) = a-a$ | distribution
$a\cdot0 = 0$ | definition ( of additive inverse )

9. $(-a) \cdot (-b) = ab$ for every $a$, $b \in \mathbb{Z}$

<b>First prove: $-a = (-1)a$</b>

Step | Reason
---|---
$(1 + -1)a = 0 \cdot a = 0$ | Given
$a + (-1)a=0$ | distribution
$(-1)a = -a$ | subtraction

Now it is trivial:

Step | Reason
---|---
$(-a)(-b)$ | given
$= ((-1)a)((-1)b)$ | proved above
$= (-1)(-1)(ab)$ | distribution
$= ab$ | evaluation


10. For all $a$, $b \in \mathbb{Z}$, if $a|b$, then $b|a$

Step | Reason
--- | ---
$a\vert b$ | Given
$b\vert a$ | Assumed to be true
$ap_1 = b$ <br> $bp_2 = a$ | definition
$(bp_2)p_1 = b$ | substitution
$b(p_2p_1) = b$ | association
$b(p_2p_1)/b = b/b$ | division
$(b/b)(p_2p_1) = b/b$ | distribution
$1 \cdot (p_2p_1) = 1$ | definition ( of multiplicative inverse )
$p_2p_1 = 1$ | ring axiom
$p_1 = 1$ and $p_2 = 1$ | <u>proven below</u>
$a = b$ or $b = a$ | substitution

Therefore, the claim should read For all $a$, $b \in \mathbb{Z}$, if $a=b$, then $b|a$ and $a|b$.

<b>Proof that if $ab=1$, and $a$, $b\in \mathbb{Z}$, then $a=b=1$ </b>
<b>Case 1: $a=1$, $b \neq 1$</b>: 1 is the multiplicative identity therefore $ab=b$.
<b>Case 2: $a \neq1$, $b = 1$</b>: 1 is the multiplicative identity therefore $ab=a$.
<b>Case 3: $a \neq1$, $b\neq1$</b>: 
>$ab=1$
>$\implies a=\frac{1}{b}$
>$\frac{1}{b} \in \mathbb{Z}$ if and only if $b=1$
>$\therefore a=1$
>However, this contradict $a\ne 1$

<b>Case 4: </b>$a=1$, $b=1$: $ab=1$; $1 \cdot 1=1$; $1=1$

Because only case 4 works, and all cases have been considered, $a = b = 1$ is the only possible values for $a$ and $b$.
