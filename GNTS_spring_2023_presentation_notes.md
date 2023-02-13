---
cssclass: clean-embeds
aliases: []
tags: [_meta/notes, _meta/self_written]
---
# GNTS Spring 2023 Presentation Notes

---

- Written by: [Hyun Jong Kim](https://sites.google.com/wisc.edu/hyunjongkim?pli=1)
- Created: 2/11/2023
- Last updated: 2/13/2023

These are notes for my [[_index_GNTS_fall_2022|fall 2022 GNTS presentation notes]] on Tuesday, 2/14/2023.

I would greatly appreciate comments and corrections to these notes; please send such suggestions to me at `hyunjong<dot>kim<at>math<dot>wisc<dot>edu` or to my latest email address.

---

> [!Disclaimer]
> You might find it useful to use [Obsidian.md](https://obsidian.md/) if you are reading this as a Markdown file so that you can use the internal links in these notes. However, I may or may not make other notes that this note links to publicly available, so such links may be useless to you. Nevertheless, reading this as a Markdown file on Obsidian.md (alongside as a pdf file) could supplement your reading experience.

---

> [!Title]
> Bounded Height Problem for Dynamically Defined Sets

 >[!Abstract]
 > I will give a survey talk about one of the projects that Laura DeMarco has proposed for the upcoming Arizona Winter School in March. Namely, the problem aims to show that the set of orbit collisions via families of self maps of $\mathbb{P}^1$ defined over $\overline{\mathbb{Q}}$ has bounded height.

---

References:
- [[demarco_laura|Laura DeMarco]], *Arithmetic Dynamics and Intersection Problems*, Course and project outline for Arizona Winter School 2023.  ^demarcoaws2023outline
	- Available at https://swc-math.github.io/aws/2023/index.html

![[_reference_demarco_aws_2023_draft_2023_02_03]]  ^demarcoaws2023draft

![[_reference_demarco_kawa_2015]] ^demarcokawa2015

- [[demarco_laura|Laura DeMarco]], private communications, 2023.  ^demarcoprivatecomm

![[_reference_demarco_et_al_bhfds]] ^demarcoetalbhfds

![[_reference_silverman_ads]] ^silvermanads

---

# Outline
- Basic Definitions from Dynamics
	- Dynamical system, forward orbit, periodic point, preperiodic point
 - Unlikely intersections
	 - The question of unlikely intersections takes space $M$, a subset $Z \subset M$ of "special" points and asks the following: if a curve $C \subset M$ passes through infinitely many points of $Z$, then what is special about $C$?
- Question of bounded height in a dynamically defined curve
	- ![[#^672a02]]
- Relationship between unlikely intersection and bounded height problems
	- Sets of bounded height are considered "sparse" and intersections of sparse sets should be very rare.
- Questions that [[#^demarcoetalbhfds|DeMarco et al]] address.


# Basic Definitions from Dynamics[^1]

[^1]: See [[#^silvermanads|Silverman]], Chapter 0, for more details.


> [!Definition]
> A **(discrete) dynamical system** consists of a set $S$ and a function $\phi: S \rightarrow S$ mapping the set $S$ to itself. This self-mapping permits iteration
>
> **$$  \phi^n=\underbrace{\phi \circ \phi \circ \cdots \circ \phi}_{n \text { times }}=n^{\text {th }} \text { iterate of } \phi .  $$**
> 
> (By convention, $\phi^0$ denotes the identity map on $S$.)

> [!Definition]
> Let $S$ be a dynamical system.
> For a given point $\alpha \in S$, the **(forward) orbit of $\alpha$** is the set
> 
> **$$  \mathcal{O}_\phi(\alpha)=\mathcal{O}(\alpha)=\left\{\phi^n(\alpha): n \geq 0\right\}  $$**

^044f9f

> [!Definition]
> Let $S$ be a dynamical system.
> The point $\alpha$ is **periodic** if $\phi^n(\alpha)=\alpha$ for some $n \geq 1$. The smallest such $n$ is called the **exact period of $\alpha$**. The point $\alpha$ is **preperiodic** if some iterate $\phi^m(\alpha)$ is periodic.

> [!Remark]
> Note that a point $\alpha$ of a dynamical system $S$ is preperiodic if and only if there exist $n \geq 1$ and $m \geq 0$ such that $\phi^{m+n}(\alpha) = \phi^m(\alpha)$.

We will mostly discuss dynamical systems $f: \mathbb{P}^1 \to \mathbb{P}^1$.

# General question of unlikely intersections[^2]

[^2]: See [[#^demarcokawa2015|DeMarco, Kawa 2015...]], Section 4 for more details. [Qiao He](https://people.math.wisc.edu/~qhe36/) also gave a very nice talk giving an overview of unlikely intersections at the GNTS during the fall 2022 semester.

The general question of unlikely intersection in its vague, heuristic form is:

> [!General Question]
> Suppose $M$ is a complex algebraic variety, perhaps a moduli space of objects.  Suppose $Z \subset M$ is a subset of "special" points within $M$.  If a complex algebraic curve $C\subset M$ passes through infinitely many points of $Z$, then what is special about $C$?

An example is André's theorem; recall that the $j$-invariant of a complex elliptic curve uniquely determines its isomorphism class. Now let $M = \mathbb{C}^2$ parameterize pairs of (isomorphism classes of) elliptic curves $(E_1,E_2)$ by their $j$-invariants. Now let us consider a point $(E_1, E_2) \in M$ to be "special" if both $E_i$ have complex multiplication (CM), i.e. the endomorphism rings of the elliptic curves are both strictly larger than $\mathbb{Z}$. In other words, let 
$$Z = \{(E_1, E_2) \in M: E_1, E_2 \text{ are both CM elliptic curves} \}.$$

André's theorem states that a complex algebraic curve $C \subset M = \mathbb{C}^2$ has infinite intersection with $Z$ if and only if $C$ is 
1. a vertical line $\{E_0\}\times {\mathbb C}$ where $E_0$ has complex multiplication, 
2. a horizontal line ${\mathbb C}\times \{E_0\}$ where $E_0$ has complex multiplication, or 
3. the modular curve $Y_0(N)$, consisting of pairs $(E_1, E_2)$ for which there exists an isogeny $E_1 \to E_2$ of degree $N$, where $N$ is a positive integer.

Generalizations of André's theorem and related results led to the development of the André-Oort Conjecture.
> [!Conjecture]
> Let $X$ be a Shimura variety. Let $Y$ be a subvariety. Let $Z$ be the set of CM points.  The conjecture states that $Y \cap Z$ is dense in $Y$ if and only if $Y$ is "special" (More specifically, $Y$ is a sub-Shimura variety). 




# General question of bounded height in a dynamically defined curve[^3]

[^3]: See [[#^demarcoetalbhfds|DeMarco et al]] for more details. 

DeMarco proposed the following problem in the course and project outline for the 2023 Arizona Winter School:

>[!Problem]
>Fix two families of maps $f_t, g_t: \mathbb{P}^1 \to \mathbb{P}^1$, defined over $\overline{\mathbb{Q}}$, parameterized by $t$ in an algebraic curve $C$. Fix two maps $a,b: C \to \mathbb{P}^1$, also defined over $\overline{\mathbb{Q}}$. Is the set of orbit collisions
> $$\{t \in C(\overline{\mathbb{Q}}): \exists n,m \geq 0 \text{ such that } f^n_t(a(t)) = g^m_t(b(t)) \}$$
> of bounded height on $C$?

^672a02

Special cases are the central focus of the paper of [[#^demarcoetalbhfds|DeMarco et al]]. For instance, this paper proves 

>[!Theorem] Theorem, [DeMarco et al, Theorem 1.1], 
> Let $f_t(z)=g_t(z)=z^2+t$ and $a,b\in \overline{\mathbb{Q}}$ such that 
> exactly one of $a$ and $b$ is an algebraic integer. Then
> the set 
> **$$S:=\{t\in \overline{\mathbb{Q}}:\ \text{$f_t^m(a)=g_t^n(b)$ for some $m,n\in{\mathbb N}$}\}$$**
> has bounded height.

In this case, note that $C = \mathbb{P}^1_{\overline{\mathbb{Q}}}$. Moreover, in the general case, $a$ and $b$ are maps $C \to \mathbb{P}^1$[^7], but in the special case of the theorem, $a$ and $b$ are constant functions, i.e. elements of $\overline{\mathbb{Q}}$.

[^7]: Equivalently, $a$ and $b$ are elements of the function field $\overline{\mathbb{Q}}(C)$ and in particular, it makes sense to talk about $a(t)$ and $b(t)$

More generally, the paper proves

> [!Theorem] Theorem, [DeMarco et al, Corollary 7.5],
> Let $d$ be a prime power and let $f(z)=z^d+t\in\overline{\mathbb{Q}}[t][z]$. 
> Let $a,b\in \overline{\mathbb{Q}}$ exactly one of which is an algebraic integer. 
> 
> Then the set 
> $$S=\{t_0\in\overline{\mathbb{Q}}:\ f^m_{t_0}(a)=f^n_{t_0}(b)\ \text{for some $m,n\in{\mathbb N}$}\}$$
> 
> has bounded height.





# Relationship between the unlikely intersection and bounded height problems[^5]

[^5]: The contents of this section are mostly drawn from private communications, cf. [[#^demarcoprivatecomm]]

[[#^demarcoprivatecomm|DeMarco provided me]] with some insights on one way in which general bounded height problems relate to unlikely intersection problems --- sets of bounded height are considered "sparse", and intersections of sparse sets should be very rare.

> [!Remark]
> [[#^demarcoprivatecomm|DeMarco further suggested]] a framework of this idea in practice. Many proofs showing that the intersection $A \cap B$ of sets $A$ and $B$ is finite or not Zariski dense, first show that both $A$ and $B$ have bounded height[^6]. One can use the boundedness of height to build "good" alternative height functions $h_A$ and $h_B$ and the sets of bounded height become sets of zero height under these alternative height functions. Equidistribution results can then show equidistribution towards a natural measure thereby showing that $A \cap B$ cannot be Zariski dense or sufficiently generic.

[^6]: Such sets $A$ and $B$ do not always have bounded height, but they have been shown to have bounded height in many important examples.

Now in the case of the [[#^672a02|proposed problem]], DeMarco also shared with me ideas from Bombieri, Zannier, and their various coauthors --- let the set of orbit collisions fill the role of $A$. We know that this set is infinite (and therefore Zariski dense in $C$), but now the question is whether this set is "sparse". We can now explore/generate problems by choosing a set to fill the role of $B$.

# Some questions that DeMarco et al address

## Wide generalization of the proposed problems
[[#General question of bounded height in a dynamically defined curve[ 3|Recall that]] DeMarco's proposed problem and the theorem in DeMarco et al deals with the set of orbit collisions of *two* families $f^n_t$ and $g^m_t$ of maps $\mathbb{P}^1 \to \mathbb{P}^1$. 

Here is a generalization:

> [!Problem]
> Let $C$ be a projective curve defined over $\overline{\mathbb{Q}}$ and **$\mathcal{F}=\overline{\mathbb{Q}}(C)$**.  Fix $r\geq 2$, and $f_1(z),\ldots,f_r(z)\in \mathcal{F}(z)$ of degrees $d_1, \ldots, d_r \geq 2$.  Given points $c_1,\ldots,c_r\in {\mathbb P}^1(\mathcal{F})$, let **$f_i^n(c_i)$** denote their iterates under $f_i$ in ${\mathbb P}^1(\mathcal{F})$.  Let $V$ be a hypersurface in $({\mathbb P}^1)^r$, defined over $\mathcal{F}$.  When can we conclude that the set
> 
> $$\begin{eqnarray*} 
>  \{\; t\in C(\overline{\mathbb{Q}}) & : &\mbox{ there exist } n_1,\ldots, n_r \geq 0 \mbox{ such that the specialization }\\  
>  	&& ( f_1^{n_1}(c_{1}),\ldots,f_r^{n_r}(c_r))_t \mbox{ lies in }  V_t(\overline{\mathbb{Q}}) \;\}
> \end{eqnarray*}$$
> has bounded height? 

Setting $r = 2$ and $V$ be the diagonal of $(\mathbb{P}^1)^r$ yields the proposed problem.

## Conjecture surrounding the proposed problem

Let us introduce some notation:
- $C/\overline{\mathbb{Q}}$ denotes a curve. ^d183d8
- $\mathcal{F}$ denotes the function field $\overline{\mathbb{Q}}(C)$. ^a6e2e1

> [!Conjecture] Conjecture [DeMarco et al, Conjecture 1.5]
> Fix $f(z),g(z)\in \mathcal{F}(z)$ with degrees at least $2$ and **$a,b\in {\mathbb P}^1(\mathcal{F})$**. 
> Assume that at least one of $f$ and $g$ is not [[demarco_et_al_bhfds_5_1|special]][^8].  Set
> 
> [^8]: i.e. at least one of $f$ and $g$ is not conjugate via a Mobius transformation to $\pm z^d$, $\pm T_d(z)$ (where $T_d$ is the Chebyshev polynomial, or a [[demarco_et_al_bhfds_5_1|Lattes map]].
> 
> **$$S:=\{t\in C(\overline{\mathbb{Q}}): \text{$f_t^m(a(t))=g_t^n(b(t))$ for some $m,n \geq 0$}\}.$$**  
> 
> Then at least one of the following statements must hold:
> 
> 1. Either $(f,a)$ or $(g,b)$ is isotrivial.
> 2. There exist $m,n \geq 0$ such that  $f^m(a)=g^n(b)$.
> 3. $S$ has bounded height.
> 

Here, $(f,a)$ is **isotrivial** if there exists a fractional linear transformation $\mu\in \overline{\mathcal{F}}(z)$ such that $\mu\circ f\circ \mu^{-1}\in \overline{\mathbb{Q}}(z)$ and $\mu(c)\in {\mathbb P}^1(\overline{\mathbb{Q}})$.

Note that condition $2$ is an obstruction to $S$ having bounded height; if $2$ holds, then $S$ is simply all of $C(\overline{\mathbb{Q}})$. Condition $1$ can also lead to unbounded height. For example, if $f(z) \in \overline{\mathbb{Q}}(z)$ (i.e. $f$ is constant in $t$) and $a \in \mathbb{P}^1(\overline{\mathbb{Q}})$ is not preperiodic for $f$, then the sequence $\{f^m(a)\}_{m \geq 0}$ has unbounded height in $\mathbb{P}^1(\overline{\mathbb{Q}})$ by the Northcott property of the Weil height[^9]. Fixing $n$, the solutions to the equations
	$$f^m(a)=g_t^n(b(t))$$
as $m$ goes to infinity will also have unbounded height[^10].

[^9]: The Northcott property of the Weil height states that there are only finitely many objects (e.g. points, numbers etc) of bounded degree and height. In particular, what is being said here is that $\{f^m(a)\}_{m \geq 0}$ has infinitely many distinct points because $a$ is not preperiodic for $f$, and thus $\{f^m(a)\}_{m \geq 0}$ has unbounded height by the Northcott property.

[^10]: I imagine that the solutions to the equations as $m$ goes to infinity have unbounded height because the heights of $f^m(a)$ tend to $\infty$ whereas the height of $g_t^n(b(t))$ is asymptotically close to the height of $t$.


Let us introduce more notation:

- $d_1, d_2$ denotes the degrees of given families $f_t, g_t: \mathbb{P}^1 \to \mathbb{P}^1$ (as functions in $z$ over $\mathcal{F}$, not as functions in $t$.) ^bf2862
- $\hat{h}_f$ denotes the canonical height function on $\mathbb{P}^1(\mathcal{F})$ associated to $f: \mathbb{P}^1 \to \mathbb{P}^1$ defined over $\mathcal{F}$. It was constructed and studied by Call and Silverman. ^28333d
- $\mathcal{M}$ denotes the set $\{(m,n) \in \mathbb{N}^2: d_1^m \hat{h}_f(a) = d_2^m \hat{h}_g(b) \}$ given $f,g: \mathbb{P}^1 \to \mathbb{P}^1$ defined over $\mathcal{F}$. ^bfe3a5
- $S_\mathcal{M}$ denotes the set $\{t \in C(\overline{\mathbb{Q}}): f_t^m(a(t)) = g_t^n(b(t)) \text{ for some } (m,n) \in \mathcal{M}\}$. ^07d71b


Demonstrating the conjecture reduces to showing that $S_\mathcal{M}$ has bounded height, assuming that $d_1$ and $d_2$ are **multiplicatively dependent**, i.e. $d_1^m = d_2^n$ for some nonzero integers $m,n$.


> [!Theorem] Theorem [DeMarco et al, Theorem 1.7]
> Let $C$, $\mathcal{F}$, $f(z)$, $g(z)$, $a$, $b$, $S$, $\mathcal{M}$, and $S_{\mathcal{M}}$ be as above, and assume that $d_1=\deg(f)\geq 2$ and $d_2=\deg(g)\geq 2$ are multiplicatively dependent. 
> (We allow the possibility that both $f$ and $g$ are [[demarco_et_al_bhfds_5_1|special]].) 
> If the set $S_{\mathcal{M}}$ has bounded height, then one of the following holds:
> 
> 1. Either $(f,a)$ or $(g,b)$ is isotrivial. 
> 2. There exist $m,n \geq 0$ such that $f^m(a)=g^n(b)$.
> 3. $S$ has bounded height. 
>  
> In particular, if $\mathcal{M}$ is empty, then the Conjecture holds for the pairs $(f,a)$ and $(g,b)$.
> 

^a9a05d

In particular, this theorem allows one to prove that $S$ has bounded height by 1. assuming that $(f,a)$ and $(g,b)$ are not isotrivial, 2. assuming that there do not exist $m,n \geq 0$ such that $f^m(a) = g^n(b)$ (as functions of $t$), and 3. showing that $S_\mathcal{M}$ is of bounded height, see \[[[#^demarcoetalbhfds|DeMarco et al]], Theorem 7.1]. 



# Notations used
- $C/\overline{\mathbb{Q}}$ [[#^d183d8|denotes]] a curve.
- $\mathcal{F}$ [[#^a6e2e1|denotes]] the function field $\overline{\mathbb{Q}}(C)$.
- $d_1,d_2$ [[#^bf2862|denotes]] the degrees of given families $f_t,g_t: \mathbb{P}^1 \to \mathbb{P}^1$ (as functions in $z$ over $\mathcal{F}$).
- $\hat{h}_f$ [[#^28333d|denotes]] the canonical height function on $\mathbb{P}^1(\mathcal{F})$ associated to $f: \mathbb{P}^1 \to \mathbb{P}^1$ defined over $\mathcal{F}$. It was constructed and studied by Call and Silverman.
- $\mathcal{M}$ [[#^bfe3a5|denotes]] 
- $\mathcal{O}_{\phi(\alpha)}$ [[#^044f9f|denotes]] the forward orbit of the point $\alpha$ of a (discrete) dynamical system $(S, \phi)$. It is defined as the set $$  \mathcal{O}_\phi(\alpha)=\mathcal{O}(\alpha)=\left\{\phi^n(\alpha): n \geq 0\right\}.$$
- $S$ [[#^a9a05d|denotes]] the set $$S := \{t \in C(\overline{\mathbb{Q}}): f_t^m(a(t)) = g_t^n(b(t)) \text{ for some } m,n \geq 0\}$$ where $C/\overline{\mathbb{Q}}$ is a curve, $f_t,g_t: \mathbb{P}^1 \to \mathbb{P}^1$ are families of maps defined over $\overline{\mathbb{Q}}$ parameterized by the function $t$ on $C$.
- $S_\mathcal{M}$ [[#^07d71b|denotes]] the set $\{t \in C(\overline{\mathbb{Q}}): f_t^m(a(t)) = g_t^n(b(t)) \text{ for some } (m,n) \in \mathcal{M}\}$.



# See Also



# Meta
## References

## Citations and Footnotes

# See Also

# Meta
## References

## Citations and Footnotes