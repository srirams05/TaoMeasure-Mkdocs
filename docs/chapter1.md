



## Jordan Measure



Let $I$ be an interval of the real line. The length of $I$ given by $|I|$ can be recovered by the limiting formula
$$
|I| = \lim_{N \to \infty} \frac{1}{N} \\#(I \cap \frac{1}{N} Z)
$$
where: $\frac{1}{N} Z := \{\frac{n}{N}: n \in Z\}$, $Z$ is the set of integers and $\#(A)$ denotes the cardinality of the finite set $A$.

Prove this statement.
 
**Answer** 

Below is a standard proof that for a (bounded) interval $I \subset \mathbb{R}$, its length $\lvert I\rvert$ can be recovered by counting how many points of the form $\tfrac{n}{N}$ (with $n \in \mathbb{Z}$) lie in $I$ and then dividing by $N$.  Indeed, one often writes:  
   
$$  
\lvert I\rvert  
\;=\;  
\lim_{N \to \infty}   
\frac{1}{N}\,\#\bigl(I \cap \tfrac{1}{N}\mathbb{Z}\bigr),  
$$  
   
which is a well-known way to recover the length (Lebesgue measure) of $I$. Below is a step-by-step proof for the case of a closed and bounded interval $I = [a,b]$. One can adapt the reasoning to open, half-open, or other intervals with minor modifications.  
   
1 **Setup and notation**  
   
• Let $I = [a,b]$ be a (closed) bounded interval in $\mathbb{R}$.    
• For each positive integer $N$, define 

$$  
A_N \;=\; I \cap \tfrac{1}{N}\mathbb{Z}  
\;=\;  
\bigl\{ \tfrac{n}{N} : n\in \mathbb{Z}, \;\tfrac{n}{N}\in [a,b] \bigr\}.  
$$  

• Let $\#A_N$ denote the number of elements in $A_N$. Since $\tfrac{n}{N}\in [a,b]$ forces $n$ to be in a finite range, $\#A_N$ is a finite integer.    
  
We want to show  

$$  
\lvert I\rvert \;=\; b-a  
\;=\;  
\lim_{N\to \infty} \frac{1}{N}\,\#(A_N).  
$$  
   
2 **Counting the number of multiples in the interval**  
   
Observe that  

$$  
A_N  
\;=\;  
\left\{ \tfrac{n}{N} : n \in \mathbb{Z}, \; a \,\le\, \tfrac{n}{N} \,\le\, b \right\}.  
$$  

This means  

$$  
a \;\le\; \tfrac{n}{N} \;\le\; b  
\quad\Longleftrightarrow\quad  
aN \;\le\; n \;\le\; bN.  
$$  

Hence the integers $n$ that belong to $A_N$ must satisfy  

$$  
n \;\in\; \bigl\{ \lceil aN \rceil, \; \lceil aN \rceil + 1,   
\ldots, \lfloor bN \rfloor-1,\; \lfloor bN \rfloor \bigr\}.  
$$  

Therefore,  

$$  
\#A_N  
\;=\;  
\lfloor bN \rfloor \;-\; \lceil aN \rceil \;+\; 1.  
$$ 

(The “$+1$” accounts for including both endpoints in the count of integers.)  
   
3 **Bounding $\#A_N$ from above and below**  
   
We know that for any real number $x$, 

$$  
x-1 < \lfloor x \rfloor \;\le\; x,  
\quad  
x \le \lceil x \rceil < x + 1.  
$$  

Applying these to $\lfloor bN\rfloor$ and $\lceil aN\rceil$:  
   
1. $\lfloor bN \rfloor \;\ge\; bN - 1.$    
2. $\lceil aN \rceil \;\le\; aN + 1.$  
   
Thus  

$$  
\#A_N  
\;=\;  
\lfloor bN \rfloor - \lceil aN \rceil + 1  
\;\ge\;  
\bigl(bN - 1\bigr) - \bigl(aN + 1\bigr) + 1  
\;=\;  
(b-a)\,N \;-\; 1.  
$$  

Similarly,  

$$  
\#A_N  
\;=\;  
\lfloor bN \rfloor - \lceil aN \rceil + 1  
\;\le\;  
\lfloor bN\rfloor - \bigl(aN\bigr) + 1  
\;\le\;  
(bN) - (aN) + 1  
\;=\;  
(b-a)\,N + 1.  
$$  
Hence  
$$  
(b-a)\,N - 1  
\;\le\;  
\#A_N  
\;\le\;  
(b-a)\,N + 1.  
$$  
   
4 **Dividing by $N$ and taking the limit**  
   
Divide the above chain of inequalities by $N>0$:  
   
$$  
(b-a)  
\;-\;  
\frac{1}{N}  
\;\;\le\;\;  
\frac{\#A_N}{N}  
\;\;\le\;\;  
(b-a)  
\;+\;  
\frac{1}{N}.  
$$  

As $N \to \infty$, both of the bounds  

$$  
(b-a)\;-\;\frac{1}{N}  
\quad\text{and}\quad  
(b-a)\;+\;\frac{1}{N}  
$$  

converge to $(b-a)$. By the squeeze theorem, we conclude  

$$  
\lim_{N\to\infty}  
\frac{\#(A_N)}{N}  
\;=\;  
b-a  
\;=\;  
\lvert I\rvert.  
$$  
   
In other words,  

$$  
\lvert I\rvert  
\;=\;  
\lim_{N\to \infty}  
\frac{1}{N}\;\#\bigl(I \,\cap\, \tfrac{1}{N}\mathbb{Z}\bigr).  
$$  
   
5 **Remarks on variants of the statement**  
   
• If one uses the union $I \cup \tfrac{1}{N}\mathbb{Z}$, this set is typically infinite, so $\#\bigl(I \cup \tfrac{1}{N}\mathbb{Z}\bigr) = \infty$. The usual statement is indeed about the intersection $I \cap \tfrac{1}{N}\mathbb{Z}$.    
• If $I$ is not bounded or not closed, one can refine the above argument by approximating $I$ by bounded closed intervals or handling endpoints carefully. The limit argument remains essentially the same and the length is still recovered.    
• This formula is a discrete analog of the idea behind Riemann integration: counting how many equally-spaced points fall into $I$ is akin to a Riemann sum for the indicator function of $I$.    
  
Thus the key takeaway is:  
   
$$  
\boxed{  
\text{For a bounded interval }I = [a,b],\quad  
\lim_{N\to \infty}  
\dfrac{1}{N}\,\#\Bigl(I \cap \tfrac{1}{N}\mathbb{Z}\Bigr)  
\;=\;  
b - a  
\;=\;  
\lvert I\rvert.  
}  
$$

## Intuition of counting argument

***I am having trouble on the intuition of this result. We seem to be equating the cardinality of a set with the length of an interval which does not seem to make sense. By measuring the cardinality are we measuring the number of equal length sub intervals in $I$? Provide an intuitive explanation.***

Here is one intuitive way to think about the identity  

$$  
|I| \;=\; \lim_{N\to\infty} \frac{1}{N}\, \# \Bigl(I \cap \tfrac{1}{N}\mathbb{Z}\Bigr).  
$$  
   
1) Think of sampling points in I.    
   – Consider the set $\tfrac{1}{N}\mathbb{Z}=\{\tfrac{n}{N}: n\in \mathbb{Z}\}$. These points “chop up” the real line into little increments of length $\tfrac{1}{N}$.    
   – The expression $\#(I \cap \tfrac{1}{N}\mathbb{Z})$ is simply the number of these chopped-up points that end up falling inside the interval $I$.    
  
2) Why divide by $N$?    
   – Since each “chop” is of width $\tfrac{1}{N}$, if you want to approximate the length of $I$ by the number of chops, you must multiply (or effectively “weight”) the count by that chop-size $\tfrac{1}{N}$.    
   – Equivalently, dividing the count by $N$ is the same as multiplying it by $\tfrac{1}{N}$. Hence
   
   $$  
       \frac{1}{N}\, \\# \bigl(I \cap \tfrac{1}{N}\mathbb{Z}\bigr)\;=\;  
       \bigl(\tfrac{1}{N}\bigr)\times   
       \bigl(\text{number of points of spacing } \tfrac{1}{N}\text{ in }I\bigr).  
     $$  
   
3) Relation to a “ruler” analogy.    
   – Imagine laying down a “ruler” marked only at the fractions $\tfrac{0}{N}, \tfrac{1}{N}, \tfrac{2}{N}, \dots$.    
   – Counting how many marks of that ruler land in $I$ and then multiplying by $\tfrac{1}{N}$ is analogous to measuring $I$ using only these coarse marks.    
  
4) Why do we need a limit as $N\to\infty$?    
   – For small $N$, this coarse measurement might glancingly miss a bit of $I$ near the edges or skip small gaps. But as $N$ becomes larger, the marks become denser and the count becomes a better and better approximation of the actual length.    
   – In the limit $N \to \infty$, the quantity    
     $\tfrac{1}{N}\, \# \bigl(I \cap \tfrac{1}{N}\mathbb{Z}\bigr)$    
     converges to the exact length of $I$.    
  
Thus, we are not literally equating “number of points” with “length”: rather, we count how many evenly spaced points of spacing $\tfrac{1}{N}$ fit in $I$, and then multiply that count by the spacing $\tfrac{1}{N}$. That product approximates the length of $I$. As the spacing $\tfrac{1}{N}$ goes to $0$ (i.e., $N \to \infty$), this approximation converges to the true length of $I$.

## Elementary sets

Given an interval $I$, define a box $B = I_1 \times I_2 \times \cdots, \times I_d$. $B \in R^d$
$|I| = b-a$ when $I = [a b], \; (a b), \; [a b), \; (a b]$. Similarly, 
$\text{vol}(B) = |I_1| \times |I_2| \times \cdots \times |I_d|$

Define an elementary set $E$ to be the finite, disjoint union of boxes $B$ as defined above.

the measure of $E$ is given by $m(E)$ is the sum of the volumes of the boxes of the disjoint partition.

Now consdier a general, bounded set $S$. Define the concept of Jordan measure of $S$ using the measure of elementary sets.

**Answer**


Below is one common way to define the Jordan measure of a bounded set in $\mathbb{R}^d$, using the notion of elementary sets (finite unions of disjoint boxes):  
   
1) Elementary sets and their measure  
─────────────────────────────────────────────── 


1. An (open/closed/half‐open) interval in $\mathbb{R}$ has length    
   $$  
   |I| \;=\; b - a  
   \quad  
   \text{if}  
   \quad  
   I  
   \;=\;  
   [\,a,b\,],\;\,(a,b),\;\,[\,a,b),\;\,(a,b\,].  
   $$  
2. A box $B\subset \mathbb{R}^d$ is a product of intervals:  
   $$  
   B \;=\; I_1 \,\times\, I_2 \,\times\,\cdots\,\times\, I_d,  
   $$  
   where each $I_k\subset \mathbb{R}$ is an interval. The volume of such a box is  
   $$  
   \mathrm{vol}(B)  
   \;=\;  
   |I_1| \,\times\, |I_2| \,\times\,\cdots\times\, |I_d|.  
   $$  
3. An elementary set $E\subset\mathbb{R}^d$ is a finite union of boxes that are pairwise disjoint:  
   $$  
   E \;=\; B_1 \;\cup\; B_2 \;\cup\; \cdots \;\cup\; B_n,  
   \quad  
   B_i \cap B_j = \varnothing \;\;(i\neq j).  
   $$  
   The measure (or volume) of $E$ is defined as the sum of the volumes of its boxes:  
   $$  
   m(E)  
   \;=\;  
   \sum_{i=1}^n \mathrm{vol}(B_i).  
   $$  
   
──────────────────────────────────────  
2) Outer and inner approximations by elementary sets  ───────────────────────────────────────  
Let $S\subset \mathbb{R}^d$ be a bounded set. We approximate $S$ from “above” and “below” by elementary sets:  
   
• An elementary set $E$ is called an outer approximation of $S$ if 
$S \subseteq E$.    
• An elementary set $F$ is called an inner approximation of $S$ if $F \subseteq S$.  
   
Define:    
• The outer (“upper”) measure of $S$ by    

  $$  
  m^*(S)  
  \;=\;  
  \inf \bigl \\{ \,m(E) \;:\; E \text{ is an elementary set and } S \subseteq E \bigr \\}.  
  $$    

• The inner (“lower”) measure of $S$ by   

  $$  
  m_*(S)  
  \;=\;  
  \sup \bigl \\{\,m(F) \;:\; F \text{ is an elementary set and } F \subseteq S \bigr \\}.  
  $$  
   
────────────────────────────────────────────────  
3) Jordan measurability and Jordan measure  
────────────────────────────────────────────────  
We say that a bounded set $S\subset\mathbb{R}^d$ is Jordan measurable if the outer and inner measures coincide:  

$$  
m^*(S) \;=\; m_*(S).  
$$  

In that case, we define the Jordan measure of $S$ (also called the Jordan content) to be this common value:  

$$  
m(S)  
\;=\;  
m^*(S)  
\;=\;  
m_*(S).  
$$  
   
Intuitively:    
• If you can cover $S$ by some finite union of boxes (an elementary set) with total volume very close to some number $L$, and also fit inside $S$ a disjoint union of boxes with total volume very close to the same number $L$, then that “squeezes” the measure of $S$ to exactly $L$.    
• If no matter how carefully you cover $S$ from above and below by elementary sets, there remains a “gap” in the volumes, then $S$ is not Jordan measurable.  
   
Thus, for a bounded set $S\subset \mathbb{R}^d$, its Jordan measure (if it exists) is the unique value you get by approximating $S$ from inside and outside by finite unions of boxes, and letting those approximations converge.

## $\varepsilon$ superset

In many of the proofs, you use a result like this. For a Jordan measurable set $S \in R^d$, if $E \supset S$ is an elementary set, then we have that for any $\varepsilon > 0$, 

\[ 
m(E) < m^{*,J}(S) + \varepsilon
\]

Why is this true? Explain.

**Answer**

Below is an explanation based on the definition of infimum in the context of outer measures:

──────────────────────────────

1) Jordan outer measure as an infimum
   
──────────────────────────────

Recall that the Jordan outer measure of a bounded set \(S\subset\mathbb{R}^d\) is defined by  

\[
m^{*,J}(S)
\;=\;
\inf
\Bigl\{
\,m(E)
\,\Bigm|\;
E \supset S,\;
E \text{ is an elementary set}
\Bigr\}.
\]

An “elementary set” here means a finite union of pairwise disjoint boxes in \(\mathbb{R}^d\).  

────────────────────────────

2) Property of the infimum
   
────────────────────────────

By definition of the infimum, if 

\[
z \;=\; \inf\{\,x_\alpha : \alpha \in A\}\quad \text{for some set } \{x_\alpha\}_{\alpha\in A},
\]

then for each \(\varepsilon>0\), there exists an element \(x_{\alpha_0}\) in that set such that  

\[
x_{\alpha_0} \;<\; z \;+\;\varepsilon.
\]

In other words, infimum means “greatest lower bound,” and one can always find an element whose value is within any prescribed \(\varepsilon\)-distance above \(z\).

──────────────────────────────

3) Applying this to the outer measure
 
───────────────────────────────

Since

\[
m^{*,J}(S)
\;=\;
\inf
\Bigl\{
m(E)
\;\Bigm|\;
E \supset S, 
\;E\text{ is elementary}
\Bigr\},
\]

take \(\varepsilon>0\). By the property of the infimum, there must exist at least one elementary set \(E_0\) covering \(S\) such that

\[
m(E_0)
\;<\;
m^{*,J}(S)
\;+\;
\varepsilon.
\]

Hence:

 • “For every \(\varepsilon>0\), we can choose an elementary superset \(E_0\) of \(S\) whose measure is less than \(m^{*,J}(S) + \varepsilon\).”

This is exactly the statement so often used in proofs: one picks an appropriate elementary set that covers \(S\), with total volume arbitrarily close to \(m^{*,J}(S)\).

────────────────────────────

4) Why this is used in proofs
   
────────────────────────────

This fact is crucial whenever we want to show that we can approximate \(S\) “from the outside” by an elementary set with measure no more than a small amount above \(m^{*,J}(S)\). Among other things, it allows one to  
• show sub-additivity properties,  
• merge or split covers in precise ways,  
• argue that boundaries can be covered with arbitrarily small volumes, etc.

All these steps rely on the ability to pick “near-optimal” covers of \(S\) whose measure sits just over \(m^{*,J}(S)\) by at most \(\varepsilon\).





## $\varepsilon$ subset

It would see that there should be an analogous result when we approximate $S$ “from the inside” by an elementary set and use the supremum property. Is this correct?

**Answer**

Yes, precisely. In fact, the Jordan inner measure of a bounded set \(S\subset\mathbb{R}^d\) is defined by  

\[
m_{*,J}(S)
\;=\;
\sup
\Bigl\{
\,m(E)
\;\Bigm|\;
E \subset S,\;
E \text{ is an elementary set}
\Bigr\}.
\]

The property of a supremum says:

If 

\[
L
\;=\;
\sup
\{\,x_\alpha : \alpha \in A\}\quad\text{for some set }\{x_\alpha\}_{\alpha\in A},
\]

then for each \(\varepsilon>0\), there is an \(x_{\alpha_0}\) in that set such that

\[
x_{\alpha_0}
\;>\;
L
\;-\;
\varepsilon.
\]

Hence, applied to Jordan inner measure, given \(\varepsilon>0\), there must exist an elementary set \(E_0 \subset S\) such that

\[
m(E_0)
\;>\;
m_{*,J}(S)
\;-\;
\varepsilon.
\]

This is the inside‐approximation analogue of the outer‐approximation fact  

\[
m(E_0)
\;<\;
m^{*,J}(S)
\;+\;
\varepsilon
\quad
\text{for some }
E_0 \supset S.
\]

Both properties—the ability to find an “optimal” cover of \(S\) from outside (within any \(\varepsilon>0\) of \(m^{*,J}(S)\)) and to find an “optimal” contained set (within any \(\varepsilon>0\) of \(m_{*,J}(S)\))—are at the heart of how Jordan outer and inner measures are used in proofs.


---------
Let $B \in R^d$ be a closed box. Let $f: B \to R$ be continuous. 
The set $\{(x, f(x): x \in B\} \in R^{d+1}$ is the graph of $f$. 
Show that it is Jordan measurable.
--------------

Explanation:  
   
We wish to show that if $B \subset \mathbb{R}^d$ is a closed box and $f : B \to \mathbb{R}$ is a continuous function, then the graph 

$$  
G \;=\; \bigl \\{ (x, f(x)) : x \in B \bigr \\}  
\;\subset\;  
\mathbb{R}^{d+1}  
$$  

is Jordan measurable in $\mathbb{R}^{d+1}$.    
  
The key idea is that although $G$ lives in $\mathbb{R}^{d+1}$, it is “only” $d$-dimensional in nature; as a result it occupies no $(d+1)$-dimensional volume, and one can cover it by boxes of arbitrarily small total volume. From the fundamental criterion for Jordan measurability in $\mathbb{R}^{d+1}$ (a bounded set is Jordan measurable if and only if its boundary has measure zero), it will follow that $G$ has $(d+1)$-dimensional Jordan measure zero and hence is Jordan measurable.  
   
────────────────────────────────────────────────  
1) $G$ is closed and bounded  
────────────────────────────────────────────────  
1. Since $B$ is a closed box in $\mathbb{R}^d$, it is compact.    
2. Since $f$ is continuous on the compact set $B$, it is bounded and uniformly continuous on $B$. Hence $\{ (x,f(x)) : x \in B\}$ is contained in a closed and bounded region in $\mathbb{R}^{d+1}$.    
3. The graph $G$ is also a closed subset of $\mathbb{R}^{d+1}$ (continuity of $f$ ensures that).    
  
Hence $G\subset \mathbb{R}^{d+1}$ is closed and bounded.  
   
──────────────────────────────────────────────────  
2) Covering $G$ with “thin pillars”  
────────────────────────────────────────────────────  
To show $G$ has $(d+1)$-dimensional measure zero, we will cover it by sets (boxes in $\mathbb{R}^{d+1}$) whose total volume can be made arbitrarily small.    
  
Because $f$ is uniformly continuous, given $\varepsilon > 0$, there exists $\delta > 0$ such that whenever $\|x - y\| < \delta$ in $B$, we have  

$$  
\bigl\vert \,f(x)\;-\;f(y)\bigr \vert < \varepsilon.  
$$  

Now partition the box $B\subset \mathbb{R}^d$ into finitely many smaller boxes $B_1, B_2, \dots, B_n$ so that the diameter of each $B_i$ is less than $\delta$. Hence, within each $B_i$, the function $f$ varies by no more than $\varepsilon$.  
   
For each such $B_i$, consider its “vertical extension” or “pillar” in $\mathbb{R}^{d+1}$: 

$$  
\widehat{B}_i  
\;=\;  
B_i  
\times  
\bigl[\,\min_{x\in B_i}f(x),\,\max_{x\in B_i}f(x)\bigr]  
\;\subset\;  
\mathbb{R}^{d+1}.  
$$  

Because the oscillation of $f$ on $B_i$ is at most $\varepsilon$, we see   

$$  
\bigl[\min_{x\in B_i}f(x),\,\max_{x\in B_i}f(x)\bigr]  
$$  

is an interval of length at most $\varepsilon$. Thus each $\widehat{B}_i$ has volume 

$$  
\mathrm{vol}\bigl(\widehat{B}_i\bigr)  
\;\le\;  
\mathrm{vol}\bigl(B_i\bigr) \;\times\; \varepsilon.  
$$  

Since $G\cap \bigl(B_i\times\mathbb{R}\bigr)$ is contained in $\widehat{B}_i$, the union of these pillars covers $G$:  

$$  
G  
\;\subseteq\;  
\bigcup_{i=1}^n \,\widehat{B}_i.  
$$  
   
Hence,  

$$  
\mathrm{vol}  
\Bigl(\bigcup_{i=1}^n \widehat{B}_i\Bigr)  
\;\le\;  
\sum_{i=1}^n \mathrm{vol}\bigl(\widehat{B}_i\bigr)  
\;\le\;  
\sum_{i=1}^n \Bigl(\mathrm{vol}(B_i)\times \varepsilon\Bigr)  
\;=\;  
\varepsilon  
\sum_{i=1}^n \mathrm{vol}(B_i).  
$$  

Since $\{B_i\}$ is just a partition of $B$, the sum of the $\mathrm{vol}(B_i)$ is $\mathrm{vol}(B)$, a fixed finite number. We can make $\varepsilon>0$ arbitrarily small, so: 

$$  
\forall \epsilon>0:  
\quad  
\exists  
\Bigl(\text{cover of }G\text{ by boxes of total volume }< \epsilon\Bigr).  
$$  

This implies $G$ has Lebesgue (or Jordan) measure zero in $\mathbb{R}^{d+1}$.  
   
───────────────────────────────────────────────────  
3) Conclusion: Jordan measurability  
────────────────────────────────────────────────────  
A bounded subset of $\mathbb{R}^{d+1}$ of measure zero is automatically Jordan measurable, because its boundary is contained within itself (a set of measure zero) and thus also has measure zero. Concretely, for Jordan measurability we need that the set is bounded and that for every $\varepsilon>0$, we can find an elementary set that covers $G$ with volume $< \varepsilon$, and another elementary set contained in $G$ of volume $> -\varepsilon$. But the second is trivial (take the empty set), and the first we saw how to construct.    
  
Hence,  

$$  
G  
\;=\;  
\bigl\{(x,f(x)): x\in B\bigr\}  
$$  

is Jordan measurable in $\mathbb{R}^{d+1}$. In fact, its Jordan measure (the $(d+1)$-dimensional “volume” of the hypersurface) is $0$.


***Let $B(x,r) := \{y \in R^d: |y - x| < r \}$ be an open ball centered at $x \in R^d$. Show that it is Jordan measurable.***


Explanation:  
   
To show that an open ball    

$$  
B(x,r)\;=\;\bigl\{\,y\in\mathbb{R}^d : \lvert y - x\rvert < r\bigr\}  
$$    

is Jordan measurable using only the notions of Jordan outer and inner measures, we must prove that 

$$  
m^*\bigl(B(x,r)\bigr)  
\;=\;  
m_*\bigl(B(x,r)\bigr).  
$$    

Recall:  
   
• The Jordan outer measure of $S\subset\mathbb{R}^d$ is  

  $$  
  m^*(S)  
  \;=\;  
  \inf  
  \Bigl \\{  
    m(E)  
    \;:\;  
    E \text{ is an elementary set and } S \subseteq E  
  \Bigr \\}.  
  $$  

• The Jordan inner measure of $S\subset\mathbb{R}^d$ is    

  $$  
  m_*(S)  
  \;=\;  
  \sup  
  \Bigl \\{  
    m(F)  
    \;:\;  
    F \text{ is an elementary set and } F \subseteq S  
  \Bigr \\}.  
  $$  

• A set $S$ is called Jordan measurable if $m^*(S) = m_*(S)$. In that case, that common value is denoted by $m(S)$.  
   
─────────────────────────────────────────  
1) Known volume of a ball  
─────────────────────────────────────────  
From geometry (or integration in spherical coordinates), one knows that the Lebesgue volume of a (closed or open) ball of radius $r$ in $\mathbb{R}^d$ is  

$$  
\omega_d\, r^d,  
$$  

where $\omega_d$ is the volume of the unit ball in $\mathbb{R}^d$. Our aim is to show 

$$  
m^*\bigl(B(x,r)\bigr)  
=  
m_*\bigl(B(x,r)\bigr)  
=  
\omega_d\,r^d.  
$$  
   
─────────────────────────────────────────  
2) Outer measure ≤ $\omega_d r^d$ + ε  
───────────────────────────────────────────  
We show that for every $\varepsilon > 0$, there is an elementary set $E_\varepsilon \supseteq B(x,r)$ whose total volume is less than $\omega_d r^d + \varepsilon$. Because $m^*(B(x,r))$ is the infimum of volumes of such covers, that will imply  

$$  
m^*\bigl(B(x,r)\bigr)  
\;\le\;  
\omega_d\,r^d.  
$$  
   
Step-by-step idea:    
1. Enclose the ball $B(x,r)$ in a large coordinate-aligned box (for instance, a cube of side $2r$ centered at $x$).    
2. Subdivide that box into a fine grid of little cubes (of side length $\delta$), so that (i) every cube that intersects $B(x,r)$ is included in the cover; (ii) the cubes are disjoint in the interior and together form an elementary set.    
3. As $\delta\to 0$, the total volume of cubes that intersect the ball approaches $\omega_d r^d$ from above.  The error near the “boundary shell” of the ball can be made as small as desired by choosing sufficiently fine subdivisions.    
  
This shows that for any $\varepsilon>0$, we can find an elementary set $E_\varepsilon$ with    

$$  
B(x,r)\;\subseteq\;E_\varepsilon  
\quad  
\text{and}  
\quad  
m\bigl(E_\varepsilon\bigr)<\omega_d r^d+\varepsilon.  
$$  

Hence,  

$$  
m^*\bigl(B(x,r)\bigr)\;=\;\inf_{S\supset B(x,r)}\,m(S)\;\le\;\omega_d\,r^d.  
$$  
   
────────────────────────────────────────  
3) Inner measure ≥ $\omega_d r^d$ - ε  
───────────────────────────────────────────  
We similarly show that for every $\varepsilon>0$, there is an elementary set $F_\varepsilon \subseteq B(x,r)$ whose total volume is at least $\omega_d r^d - \varepsilon$. Because $m_*(B(x,r))$ is the supremum of volumes of such “inscribed” elementary sets, this implies  

$$  
m_*\bigl(B(x,r)\bigr)  
\;\ge\;  
\omega_d\,r^d.  
$$  
   
One does almost the same subdivision, but now only keep those small cubes that fit entirely inside $B(x,r)$. Very close to the boundary, you may have small cubes that partially stick out; you discard those. By letting the grid size go to zero, the total volume of cubes that lie wholly inside $B(x,r)$ approaches $\omega_d r^d$ from below. In symbols, for any $\varepsilon>0$, one can refine the grid so that an inscribed elementary set $F_\varepsilon \subset B(x,r)$ has 

$$  
m\bigl(F_\varepsilon\bigr)  >  
\omega_d\,r^d - \varepsilon.  
$$  

Thus  

$$  
m_*\bigl(B(x,r)\bigr)  
\;=\;  
\sup_{F \subset B(x,r)}\,m(F)  
\;\ge\;  
\omega_d\,r^d.  
$$  
   
──────────────────────────────────  
4) Conclusion: Jordan measurability  
───────────────────────────────────  
Combining these two inequalities,  
   
• from above:  
  $\displaystyle m^*\bigl(B(x,r)\bigr)\;\le\;\omega_d\,r^d,$  
   
• from below:  
  $\displaystyle m_*\bigl(B(x,r)\bigr)\;\ge\;\omega_d\,r^d,$  
   
forces  

$$  
m^*\bigl(B(x,r)\bigr)  
\;=\;  
m_*\bigl(B(x,r)\bigr)  
\;=\;  
\omega_d\,r^d.  
$$  

Hence $B(x,r)$ is Jordan measurable, and its Jordan measure is exactly the usual volume $\omega_d\,r^d$.

***Let $S \subset R^d$ be a bounded set. Let $A, B \subset R^d$ be elementary sets such that $A \subset S \subset B$ and $m(B \setminus A) \leq \epsilon$ for every $\epsilon > 0$. This is equivalent to Jordan measurability of $S$. Prove this.***

Explanation:  
   
We wish to show that the following two statements about a bounded set $S \subset \mathbb{R}^d$ are equivalent:  
   
(1)  $S$ is Jordan measurable (i.e., $m^*(S) = m_*(S)$), where 

$$  
  m^*(S)  
     \;=\;  
     \inf\{m(E): E\supset S,\; E \text{ is elementary}\},   
     \quad  
     m_*(S)  
     \;=\;  
     \sup\{m(F): F\subset S,\; F \text{ is elementary}\}.
         $$    

   
(2)  For every $\varepsilon>0$, there exist elementary sets $A,B\subset \mathbb{R}^d$ such that   

   $$  
     A \;\subset\; S \;\subset\; B  
     \quad\text{and}\quad  
     m\bigl(B\setminus A\bigr)\;\le\;\varepsilon.  
             $$  
   
Below is a step‐by‐step proof of the equivalence.  
   
─────────────────────────────────────  
⇒ Direction (Jordan measurability implies the “ε-thin sandwich” property)  
─────────────────────────────────────  
   
Assume $S$ is Jordan measurable, so $m^*(S) = m_*(S)$. Let $\varepsilon > 0$. We will construct elementary sets $A\subset S \subset B$ such that $m(B \setminus A) < \varepsilon$.  
   
Step 1. Approximate $S$ from below.    
Since $m_*(S) = \sup\{ m(F) : F\subset S,\;F\text{ elementary}\}$, there is an elementary set $A\subset S$ so that    

$$  
m(A)  
\;>\;  
m_*(S) - \tfrac{\varepsilon}{2}.  
$$  
   
Step 2. Approximate $S$ from above.    
Since $m^*(S) = \inf\{ m(G) : G\supset S,\;G\text{ elementary}\}$, there is an elementary set $G\supset S$ so that   

$$  
m(G)  
\;<\;  
m^*(S) + \tfrac{\varepsilon}{2}.  
$$  
   
Step 3. Ensure $A \subset G$.    
Usually one needs a small refinement step: replace $G$ by an elementary set $B$ such that $A\subset B\subset G$ (if necessary, we can split boxes of $G$ to include those from $A$, so that $B$ and $A$ fit together nicely). This does not increase the measure, so 

$$  
m(B)\;\le\;m(G)  
\;<\;m^*(S)+\tfrac{\varepsilon}{2}.  
$$  

Hence we have  

$$  
A \;\subset\; S \;\subset\; B,  
$$  

with $A$ and $B$ elemental.  
   
Step 4. Estimate $m(B\setminus A)$.    
Since $B\setminus A\subset B$, we have 

$$  
m\bigl(B\setminus A\bigr)  
\;\le\;  
m(B) \;-\; m(A)  
\;\le\;  
\bigl(m^*(S) + \tfrac{\varepsilon}{2}\bigr)  
\;-\;  
\bigl(m_*(S) - \tfrac{\varepsilon}{2}\bigr)  
\;=\;  
m^*(S) - m_*(S) + \varepsilon.  
$$  

But for a Jordan measurable set, $m^*(S) - m_*(S)=0$. Therefore 

$$  
m\bigl(B\setminus A\bigr)  
\;\le\;  
\varepsilon.  
$$  

This shows that for every $\varepsilon>0$, we found $A,B$ elementary with $A\subset S\subset B$ and $m(B\setminus A)\le\varepsilon$.   
  
───────────────────────────────────  
⇐ Direction (“ε-thin sandwich” property implies Jordan measurability)  
───────────────────────────────────  
   
Conversely, suppose that for each $\varepsilon > 0$, there are elementary sets   

$$  
A_\varepsilon \;\subset\; S \;\subset\; B_\varepsilon  
\quad  
\text{with}  
\quad  
m\bigl(B_\varepsilon\setminus A_\varepsilon\bigr)\;\le\;\varepsilon.  
$$  

We want to conclude $S$ is Jordan measurable, i.e. $m^*(S) = m_*(S)$.  
   
Step 1. Relation to inner and outer measures.    
By definition:  

$$  
m_*(S)  
\;=\;  
\sup\{\,m(F):F \subset S,\;F\text{ is elementary}\}  
\quad\text{and}\quad  
m^*(S)  
\;=\;  
\inf\{\,m(G):G \supset S,\;G\text{ is elementary}\}.  
$$  

Since $A_\varepsilon \subset S\subset B_\varepsilon$, we have  

$$  
m_*(S)  
\;\ge\;  
m\bigl(A_\varepsilon\bigr)  
\quad\text{and}\quad  
m^*(S)  
\;\le\;  
m\bigl(B_\varepsilon\bigr).  
$$  

Hence  

$$  
m^*(S) \;-\; m_*(S)  
\;\le\;  
m\bigl(B_\varepsilon\bigr)  
\;-\;  
m\bigl(A_\varepsilon\bigr).  
$$  
   
Step 2. Relate $m(B_\varepsilon) - m(A_\varepsilon)$ to $m(B_\varepsilon\setminus A_\varepsilon)$.    
In general for an elementary set $A_\varepsilon\subset B_\varepsilon$, we have  

$$  
m\bigl(B_\varepsilon\bigr)  
\;-\;  
m\bigl(A_\varepsilon\bigr)  
\;\ge\;  
m\bigl(B_\varepsilon\setminus A_\varepsilon\bigr).  
$$  

(This inequality becomes an equality if both are unions of disjoint boxes and $A_\varepsilon\subset B_\varepsilon$ in a “compatible” way, but at least the “$\ge$” always holds.)  
   
From our assumption,  

$$  
m\bigl(B_\varepsilon\setminus A_\varepsilon\bigr)  
\;\le\;  
\varepsilon.  
$$  

Thus,  

$$  
m^*(S)\;-\;m_*(S)  
\;\le\;  
m\bigl(B_\varepsilon\bigr)\;-\;m\bigl(A_\varepsilon\bigr)  
\;\le\;  
m\bigl(B_\varepsilon\setminus A_\varepsilon\bigr)  
\;\le\;  
\varepsilon.  
$$  
   
Step 3. Conclude $m^*(S) = m_*(S)$.    
Because $\varepsilon>0$ was arbitrary, the above inequality implies

$$  
m^*(S)\;-\;m_*(S)\;=\;0,  
$$  

which is precisely the definition that $S$ is Jordan measurable.  
   
──────────────────────────────────────  
Conclusion  
──────────────────────────────────────  
   
The two statements are therefore equivalent:    
• “For every $\varepsilon>0$, there are elementary sets $A_\varepsilon \subset S\subset B_\varepsilon$ with $m(B_\varepsilon \setminus A_\varepsilon)\le \varepsilon$.”    
• “$S$ is Jordan measurable, i.e. $m^*(S) = m_*(S)$.”    
  
Hence the proof is complete.

***Let $E \subset R^d$ be a bounded set. and $F \subset R^d$ be an elementary set.***
***Show that $m^*(E) = m^*(E \cap F) + m^*(E\setminus F)$ where $m^*(\cdot)$ is the Jordan outer measure.***

Below is a “direct‐from‐definitions” proof of  

$$  
\mu^*(E)  
\;=\;  
\mu^*\bigl(E \cap F\bigr)  
\;+\;  
\mu^*\bigl(E \setminus F\bigr)  
$$    

for any bounded set $E\subset\mathbb{R}^d$ and any elementary set $F\subset\mathbb{R}^d$.    
Here, $\mu^*(\,\cdot\,)$ is the Jordan outer measure, defined by 

$$  
\mu^*(E)  
\;=\;  
\inf\!\Bigl\{\,\mu(G):G\supset E,\;G\text{ is elementary}\Bigr\},  
$$    

and $\mu(\,\cdot\,)$ is the usual “volume” of an elementary set (finite union of boxes).  We will avoid appealing to any “general outer‐measure subadditivity theorem,” using instead only the geometric additivity properties of the volume of elementary sets.  
   
─────────────────────────────────────────────────  
1) Terminology: “Elementary Set” and its Volume  
   
• An elementary set in $\mathbb{R}^d$ is a finite union of boxes, each box being a Cartesian product of closed intervals.    
• The volume $\mu(G)$ of an elementary set $G$ is computed by summing the volumes of finitely many pairwise disjoint boxes that cover $G$.  One shows directly that if $G_1,G_2$ are elementary, then    

  $$  
  \mu\bigl(G_1\cup G_2\bigr)  
  \;\le\;  
  \mu(G_1) \;+\; \mu(G_2),  
  $$  

  simply by combining boxes and (if necessary) subdividing them into disjoint pieces.  
   
───────────────────────────────────────  
2) Desired Equality  
   
We want to prove that if $E\subset\mathbb{R}^d$ is bounded and $F\subset\mathbb{R}^d$ is elementary, then the two disjoint sets $E\cap F$ and $E\setminus F$ satisfy    

$$  
\mu^*(E)  
\;=\;  
\mu^*\bigl(E \cap F\bigr)  
\;+\;  
\mu^*\bigl(E \setminus F\bigr).  
$$  

Note that $E = \bigl(E\cap F\bigr)\cup \bigl(E\setminus F\bigr)$ is a disjoint union.  
   
We split the proof into two inequalities:  
   
─────────────────────────────────────────────────  
3) First Inequality:    
   
$$
\mu^*(E) ≤ \mu^*(E ∩ F) + μ*(E \setminus F).  
$$
   
(a) Cover each piece separately.    
• Let $\varepsilon > 0$.    
• By definition of $\mu^*(E\cap F)$, there is an elementary set $G_1\supset E\cap F$ with    

  $$  
  \mu(G_1)  
  \;<\;  
  \mu^*(E\cap F)  
  \;+\;  
  \tfrac{\varepsilon}{2}.  
  $$    

• Similarly, there is an elementary set $G_2\supset E\setminus F$ with  

  $$  
  \mu(G_2)  
  \;<\;  
  \mu^*(E \setminus F)  
  \;+\;  
  \tfrac{\varepsilon}{2}.  
  $$  
   
(b) Combine the covers.    
• Note that $E = (E\cap F)\cup(E\setminus F) \subset G_1\cup G_2$.    
• Set $H=G_1\cup G_2$.  Since the union of two elementary sets is again elementary, $H$ is an elementary set containing $E$.  By definition of outer measure,  

  $$  
  \mu^*(E)  
  \;\le\;  
  \mu(H).  
  $$  
   
(c) Relate μ(H) to μ(G1) and μ(G2).    
• Because $G_1$ and $G_2$ are each finite unions of boxes, one shows directly    

  $$  
  \mu\bigl(G_1 \cup G_2\bigr)  
  \;\le\;  
  \mu(G_1)  
  \;+\;  
  \mu(G_2).  
  $$    

  (This follows from decomposing the union into disjoint boxes, or, more simply, from the fact that elementary‐set “volume” satisfies finite subadditivity.)  
   
(d) Putting it together.    
 Consequently,  

$$  
  \mu^*(E)  \; \le \;  \mu(H)  =  
  \mu\bigl(G_1 \cup G_2\bigr)  
  \;\le\;  
  \mu(G_1)  
  +  
  \mu(G_2)  
  \;<\;  
  \Bigl(\mu^*(E\cap F) + \tfrac{\varepsilon}{2}\Bigr)  
  +  
  \Bigl(\mu^*(E\setminus F) + \tfrac{\varepsilon}{2}\Bigr).  
$$  

  Hence,  

$$  
  \mu^*(E)  
  \;<\;  
  \mu^*(E\cap F) \;+\; \mu^*(E\setminus F) \;+\; \varepsilon.  
$$  

• Letting $\varepsilon\to 0$, we obtain  

$$  
  \mu^*(E)  
  \;\le\;  
  \mu^*\bigl(E \cap F\bigr)  
  \;+\;  
  \mu^*\bigl(E \setminus F\bigr).  
$$  
   
─────────────────────────────────────────────  
4) Second Inequality:    
μ*(E) ≥ μ*(E ∩ F) + μ*(E \setminus F).  
   
(a) Cover $E$ as a whole.    
• Let $\varepsilon > 0$.  By definition of $\mu^*(E)$, there is an elementary $G\supset E$ with  

$$  
  \mu(G)  
  \;<\;  
  \mu^*(E) + \varepsilon.  
$$  
   
(b) Enclose each piece inside G.    
• Clearly, $E\cap F \;\subset\; G\cap F$ and $E\setminus F\;\subset\; G\setminus F.$    
• Then by monotonicity of outer‐measure cover,    

$$  
  \mu^*\bigl(E\cap F\bigr)  
  \;\le\;  
  \mu\bigl(G\cap F\bigr),  
  \quad  
  \mu^*\bigl(E\setminus F\bigr)  
  \;\le\;  
  \mu\bigl(G\setminus F\bigr).  
$$  
   
(c) Additivity on disjoint parts

 Observe that $G\cap F$ and $G\setminus F$ are disjoint elementary sets whose union is $G$.  Therefore    

$$  
  \mu(G)  =  
  \mu\bigl(G\cap F\bigr)  
  +  
  \mu\bigl(G\setminus F\bigr).  
$$   
  
(d) Conclude.    
• Summing the two inequalities in (b) and using the above partition of $G$:  

$$  
  \mu^*\bigl(E\cap F\bigr)  +  \mu^*\bigl(E\setminus F\bigr)  
  \;\le\;  
  \mu\bigl(G\cap F\bigr)  +  
  \mu\bigl(G\setminus F\bigr)  =  
  \mu(G)  
  \;<\;  
  \mu^*(E) + \varepsilon.  
$$   

• Letting $\varepsilon \to 0$ yields  

$$  
  \mu^*\bigl(E\cap F\bigr)  
  +  
  \mu^*\bigl(E\setminus F\bigr)  
  \;\le\;  
  \mu^*(E).  
$$  
   
────────────────────────────────────────  
5) Combine Both Inequalities  
   
From steps (3) and (4), we have  

$$  
\mu^*(E)  
\;\le\;  
\mu^*\bigl(E \cap F\bigr)  
\;+\;  
\mu^*\bigl(E \setminus F\bigr)  
\quad\text{and}\quad  
\mu^*\bigl(E \cap F\bigr)  
\;+\;  
\mu^*\bigl(E \setminus F\bigr)  
\;\le\;  
\mu^*(E).  
$$  

Hence   

$$  
\mu^*(E)  
\;=\;  
\mu^*\bigl(E \cap F\bigr)  
\;+\;  
\mu^*\bigl(E \setminus F\bigr),  
$$  

and the proof is complete—without ever invoking a “general subadditivity property of outer measures.” Instead, we used only:  
   
• The definition of $\mu^*(E)$ as an infimum of $\mu(G)$ over elementary covers $G$.    
• The fact that the measure $\mu(\,\cdot\,)$ of an elementary set is finite‐additive over disjoint unions and is ≤‐additive (i.e.\ $\mu(G_1\cup G_2)\le \mu(G_1)+\mu(G_2)$) for two elementary sets $G_1,G_2$.    
  
────────────────────────────────────  
Summary:  
   
For any bounded set $E$ in $\mathbb{R}^d$ and any elementary set $F$, the Jordan outer measure satisfies    

$$  
\mu^*(E)  
\;=\;  
\mu^*\bigl(E \cap F\bigr)  
\;+\;  
\mu^*\bigl(E \setminus F\bigr).  
$$  

Both directions of the proof follow directly from the definition of $\mu^*$ and the basic geometry of finite unions of boxes (i.e.\ elementary sets). This does not require invoking the usual “outer‐measure subadditivity theorem,” but only the simpler statement that    
$\mu(G_1 \cup G_2)\le \mu(G_1)+\mu(G_2)$    
for elementary $G_1,G_2$.





# Darboux and Riemann Integral

### Piecewise constant Integral

Let $f: [a \; \; b] \to R$ be a bounded, piecewise constant (p.c.) function on a finite partition $I_1, \cdots, I_n$ of $[a \; \; b]$. Let $c_i$ be the value of the function on the interval $I_i$. Then, the sum $\sum_i c_i |I_i|$ is defined to be the real number denoted as $\text{p.c.} \int_a^b f(x) dx$ and we will refer to it as the piecewise constant (p.c.) integral.

Prove the following properties:
+ Linearity
+ Monotonicity
+ any other relevant property

----------------------------------------------------

$$  
\textbf{Setup:}  
$$  
Let $[a,b]\subset \mathbb{R}$ be a closed and bounded interval.  Suppose we have a finite partition  
$$  
P:\quad a = x_0 < x_1 < x_2 < \cdots < x_{n-1} < x_n = b,  
$$  
and define the subintervals  
$$  
I_k \;=\; [\,x_{k-1},\,x_k\,],\quad k=1,\dots,n.  
$$  
A function $f:[a,b]\to \mathbb{R}$ is called piecewise constant on $P$ (or just “p.c. on $[a,b]$” if the partition is understood) if there exist constants $c_k\in \mathbb{R}$ such that  
$$  
f(x) \;=\; c_k  
\quad\text{for all }x\in (x_{k-1},\, x_k),  
\quad k=1,\dots,n.  
$$  
(We do not care about the values of $f$ at the partition endpoints.)  
   
The “piecewise constant (p.c.) integral” of $f$ over $[a,b]$ is defined by  
$$  
\mathrm{p.c.}\int_a^b f(x)\,dx  
\;:=\;  
\sum_{k=1}^{n}  
c_k \,\bigl|\,I_k\bigr|  
\;=\;  
\sum_{k=1}^n c_k \,\bigl(x_k - x_{k-1}\bigr).  
$$  
   
──────────────────────────────────────  
1) Linearity  
──────────────────────────────────────  
   
$$  
\textbf{Claim: }  
\quad  
\mathrm{p.c.}\int_a^b \bigl(\alpha f(x) + \beta g(x)\bigr)\,dx  
\;=\;  
\alpha\,\mathrm{p.c.}\int_a^b f(x)\,dx \;+\;\beta\,\mathrm{p.c.}\int_a^b g(x)\,dx,  
$$  
for any real scalars $\alpha,\beta$ and piecewise constant functions $f,g$.  
   
────────────────────────────────────  
$\bullet$ $\textit{Proof idea.}  $
   
Without loss of generality, refine the partition (if necessary) so that both $f$ and $g$ are piecewise constant on the same partition $P$. That is, there exist constants $c_k,d_k\in\mathbb{R}$ such that  
$$  
f(x) = c_k,\quad g(x)=d_k  
\quad\text{for }x\in (x_{k-1},x_k),  
\quad k=1,\dots,n.  
$$  
   
For $h(x) := \alpha f(x)+\beta g(x)$, we have $h(x)=\alpha c_k+\beta d_k$ when $x\in (x_{k-1},x_k)$. Then by definition:  
$$  
\mathrm{p.c.}\int_a^b h(x)\,dx  
\;=\;  
\sum_{k=1}^n \bigl(\alpha c_k + \beta d_k\bigr)\,\bigl(x_k - x_{k-1}\bigr).  
$$  
Meanwhile,  
$$  
\alpha\,\mathrm{p.c.}\int_a^b f(x)\,dx  
\;+\;\beta\,\mathrm{p.c.}\int_a^b g(x)\,dx  
\;=\;  
\alpha\sum_{k=1}^n c_k\,|I_k|  
\;+\;  
\beta\sum_{k=1}^n d_k\,|I_k|.  
$$  
Factoring out $\sum_{k=1}^n (x_k-x_{k-1})$, these are exactly the same sum.  Thus  
$$  
\mathrm{p.c.}\int_a^b \bigl(\alpha f + \beta g\bigr)  
\;=\;  
\alpha\,\mathrm{p.c.}\int_a^b f \;+\;\beta\,\mathrm{p.c.}\int_a^b g.  
$$  
   
Hence linearity holds.  
   
──────────────────────────────────────  
2) Monotonicity  
───────────────────────────────────────  
   
$$  
\textbf{Claim: }  
\quad  
\text{If }f(x)\le g(x)\text{ for all }x\in [a,b],  
\text{ then }  
\mathrm{p.c.}\int_a^b f(x)\,dx  
\;\le\;  
\mathrm{p.c.}\int_a^b g(x)\,dx.  
$$  
   
────────────────────────────────  
$\bullet$ $\textit{Proof idea.}  $
   
Again, we use a common partition $P$.  Suppose on each interval $(x_{k-1},x_k)$, $f(x)=c_k\le d_k=g(x)$. Then  
$$  
\mathrm{p.c.}\int_a^b f(x)\,dx  
\,=\,  
\sum_{k=1}^n c_k\,\bigl(x_k-x_{k-1}\bigr),  
\quad  
\mathrm{p.c.}\int_a^b g(x)\,dx  
\,=\,  
\sum_{k=1}^n d_k\,\bigl(x_k-x_{k-1}\bigr).  
$$  
Because $c_k\le d_k$ for each $k$ and $\bigl(x_k-x_{k-1}\bigr)\ge0$, each summand of the first sum is at most the corresponding summand of the second sum. Hence  
$$  
\sum_{k=1}^n c_k\,\bigl(x_k-x_{k-1}\bigr)  
\;\le\;  
\sum_{k=1}^n d_k\,\bigl(x_k-x_{k-1}\bigr).  
$$  
That is,  
$\mathrm{p.c.}\int_a^b f \;\le\;\mathrm{p.c.}\int_a^b g.$  
   
──────────────────────────────  
3) Additional Relevant Properties  
──────────────────────────────  
   
Here are a few other natural properties of the piecewise constant integral:  
   
————————————————————————————  
(a) Positivity:  
If $f(x)\ge 0$ on $[a,b]$, then  
$$  
\mathrm{p.c.}\int_a^b f(x)\,dx \;\ge\; 0.  
$$  
Indeed, if each constant value $c_k\ge0$, then each term $c_k\,|I_k|\ge0$, so their sum is nonnegative.  
   
————————————————————————————  
(b) Additivity (or “interval additivity”):  
If $c\in(a,b)$, then  
$$  
\mathrm{p.c.}\int_a^b f(x)\,dx  
\;=\;  
\mathrm{p.c.}\int_a^c f(x)\,dx  
\;+\;  
\mathrm{p.c.}\int_c^b f(x)\,dx.  
$$  
Proof sketch: If one has a partition of $[a,b]$, simply split it at the point $c$.  Then the sum of the intervals from $a$ to $c$ plus the sum from $c$ to $b$ exactly reproduces the sum from $a$ to $b$.  
   
————————————————————————————  
(c) Refinement invariance:  
If $P$ and $Q$ are two finite partitions of $[a,b]$ such that $f$ is piecewise constant with respect to both (i.e.\ constant on each subinterval of both partitions), then the p.c. integral yields the same sum.    
In other words, if we refine the partition $P$ to get a finer partition $Q$, the computed sums are identical.    
(This follows directly from the definition, since the function takes the same constant value over all sub-subintervals.)  
   
────────────────────────────────  
$\textbf{Summary:}$  
1. $\mathrm{p.c.}\int$ is linear.    
2. If $f\le g$, then $\mathrm{p.c.}\int f \le \mathrm{p.c.}\int g$ (monotonicity).    
3. $\mathrm{p.c.}\int$ is positive, additive over adjacent intervals, and independent of any subdivision refinements—properties mirroring those of the usual Riemann (and Lebesgue) integrals, but here proven more simply due to the piecewise constant setup.


### Upper, Lower Darboux integral

Below is a step‐by‐step explanation of how to define the upper and lower Darboux integrals for a bounded function on $[a,b]$, and how these definitions lead to the Darboux (Riemann–Darboux) integral.  
   
──────────────────────────────────  
1) Setup: Bounded Functions on a Closed Interval  
──────────────────────────────────  
   
Let $f\colon [a,b]\to \mathbb{R}$ be a bounded function. Being bounded means there is some $M>0$ such that $\lvert f(x)\rvert \le M$ for all $x\in [a,b]$. We wish to define the integral of $f$ over $[a,b]$ in the sense of Darboux.  
   
────────────────────────────────────  
2) Partitions of [a,b]  
─────────────────────────────────────  
   
A finite partition $P$ of the interval $[a,b]$ is a sequence of points  
$$  
P:\quad a = x_0 < x_1 < x_2 < \cdots < x_{n-1} < x_n = b.  
$$  
The subintervals determined by $P$ are  
$$  
[x_{k-1},\,x_k],  
\quad k=1,2,\ldots,n.  
$$  
We will write $\Delta_k = x_k - x_{k-1}$ for the length of the $k$-th subinterval.  
   
───────────────────────────────────────  
3) Upper and Lower Sums  
───────────────────────────────────────  
   
For a given partition $P$ of $[a,b]$ and a bounded function $f$, define:  
   
• On each subinterval $I_k := [x_{k-1},x_k]$, let  
  $$  
  M_k \;:=\; \sup_{x \in I_k}\,f(x),  
  \quad  
  m_k \;:=\; \inf_{x \in I_k}\,f(x).  
  $$  
  (Because $f$ is bounded, each of these suprema and infima is a finite real number.)  
   
• The upper Darboux sum of $f$ with respect to $P$ is  
  $$  
  U(P,f)  
  \;=\;  
  \sum_{k=1}^n M_k\,\Delta_k,  
  \quad\text{where}\quad \Delta_k = x_k \,-\, x_{k-1}.  
  $$  
• The lower Darboux sum of $f$ with respect to $P$ is  
  $$  
  L(P,f)  
  \;=\;  
  \sum_{k=1}^n m_k\,\Delta_k.  
  $$  
   
Geometrically, you can think of $U(P,f)$ as the total area of rectangles lying above the graph of $f$, with heights given by the supremum on each interval, while $L(P,f)$ is the total area of rectangles lying below the graph, with heights given by the infimum.  
   
───────────────────────────────  
4) Upper and Lower Darboux Integrals  
───────────────────────────────  
   
To incorporate the idea behind “infimum of upper sums” and “supremum of lower sums,” we define:  
   
• The upper Darboux integral:  
  $$  
  \overline{\int_a^b} f  
  \;:=\;  
  \inf_{P} \,U(P,f),  
  $$  
  where the infimum is taken over all finite partitions $P$ of $[a,b]$.  
   
• The lower Darboux integral:  
  $$  
  \underline{\int_a^b} f  
  \;:=\;  
  \sup_{P} \,L(P,f),  
  $$  
  where the supremum is taken over all finite partitions $P$ of $[a,b]$.  
   
Since every $L(P,f)$ must be at most every $U(Q,f)$ (for any partitions $P,Q$), it follows that  
$$  
\underline{\int_a^b} f  
\;\le\;  
\overline{\int_a^b} f.  
$$  
   
────────────────────────────────────  
5) Darboux (Riemann–Darboux) Integrable Functions  
───────────────────────────────────  
   
A function $f$ is said to be (Darboux) integrable on $[a,b]$ if and only if the upper and lower Darboux integrals coincide, viz.  
$$  
\underline{\int_a^b} f  
\;=\;  
\overline{\int_a^b} f.  
$$  
When this happens, we define the common value:  
$$  
\int_{a}^b f(x)\,dx  
\;:=\;  
\underline{\int_a^b} f  
\;=\;  
\overline{\int_a^b} f.  
$$  
This quantity $\int_{a}^b f(x)\,dx$ is called the (Darboux) integral of $f$ over $[a,b]$.  
   
Thus, the “Darboux integral” of $f$ is precisely the real number $I$ such that for every $\epsilon>0$, there is a partition $P$ of $[a,b]$ where the upper sum $U(P,f)$ and the lower sum $L(P,f)$ differ by less than $\epsilon$, i.e.  
$$  
U(P,f)\;-\;L(P,f)  
\;<\;  
\epsilon.  
$$  
   
────────────────────────────────  
6) Connection to “Piecewise Constant” Sums  
────────────────────────────────  
   
The logic of Darboux sums and the p.c. (piecewise constant) integrals share a similar approach:  
   
• In the piecewise constant scenario, one literally takes the function to be constant on each interval, hence the integral is just a sum of “height $\times$ width”.    
• In the Darboux approach, one uses suprema and infima of the function on each subinterval (rather than a single chosen value) and then refines partitions to home in on the actual integral.  
   
If a function is integrable in the Darboux sense, then there exist partitions on which the upper and lower sums are arbitrarily close; equivalently, one can approximate $f$ arbitrarily well by piecewise constant functions whose integrals match that of $f$.  
   
───────────────────────────  
Summary  
───────────────────────────────  
   
1) A partition $P:\,a=x_0<x_1<\dots<x_n=b$ is used to split $[a,b]$ into subintervals.    
2) For a bounded $f$, define:    
   – $M_k = \sup_{x\in[x_{k-1},x_k]} f(x)$,    
   – $m_k = \inf_{x\in[x_{k-1},x_k]} f(x)$.    
   Then    
   – Upper sum: $U(P,f)=\sum_{k=1}^n M_k(x_k-x_{k-1})$.    
   – Lower sum: $L(P,f)=\sum_{k=1}^n m_k(x_k-x_{k-1})$.    
3) The upper (resp.\ lower) Darboux integral is the infimum (resp.\ supremum) of $U(P,f)$ (resp.\ $L(P,f)$) over all partitions $P$.    
4) If these two “extreme” integrals coincide, that common value is taken to be $\int_a^b f$. This is the Darboux integral of $f$ over $[a,b]$. If they do not coincide, $f$ is not (Darboux) integrable.    
  
Hence, the Darboux integral is built out of the same conceptual approach as the piecewise constant integral, but allowing suprema and infima to capture “tightest” upper and lower approximations on each interval, yielding a criterion for integrability via the equality of these infimum/supremum sums.


### Riemann integral

Now, define Riemann integral of $f$ as before, using the ideas of a tagged partition of $[a \; \; b]$ and Riemann sums.

------------------------------------

Below is a short, step-by-step explanation of how to define the Riemann integral of a bounded function on $[a,b]$ using tagged partitions and Riemann sums. This builds on the earlier ideas of piecewise-constant integrals and Darboux sums, but now uses “tags” to evaluate $f$ at some chosen point in each subinterval.  
   
──────────────────────────────────  
1) Bounded Functions  
────────────────────────────────────  
   
Let $f:[a,b]\to \mathbb{R}$ be bounded. That is, there exists $M>0$ with $\lvert f(x)\rvert \le M$ for all $x \in [a,b]$.    
  
─────────────────────────────────────  
2) Partitions and Tagged Partitions  
────────────────────────────────────  
   
A finite partition $P$ of $[a,b]$ is given by    
$$  
P:\; a = x_0 < x_1 < \dots < x_n = b.  
$$    
We write the subintervals as    
$$  
I_k = [x_{k-1}, x_k],\quad k=1,\dots, n.  
$$  
   
A tagged partition is a partition $P$ together with a choice of a “tag” $\tau_k \in I_k$ (often one requires $\tau_k \in [x_{k-1}, x_k]$) for each $k$. Denote this by $(P,T)$, where $T = \{\tau_1,\dots,\tau_n\}$ with $\tau_k \in I_k$.  
   
────────────────────────────────────  
3) Riemann Sums  
─────────────────────────────────────  
   
Given a tagged partition $(P,T)$, we form the Riemann sum of $f$ as follows:  

$$  
S_f\bigl((P,T)\bigr)  
\;=\;  
\sum_{k=1}^n f(\tau_k)\,\bigl(x_k - x_{k-1}\bigr).  
$$  

Here:    
• $\tau_k$ is the chosen tag in the subinterval $[x_{k-1},x_k]$.    
• $x_k - x_{k-1}$ is the length of that subinterval.    
  
Intuitively, each term $f(\tau_k)\,(x_k - x_{k-1})$ represents the area of a rectangle of base $[x_{k-1}, x_k]$ and height given by the function value at the tag.  
   
────────────────────────────────────  
4) Mesh (Norm) of a Partition  
────────────────────────────────────  
   
The mesh (or norm) of a partition $P$ is the length of the largest subinterval in $P$:    

$$  
\|P\|  
\;=\;  
\max\{\,x_k - x_{k-1} \,\colon\, k=1,\dots,n\}.  
$$  

When we make $\|P\|$ very small, it means we are “refining” the partition to get many small subintervals.  
   
───────────────────────────────────────  
5) Definition of the Riemann Integral  
────────────────────────────────────────  
   
We say $f$ is Riemann integrable on $[a,b]$ if there exists a number $L \in \mathbb{R}$ such that for every $\varepsilon>0$, there is a $\delta>0$ with the following property:  
   
• For any tagged partition $(P,T)$ of $[a,b]$ whose mesh $\|P\|$ is less than $\delta$, we have  

  $$  
  \Bigl\lvert\, S_f\bigl((P,T)\bigr) \;-\; L\,\Bigr\rvert  
  \;<\;  
  \varepsilon.  
  $$  
   
If such an $L$ exists, then we say $f$ is (Riemann) integrable on $[a,b]$, and we write  

$$  
\int_a^b f(x)\,dx  
\;=\;  
L.  
$$  

Equivalently, one says that $\int_a^b f(x)\,dx$ is the limit of the Riemann sums $S_f((P,T))$ as the mesh of the partition goes to zero.  
   
─────────────────────────────────  
6) Why This Matches Darboux and Piecewise Constant Ideas  
─────────────────────────────────  
   
• If the function is integrable in the Riemann sense, one can show that the upper and lower Darboux integrals coincide (and vice versa). Hence, the Riemann integral is the same as the Darboux integral.    
• In many elementary cases (e.g.\ step functions, continuous functions on $[a,b]$), one explicitly sees that as partitions get finer, the Riemann sums approach a unique limit and agree with the area under the curve.    
• The piecewise constant (p.c.) integrals are precisely the special case where each Riemann sum is formed by choosing exactly the constant value of $f$ on each subinterval. That leads to the same concept of “area under the graph,” now formalized by taking finer partitions and letting the mesh go to zero.  
   
──────────────────────────────  
Summary  
─────────────────────────────────  
   
1. A tagged partition $(P,T)$ of $[a,b]$ consists of a partition $P$ and a choice of tags $\tau_k$ in each subinterval.    
2. The Riemann sum is $\sum_{k=1}^n f(\tau_k)(x_k-x_{k-1})$.    
3. As the mesh of $(P,T)$ goes to zero, if all these Riemann sums converge to the same real number $L$, then we say $f$ is Riemann integrable and define $\int_a^b f=L$.    
4. This Riemann integral is consistent with the Darboux approach and the piecewise constant integrals, tying all viewpoints together.


# Riemann and Darboux in $R^d$

Thus far we have dealt with the situation where $f: [a \; \; b] \to R$. When we have the case $f: U \to R$ where $U \subset R^d$ and $U$ is bounded, how to extend the ideas of Darboux and Riemann integrals that we discussed thus far in one dimension.

------------------------------------

$$  
\textbf{Extending Darboux and Riemann Integrals from 1D to Higher Dimensions}  
$$  
   
When we move from a function $f: [a,b] \to \mathbb{R}$ in one dimension to a function $f : U \to \mathbb{R}$ with $U \subset \mathbb{R}^d$ bounded, the core ideas—subdivision of the domain, infimum/supremum for Darboux sums, and sample‐point (“tagged”) sums for Riemann sums—remain the same. The main difference is that we now partition a region in $\mathbb{R}^d$ into small “boxes” (or “subrectangles”) instead of small intervals. Below is a concise overview.  
   
──────────────────────────  
1) Setup: A Bounded Domain in ℝᵈ  
──────────────────────────  
   
• Let $U \subset \mathbb{R}^d$ be bounded. That means there is a large rectangle    

  $$  
  R \;=\; [a_1, b_1]\times [a_2, b_2]\times \cdots \times [a_d, b_d]  
  $$  

  such that $U \subset R$.    
• Assume $f : U \to \mathbb{R}$ is bounded on $U$; that is, there exists $M>0$ with $\lvert f(x)\rvert \le M$ for all $x\in U$.  
   
Often, one extends $f$ by zero (or any convenient value) outside $U$ so that it is defined on all of $R$, but equals the original $f$ on $U$.  In that way, we only need partitions of $R$ rather than partitions “just of $U$.”  
   
──────────────────────
1) Partitions into Boxes  
───────────────────────  
   
A finite partition $P$ of the bounding box $R$ is given by choosing finitely many subdivision points in each coordinate direction.  Concretely, one picks  

$$  
a_i \;=\; x_{i,0} < x_{i,1} < \cdots < x_{i,n_i} \;=\; b_i  
\quad (i=1,\dots, d),  
$$  

and takes all products

$$  
B_{j_1,j_2,\ldots,j_d}  
\;=\;  
[x_{1,j_1-1},x_{1,j_1}]  
\times  
[x_{2,j_2-1},x_{2,j_2}]  
\times \cdots \times  
[x_{d,j_d-1},x_{d,j_d}],  
$$  

where $1 \le j_i \le n_i$.  Each such set $B$ is a $d$-dimensional “box.”  The union of all these boxes covers $R$, so in particular covers $U\subset R$.  
   
────────────────────────────  
3) Extending the Darboux Integral to ℝᵈ  
─────────────────────────────  
   
To define “upper” and “lower” sums in higher dimensions, we do essentially what we did in 1D, but on each box $B$:  
   
1. For each box $B$ in the partition $P$, consider the portion of $B$ that lies in $U$, namely $B \cap U$.    
2. Define    
   
   $$  
   M_B \;=\; \sup_{x \in B \cap U} f(x),  
   \qquad  
   m_B \;=\; \inf_{x \in B \cap U} f(x).  
   $$  

   (If $B \cap U$ is empty, one often takes $M_B = 0$ and $m_B = 0$ or simply omits that box from the sums.)  
   
3. Let $\mathrm{vol}(B)$ be the $d$-dimensional volume of the box $B$. Then define the upper and lower Darboux sums:  

   $$  
   U(P,f)  
   \;=\;  
   \sum_{B \in P} M_B \,\mathrm{vol}(B),  
   \quad  
   L(P,f)  
   \;=\;  
   \sum_{B \in P} m_B \,\mathrm{vol}(B).  
   $$  
   
4. As in the 1D case, the upper Darboux integral is  

   $$  
   \overline{\int_U} f  
   \;=\;  
   \inf_P\, U(P,f),  
   $$  
   and the lower Darboux integral is  
   $$  
   \underline{\int_U} f  
   \;=\;  
   \sup_P\, L(P,f),  
   $$  

   with both infimum and supremum taken over all possible partitions of $R$.    
  
5. If these two quantities coincide, we say $f$ is Darboux integrable on $U$ and define 
    
   $$  
   \int_U f  
   \;=\;  
   \underline{\int_U} f  
   \;=\;  
   \overline{\int_U} f.  
   $$  
   
This generalizes the one‐dimensional idea (sums of “suprema × subinterval length” vs. “infima × subinterval length”) to sums of “suprema × box volume” vs. “infima × box volume.”  
   
────────────────────────────────  
1) Extending the Riemann Integral via Tagged Partitions  
────────────────────────────────  
   
Similarly, for the Riemann integral in $\mathbb{R}^d$, we define a “tagged partition” of $R$:  
   
1. First form a partition $P$ of $R$ into finitely many boxes $B_1,B_2,\dots,B_N$.    
2. In each box $B_j$, choose a “tag” (a sample point) $\tau_j \in B_j \cap U$.    
3. The Riemann sum of $f$ relative to $(P,T)$ is  

   $$  
   S_f\bigl((P,T)\bigr)  
   \;=\;  
   \sum_{j=1}^N f(\tau_j)\,\mathrm{vol}(B_j).  
   $$  
   If $B_j \cap U = \emptyset$, one sets that term to 0 or omits it.  
   
4. The mesh (norm) of $P$ is the maximum of the side‐lengths of the boxes in $P$. Taking finer and finer partitions shrinks this maximum side‐length to 0.  
   
We say $f$ is (Riemann) integrable on $U\subset \mathbb{R}^d$ if there is a real number $L$ such that for every $\varepsilon>0$, one can make the mesh of the partition small enough so that all corresponding Riemann sums stay within $\varepsilon$ of $L$. Symbolically:  

$$  
\forall \varepsilon>0,\;\exists\delta>0:  
\quad  
\|P\|<\delta  
\;\Longrightarrow\;  
\bigl|\,S_f((P,T)) - L\bigr|  
< \varepsilon.  
$$  
   
If this limit $L$ exists (independent of the choices of the tags $\tau_j$), then we define 

$$  
\int_U f  
\;=\;  
L.  
$$  
   
─────────────────────────────────  
5) Equivalence of the Two Definitions  
─────────────────────────────────────  
   
In one dimension, we know that the Darboux and Riemann definitions coincide. The same holds in $\mathbb{R}^d$: a bounded function $f$ on a bounded region $U\subset \mathbb{R}^d$ is Darboux integrable if and only if it is Riemann integrable, and in that case the two integrals agree.  
   
One often refers to both as the “Riemann–Darboux integral.”  
   
──────────────────────────────────  
Summary  
───────────────────────────────────  
   
1. To extend 1D Darboux integrals, we cover $U\subset \mathbb{R}^d$ with a grid of small boxes, take infimums and supremums of $f$ on each box (restricted to $U$), form lower and upper sums, then let the partition get arbitrarily fine.    
2. To extend 1D Riemann integrals, we do exactly what we did in one dimension but in multi‐dimensional boxes: pick a sample (“tag”) in each box to evaluate $f$, multiply by the box’s volume, and sum.  Refining partitions and requiring the sums to converge yields the Riemann integral.    
3. Both methods agree, provided $f$ is integrable in the sense that the upper and lower sums converge to the same limit (Darboux) or that all Riemann sums converge to the same value (Riemann).    
  
Hence, the key 1D ideas—partitioning the domain, taking sup/inf or sample‐point evaluations, and letting the partition mesh go to zero—carry over verbatim, just using boxes and volume in place of intervals and length.



## Lebesgue Outer measure

The Jordan outer measure which we shall now show as $\mu^{*J}$ to distinguish from the Lebesgue outer measure $\mu^*$ from hereon. For a set $E \subset R^d$, 

$$
\mu^{*J} = \inf_{E \supset B, B \; \text{elementary}} \mu^J(B)
$$

Equivalently, we can replace the elementary $B$ above with a finite union of boxes $B_1 \cup \cdots B_n$. The infimum over the finite partition of boxes of $\sum_i \text{vol}(B_i)$.

By replacing the finite cover of boxes to a countably infinite cover of boxes, we pass from the Jordan outer measure to the Lebesgue outer measure.

Is this correct?

--------------------------------------------------

Below is a brief clarification of how the transition from “finite coverings by boxes” to “countably infinite coverings by boxes” leads from Jordan’s notion of outer measure to the Lebesgue outer measure:  
   
────────────────────────────────────────────────────────────────────────────  
1) Jordan Outer Measure (Finite Covers)  
────────────────────────────────────────────────────────────────────────────  
   
• For a bounded set $E \subset \mathbb{R}^d$, the Jordan outer measure $\mu^{*J}(E)$ is defined by 

  $$  
  \mu^{*J}(E)  
  \;=\;  
  \inf\Bigl \\{  
  \mu^J(B)  
  \,\Big|\,  
  B \supset E, \,B \text{ is an elementary set (finite union of boxes)}  
  \Bigr \\}.  
  $$    

  In practice, we usually take $B = B_1 \cup \cdots \cup B_n$, a finite union of boxes whose (Jordan) volume is    
  $\mu^J(B) = \sum_{i=1}^n \mathrm{vol}(B_i).$  
   
• Thus, to find $\mu^{*J}(E)$, we look at all possible finite covers of $E$ by boxes $B_1,\dots,B_n$ and take the infimum of the sum of their volumes.  
   
─────────────────────────────────────  
2) Lebesgue Outer Measure (Countable Covers)  
────────────────────────────────────  
   
• The Lebesgue outer measure $\mu^*(E)$ allows covering $E$ by *countably many* boxes:  

  $$  
  \mu^*(E)  
  \;=\;  
  \inf\Bigl\\{  
  \sum_{i=1}^{\infty} \mathrm{vol}(I_i)  
  \,\Big|\,  
  E\subset \bigcup_{i=1}^\infty I_i,  
  \ I_i \text{ are boxes}  
  \Bigr\\}.  
  $$  

• Comparing the two:    
  – Jordan outer measure restricts to $*finite*$ covers by boxes.    
  – Lebesgue outer measure allows $*countable*$ covers by boxes, hence is generally “less restrictive” (which in turn can yield a smaller infimum—i.e.\ $\mu^*(E)\le\mu^{*J}(E)$ in most situations).  
   
─────────────────────────  
3) Is the Statement “By Replacing Finite Covers by Countably Many Covers   
   We Pass from Jordan to Lebesgue Outer Measure” Correct?  
──────────────────────────  
   
Yes. In essence, the definition of Jordan outer measure is exactly like that of the Lebesgue outer measure except it limits itself to $*finite*$ families of boxes. The Lebesgue outer measure extends this by allowing $*countably infinite*$ families of boxes. Concretely:  
   
• Jordan outer measure:    

  $$  
  \mu^{*J}(E)  
  \;=\;  
  \inf_{\substack{E \subset \bigcup_{i=1}^n B_i \\ n<\infty}} \,  
  \sum_{i=1}^n \mathrm{vol}(B_i).  
  $$  

• Lebesgue outer measure:  

  $$  
  \mu^*(E)  
  \;=\;  
  \inf_{\substack{E \subset \bigcup_{i=1}^\infty B_i \\ \text{countable}}} \,  
  \sum_{i=1}^\infty \mathrm{vol}(B_i).  
  $$  
   
Thus, allowing infinite covers strictly generalizes the finite‐cover definition, moving from $\mu^{*J}$ to $\mu^*$. Indeed, any set that can be covered by a finite collection can also be covered by the same set written as a countably infinite collection (just pad with empty sets), so   

$$  
\mu^*(E) \;\le\; \mu^{*J}(E).  
$$  

Hence the statement that “by passing from finite to countably infinite covers, we move from Jordan outer measure to Lebesgue outer measure” is precisely correct.  
   
────────────────────────────  
4) Additional Note: Existence vs. Finiteness of the Jordan Measure  
────────────────────────────  
   
• Jordan measure (as opposed to Jordan $*outer*$ measure) is only defined for a restricted class of sets (“Jordan measurable” sets), basically those whose boundaries have measure zero and are bounded.    
• Lebesgue measure, on the other hand, is well‐defined (possibly infinite) for *every* subset of $\mathbb{R}^d$.    
  
Thus, the finite‐cover versus countably‐cover dichotomy reflects the broader fact that Lebesgue theory is strictly more general than Jordan’s, while coinciding for sets that are nicely “Jordan measurable.”  
   
────────────────────────────────────  
Conclusion  
───────────────────────────────────  
   
Yes, the succinct statement is correct:    
“By replacing finite box‐covers with countably infinite box‐covers in the definition, one passes from the Jordan outer measure $\mu^{*J}$ to the Lebesgue outer measure $\mu^*$.”


## Compare Jordan and Lebesgue outer measures on countable sets

Let $E = \{x_1, x_2, \cdots \} \in R^d$ be a countable set. The Jordan outer measure $\mu^{* (J)}(E)$ can be large and in some cases infinite while the Lebesgue outer measure $\mu^*(E)$ is zero. Prove this.

--------------------------------

Explanation in steps:  
   
────────────────────────────  
1) Setup and Notation  
────────────────────────────  
   
Let $E = \{x_1, x_2, \dots\}\subset \mathbb{R}^d$ be a countably infinite set. We compare:  
   
• The Jordan outer measure $\mu^{*(J)}(E)$, which uses only finite covers by boxes.    
• The Lebesgue outer measure $\mu^*(E)$, which uses countable covers by boxes.  
   
Recall:  
   
1. Jordan outer measure:  
   
   $$  
   \mu^{*(J)}(E)  
   \;=\;  
   \inf\Bigl\\{  
   \sum_{i=1}^n \mathrm{vol}(B_i)  
   \;\Big|\;  
   E\;\subset\; \bigcup_{i=1}^n B_i,\,  
   B_i \text{ are (closed/open) boxes},\,n<\infty  
   \Bigr\\}.  
   $$  
   
2. Lebesgue outer measure:  
   
   $$  
   \mu^*(E)  
   \;=\;  
   \inf\Bigl\\{  
   \sum_{i=1}^\infty  
   \mathrm{vol}(B_i)  
   \;\Big|\;  
   E\;\subset\; \bigcup_{i=1}^\infty B_i,\,  
   B_i \text{ are boxes}  
   \Bigr\\}.  
   $$  
   
Below we prove two statements:  
   
(1) $\mu^*(E)=0$ for every countable set $E$.    
(2) $\mu^{*(J)}(E)$ can be arbitrarily large (or even infinite), depending on how $E$ is “spread out,” in particular if $E$ has limit points or is dense in some region.  
   
──────────────────────────────  
1) Proof That Lebesgue Outer Measure of a Countable Set Is Zero  
───────────────────────────────  
   
To show $\mu^*(E)=0$ for any countable $E\subset \mathbb{R}^d$:  
   
• Enumerate the points of $E$ as $x_1, x_2,\dots$.    
• For each $i=1,2,\dots$, choose a little box $B_i$ around $x_i$ of volume at most $\tfrac{\varepsilon}{2^i}$.    
  
Then $E\subset \bigcup_{i=1}^\infty B_i$ and the total volume is

$$  
\sum_{i=1}^\infty  
\mathrm{vol}(B_i)  
\;\le\;  
\sum_{i=1}^\infty \frac{\varepsilon}{2^i}  
\;=\;  
\varepsilon.  
$$  

Since $\varepsilon>0$ was arbitrary, the infimum of such sums is $0$. Thus  

$$  
\mu^*(E) \;=\; 0.  
$$  
   
In other words, any countable set has Lebesgue outer measure $0$.  
   
───────────────────────────────  
3) Example Where the Jordan Outer Measure Is “Large” or Infinite  
──────────────────────────────  
   
While the Lebesgue outer measure of a countable set in $\mathbb{R}^d$ is always zero, the Jordan outer measure can fail to be small (or even finite) if one insists on *finite covers*. A standard illustration is:  
   
• Let $E=[0,1]\cap \mathbb{Q}$ be the set of rational points in the unit interval in $\mathbb{R}$.    
• It is a countable set, so $\mu^*(E)=0$.    
  
However, to cover *all* rational points in $[0,1]$ with a *finite* union of intervals, one is effectively forced to cover *every* subinterval of $[0,1]$. Indeed, if you leave out any subinterval, that subinterval contains a rational point not covered—a contradiction. Thus, the only successful finite cover of all rationals in $[0,1]$ necessarily covers $[0,1]$ entirely, giving:  
   
$$  
\mu^{*(J)}(E)  
\;=\;  
\mu^{*(J)}\bigl([0,1]\cap\mathbb{Q}\bigr)  
\;=\;  
\mathrm{vol}\bigl([0,1]\bigr)  
\;=\;  
1.  
$$  

Hence, for this countable set $\mu^{*(J)}(E)=1$, contrasting with $\mu^*(E)=0$.  
   
More generally, any countable set $E$ that is dense in some region $\Omega\subset \mathbb{R}^d$ forces any finite family of boxes covering $E$ to cover all of $\Omega$. Because $\mathrm{vol}(\Omega)$ might be positive (or unbounded), $\mu^{*(J)}(E)$ can be as large as $\mathrm{vol}(\Omega)$ or even infinite.  
   
──────────────────────────────  
4) Summary  
──────────────────────────────  
   
1. For any countable $E \subset \mathbb{R}^d$, its Lebesgue outer measure is always zero: $\mu^*(E)=0$.    
2. The Jordan outer measure $\mu^{*(J)}(E)$, which only allows *finite* covers by boxes, can be positive or even infinite for some countable sets (e.g.\ dense sets within a region).    
   – A classic example: the rationals in $[0,1]$. They have $\mu^*\bigl(\mathbb{Q}\cap[0,1]\bigr)=0$ but $\mu^{*(J)}\bigl(\mathbb{Q}\cap[0,1]\bigr)=1$.    
  
This illustrates the fundamental difference between these two outer measures and why the Jordan measure, in general, applies only to “nice” (Jordan measurable) sets, whereas Lebesgue measure extends to all sets in a more refined manner.


## Lebesgue measurability

Let $E \subset R^d$. Let $\mu^*(E)$ be the outer measure of $E$. Let $U \subset R^d$ be an open set such that for any $\varepsilon > 0$, there is an open set $U \subset R^d$ such that $\mu^*(U \setminus E) \leq \varepsilon$. Then $E$ is said to be Lebesgue measurable. 

This can be used as a definition of Lebesgue measurability. This construction avoids using the Caratheodory criterion. What do you think?

--------------------------------

First, let us restate the proposed definition in a more standard way:  
   
Definition (Via Approximation by Open Sets).    
A set $E \subset \mathbb{R}^d$ is called Lebesgue measurable if, for every $\varepsilon > 0$, there exists an open set $U \subset \mathbb{R}^d$ such that  

$$  
E \;\subset\; U  
\quad\text{and}\quad  
\mu^*\bigl(U \setminus E\bigr) \;\le\; \varepsilon,  
$$  

where $\mu^*(\cdot)$ denotes the Lebesgue outer measure.  
   
Below is a step-by-step outline explaining why this indeed provides a valid definition of Lebesgue measurability, and how it relates to the usual Carathéodory criterion.  
   
--------------------------------  
   
1) Carathéodory's Criterion (Classical Definition)  
   
Usually, one introduces the outer measure $\mu^*(\cdot)$ on all subsets of $\mathbb{R}^d$ via coverings by countable collections of boxes (or open sets). Then, one defines:  
   
Carathéodory's Criterion.    
A set $E \subset \mathbb{R}^d$ is Lebesgue measurable if and only if, for every set $A \subset \mathbb{R}^d$,  

$$  
\mu^*(A)   
\;=\;   
\mu^*\bigl(A \cap E\bigr) \;+\; \mu^*\bigl(A \cap E^c\bigr).  
$$  
   
It can be shown that sets satisfying this criterion form a $\sigma$-algebra, and the restriction of $\mu^*$ to these sets is indeed the Lebesgue measure.  
   
--------------------------------------  
   
2) Equivalence with Approximation by Open Sets  
   
An equivalent way to say that $E$ is Lebesgue measurable is:  
   
  For every $\varepsilon > 0$, one can find an open set $U \supset E$ whose “difference” from $E$ has arbitrarily small outer measure, i.e.,  
  
  $$  
  \mu^*\bigl(U \setminus E\bigr) \;\le\; \varepsilon.  
  $$  
   
Intuitively, this means $E$ can be “expanded” slightly to an open set $U$ without changing its outer measure by more than $\varepsilon$. One then shows that this is equivalent to Carathéodory’s condition. The main steps are:  
   
(a) If $E$ satisfies Carathéodory’s criterion, one uses the regularity property of Lebesgue measure (or outer measure) to approximate $E$ from above by open sets of outer measure arbitrarily close to $\mu^*(E)$. One obtains 

$$  
\mu^*\bigl(U \setminus E\bigr)   
\,=\,   
\mu^*(U) \,-\, \mu^*\bigl(U \cap E^c\bigr)   
\,\approx\,   
\mu^*(E) \,-\, \mu^*(E)   
\,=\,   
0,  
$$  

for a suitably chosen $U\supset E$. By carefully optimizing these choices, one forces $\mu^*((U\setminus E)$ to be less than $\varepsilon$.  
   
(b) Conversely, if for every $\varepsilon>0$ you can cover $E$ by an open set $U$ with $\mu^*(U\setminus E)\le\varepsilon$, then one shows by a set-containment argument (plus subadditivity and other properties of $\mu^*$) that Carathéodory’s splitting condition  

$$  
\mu^*(A)   
\,=\,   
\mu^*\bigl(A \cap E\bigr) \;+\; \mu^*\bigl(A \cap E^c\bigr)  
$$  

also holds. Essentially, given a set $A$, one approximates $A\cap E$ by $(A\cap U)$ and notes that the difference in measure can be chosen to be arbitrarily small.  
   
Thus, the approximation-by-open-sets condition and the Carathéodory criterion are logically equivalent.  
   
----------------------------------  
   
1) Practical and Conceptual Advantages  
   
Using “approximation by open sets” (together with “approximation by closed sets” from below if needed) is particularly natural once one knows:  
   
• The regularity of Lebesgue measure: every Lebesgue measurable set can be approximated from above by open sets and from below by closed sets in terms of measure.  
   
• The Borel $\sigma$-algebra and its completion: one can first define Lebesgue measure on all Borel sets (as an extension of the usual notion of volume) and then extend to all subsets of measure-zero modifications of Borel sets. In this viewpoint, saying “$E$ is contained in an open set $U$ with $U\setminus E$ small in outer measure” is a natural statement about how close $E$ is to a Borel set (indeed $U$ is Borel).  
   
Hence, many texts prefer Carathéodory’s definition as the starting axiom for measure extension, while others introduce Lebesgue measure on the Borel sets first and then define a set to be (Lebesgue) measurable if it differs from a Borel set by a set of measure zero. One then proves that these extended measurable sets are exactly those that can be approximated from above by open sets in outer measure.  
   
--------------------------------  
   
4) Conclusion  
   
Yes, one can take “for every $\varepsilon>0$, there is an open set $U\supset E$ with $\mu^*(U\setminus E)\le \varepsilon$” as a perfectly valid definition of Lebesgue measurability. It is indeed equivalent to the usual Carathéodory criterion:  
   
• The approximation-by-open-sets property ↔ Carathéodory’s splitting condition.  
   
This definition avoids directly invoking Carathéodory’s criterion, but in the background, a similar argument is used to show equivalence (by leveraging outer measure properties, subadditivity, and the structure of open/closed sets). Hence, from a purely logical standpoint, it is a sound and commonly known alternative approach to defining Lebesgue measurability.


## Properties of Lebesgue Outer measure

What are the properties of the Lebesgue outer measure $\mu^*(\cdot)$ which is defined using the construction of the infimum of sum of the volumes of a countable cover of boxes?

-------------------------------------------

Below is a step-by-step overview of the fundamental properties of the Lebesgue outer measure, denoted by $\mu^*(\cdot)$, which is defined by covering a set with countably many boxes (or intervals/rectangles in $\mathbb{R}^d$) and taking the infimum of the total volumes of those boxes.  
   
--------------------------------------------------------------------------------  
   
1) Construction of the Lebesgue Outer Measure  
   
Let $E \subset \mathbb{R}^d$. We define    

$$  
\mu^*(E)  
\;=\;  
\inf   
\left\{  
\sum_{k=1}^\infty \ell\bigl(I_k\bigr)   
:\,  
E \,\subset\, \bigcup_{k=1}^\infty I_k,  
\ \text{where each } I_k \text{ is a (closed or open) box in } \mathbb{R}^d  
\right\},  
$$  

where $\ell(I_k)$ denotes the usual $d$-dimensional volume (length, area, etc.) of the box $I_k$.  
   
--------------------------------------------------------------------------------  
   
2) Monotonicity  
   
The outer measure $\mu^*$ is monotonically increasing, meaning:  
   
$$  
A \,\subset\, B  
\quad\Longrightarrow\quad  
\mu^*(A) \;\le\; \mu^*(B).  
$$  
   
Reasoning:    
• If $A \subset B$, then any countable collection of boxes covering $B$ also covers $A$.    
• Therefore, the infimum of sums of volumes needed to cover $A$ cannot exceed that needed to cover $B$.    
  
---------------------------------------  
   
3) Countable Subadditivity (or Subadditivity in General)  
   
The outer measure $\mu^*$ is countably subadditive, meaning:  
   
$$  
\mu^*\!\Bigl(\bigcup_{k=1}^\infty E_k\Bigr)  
\;\le\;  
\sum_{k=1}^\infty \mu^*(E_k).  
$$  
   
Reasoning:    
• Given countably many sets $E_k$, for each $k$ choose a cover by boxes $\{I_{k,j}\}_{j=1}^\infty$ such that    

  $$  
  E_k \,\subset\, \bigcup_{j=1}^\infty I_{k,j}  
  \quad\text{and}\quad  
  \sum_{j=1}^\infty \ell(I_{k,j})  
  \;<\;  
  \mu^*(E_k) + \frac{\varepsilon}{2^k},  
  $$  

  for some small $\varepsilon>0$.    
• Then    

  $$  
  \bigcup_{k=1}^\infty E_k  
  \;\subset\;  
  \bigcup_{k=1}^\infty\bigcup_{j=1}^\infty I_{k,j},  
  $$  

  and the total volume of that cover is 

$$  
  \sum_{k=1}^\infty \sum_{j=1}^\infty \ell(I_{k,j})  
  \;\le\;  
  \sum_{k=1}^\infty  
  \Bigl (  
     \mu^*(E_k) + \tfrac{\varepsilon}{2^k}  
  \Bigr )  
  \;=\;  
  \varepsilon + \sum_{k=1}^\infty \mu^*(E_k).  
  $$  

• Taking the infimum over all such choices and letting $\varepsilon\to 0$ implies the result.  
   
------------------------------------  
   
4) Translation Invariance  
   
For any $E \subset \mathbb{R}^d$ and any $x \in \mathbb{R}^d$, define    

$$  
E + x   
\;=\;   
\{\,y + x \,:\, y \in E \}.  
$$  
   
Then,  
   
$$  
\mu^*(E + x)  
\;=\;  
\mu^*(E).  
$$  
   
Reasoning:    
• Translating a cover of $E$ by $x$ gives a cover of $E + x$ with the same total volume, and vice versa.    
• Hence the infimum of volumes that cover $E$ is the same as that for $E+x$.  
   
---------------------------------------------  
   
5) Consistency with Volume on Boxes  
   
By definition, if $I$ is a box in $\mathbb{R}^d$ with sides of lengths $a_1, a_2, \dots, a_d$, then  
   
$$  
\mu^*(I)   
\;=\;  
\ell(I)  
\;=\;  
a_1 \times a_2 \times \cdots \times a_d,  
$$  
   
i.e., the outer measure agrees with the usual notion of the volume of a box.  
   
---------------------------------------  
   
6) Non-Negativity and Null Set for the Empty Set  
   
• Non-negativity:    
  $\displaystyle \mu^*(E) \;\ge\; 0$ for all $E \subset \mathbb{R}^d$.    
  
• Measure of the empty set:    
  $\displaystyle \mu^*(\varnothing) = 0$.    
  
These follow directly from the definition, as covering $\varnothing$ requires no boxes.  
   
------------------------------------------  
   
7) Additional Remarks on Completeness and Extension  
   
• Once one identifies the collection of Lebesgue measurable sets via Carathéodory’s criterion (or the open-set-approximation criterion), one restricts $\mu^*$ to that $\sigma$-algebra.    
• This yields a complete measure space: any subset of a $\mu^*$-null set (i.e., a set of outer measure zero) is also measurable and has measure zero.  
   
-------------------------------------------------  
   
Summary of Key Properties  
   
1) Monotonicity: If $A \subset B$, then $\mu^*(A) \le \mu^*(B)$.    
2) Countable Subadditivity: $\mu^*\bigl(\bigcup_{k=1}^\infty E_k\bigr) \le \sum_{k=1}^\infty \mu^*(E_k)$.    
3) Translation Invariance: $\mu^*(E + x) = \mu^*(E)$ for all $x \in \mathbb{R}^d$.    
4) Agreement with Volume: For any box $I$, $\mu^*(I)$ equals the usual volume of $I$.    
5) Non-negativity and $\mu^*(\varnothing)=0$.    
  
These properties are the backbone for constructing and studying Lebesgue measure on $\mathbb{R}^d$.


## $\varepsilon/2^n$ trick

***What is the $\varepsilon / 2^n$ trick in the context of proving results regarding Lebesgue measures.  It comes up when the set in question is covered by boxes in $R^d$***


In proofs involving Lebesgue measure (or outer measure) in 
$\mathbb{R}^d$, one often wants to cover a given set $E$ by a collection of boxes (rectangles) whose total volume can be made arbitrarily small (or arbitrarily close to some target number). The “$\varepsilon/2^n$ trick” (also sometimes called the “halving trick”) is a systematic way to achieve this in countably many steps, so that the total “error” or total “excess volume” remains below a chosen $\varepsilon$. Below is an outline of how and why it works.  
   
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
1) The usual difficulty and the core idea  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
   
● Difficulty:    
  Suppose you want a single cover of $E$ by finitely or countably many boxes whose total volume is no more than (say) $\mu^*(E) + \varepsilon$. However, the process of covering $E$ might naturally happen in multiple stages (e.g., successively covering “leftover” parts of $E$ that were missed by earlier steps).    
  
● Core Idea (“Halving” the $\varepsilon$ each time):    
  Rather than trying to ensure at each intermediate step that the error is smaller than the same $\varepsilon$, we allow ourselves smaller and smaller fractions of $\varepsilon$, specifically $\frac{\varepsilon}{2}, \frac{\varepsilon}{4}, \frac{\varepsilon}{8},\dots$. In the end, the sum of all these fractions is still at most $\varepsilon$.  
   
Mathematically, if you do something “wrong” (or “use up some measure”) by at most $\frac{\varepsilon}{2}$ at the first step, then at most $\frac{\varepsilon}{4}$ at the second step, etc., the total over infinitely many steps is  
$$  
\frac{\varepsilon}{2} \;+\; \frac{\varepsilon}{4} \;+\; \frac{\varepsilon}{8} \;+\; \dots   
\;=\; \varepsilon.  
$$  
Hence, you never exceed your overall error budget $\varepsilon$.  
   
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
2) A common scenario in measure theory  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
   
A prototypical place the $\varepsilon/2^n$ trick appears is in showing that the Lebesgue outer measure $\mu^*(E)$ can be approximated arbitrarily closely by covers of $E$ by boxes in $\mathbb{R}^d$. For instance:  
   
◾ You know that    

$$  
\mu^*(E) \;=\; \inf\Bigl\{\,\sum_{i} \mathrm{vol}(R_i) \;\colon\; E\subseteq\bigcup_i R_i,\ R_i\text{ are boxes}\Bigr\}.  
$$  
   
◾ You want to show there is, in fact, a single (finite or countable) cover by boxes whose total volume is $ < \mu^*(E) + \varepsilon$.    
  
Because the outer measure is defined via an infimum, you do not automatically have a single cover attains that infimum. Instead, you construct a sequence of near-optimal covers, each stage improving the total volume by at most $\varepsilon/2^n$. Summing up all these small improvements gives you one final cover whose total volume is within $\varepsilon$ of the infimum.  
   
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
3) Typical step-by-step application  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
   
Here is how one often applies the $\varepsilon/2^n$ strategy in detail:  
   
1. Start with your desired total “error budget” $\varepsilon>0$.    
  
2. Because $\mu^*(E)$ is an infimum over covers, for the first stage (say $n=1$), you can find a countable (or finite) collection of boxes $\{R_i^{(1)}\}$ covering $E$ such that  
   $$  
   \sum_i \mathrm{vol}\bigl(R_i^{(1)}\bigr)  
   \;\le\;   
   \mu^*(E)\;+\;\frac{\varepsilon}{2}.  
   $$  
   
3. Now, maybe you still want to refine something about this cover further—e.g., remove redundant boxes, or handle boundary issues, or cover only leftover uncovered parts of $E$. You allow yourself an additional $\tfrac{\varepsilon}{4}$ “volume budget” to fix those issues. Concretely, you produce a second collection of boxes $\{R_i^{(2)}\}$ such that  
   $$  
   \sum_i \mathrm{vol}\bigl(R_i^{(2)}\bigr)   
   \;\le\;  
   \bigl[\mu^*(E) + \tfrac{\varepsilon}{2}\bigr]\;+\;\tfrac{\varepsilon}{4}.  
   $$  
   
4. If you repeat such a procedure at the $n$-th step, you might have a new cover $\{R_i^{(n)}\}$ whose total volume is  
   $$  
   \sum_i \mathrm{vol}\bigl(R_i^{(n)}\bigr)  
   \;\le\;  
   \mu^*(E)  
   \;+\;  
   \frac{\varepsilon}{2} + \frac{\varepsilon}{4} + \cdots + \frac{\varepsilon}{2^n}.  
   $$  
   
5. Since  
   $$  
   \frac{\varepsilon}{2} \;+\; \frac{\varepsilon}{4} \;+\;\cdots \;+\;\frac{\varepsilon}{2^n}  
   \;=\;  
   \varepsilon\Bigl(1-\frac{1}{2^n}\Bigr)  
   \;\to\;  
   \varepsilon   
   \quad  
   \text{as }n\to\infty,  
   $$  
   in the limit, you end up with a cover with total volume at most $\mu^*(E) + \varepsilon$.    
  
6. You can then combine all those boxes from your final stage (or union them if needed), so that the total volume is still within $\varepsilon$ of the infimum $\mu^*(E)$.    
  
Thus, the “$\varepsilon$-error” is “spread across” infinitely many small improvements, each of size $\frac{\varepsilon}{2^n}$. The sum of those infinitely many small pieces is bounded by $\varepsilon$.   
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
4) Why it is so ubiquitous  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
   
• Countable additivity / subadditivity in measure theory:    
  Because measure is countably subadditive, having a “small error” on infinitely many steps doesn’t necessarily blow up the total error. The geometric series $\sum \frac{\varepsilon}{2^n}$ remains finite.    
  
• Flexible approximations:    
  Many standard proofs (e.g., constructing outer approximations, Fubini–Tonelli arguments, or showing that open sets are unions of cubes with arbitrarily small leftover measure, etc.) proceed by gradually refining covers or partitions. At each refinement step, the overhead volume can be forced below $\varepsilon/2^n$.    
  
• Ensuring a single final cover (rather than infinitely many partial covers):    
  After each step, you keep the boxes you want, discard or adjust the ones you do not, and accept only an extra $\frac{\varepsilon}{2^n}$ of volume “waste.” In the end, you collect all the final boxes into one big cover. The total measure overhead from all steps is bounded by $\varepsilon$.    
  
In short, the $\varepsilon/2^n$ trick is a staple in measure theory because it handles the infinite process of refining covers in such a way that the total volume overhead is controlled by a convergent geometric series.  
   
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
5) Summary  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  
   
The “$\varepsilon/2^n$ trick” is simply the systematic practice of splitting your allowable error $\varepsilon$ into a geometric sequence of smaller portions—$\tfrac{\varepsilon}{2}, \tfrac{\varepsilon}{4}, \tfrac{\varepsilon}{8},\dots$. When covering a set $E$ by a sequence of (hopefully better and better) covers, each refinement can “use up” only $\tfrac{\varepsilon}{2^n}$ of extra volume. Summing these yields a total error below $\varepsilon$. Thus, by the final stage (or a union of all stages), you obtain a single cover whose volume is within $\varepsilon$ of the optimal possible measure. This elegantly resolves infinite-step constructions in measure theory while keeping track of the total cost in a finite way.


# The Lebesgue outer measure of an elementary set

-----------------------------------------

Let $E \subset of R^d$ be a bounded, elementary set. An elementary set is one which is a finite or countably finite union of "boxes" in $R^d$. We can define the elementary measure $\mu(E)$, the Jordan outer measure $\mu^{*,(J)}$  and the Lebesgue outer measure $\mu^*(E)$ in the standard manner. We note that in this case, $\mu(E) = \mu^{*,(J)}$.

We need to prove that $\mu^* (E) = \mu(E)$. 

First we note that We have to prove two inequalities:

$$ 
\mu^* (E) \leq \mu(E) \qquad \mu(E) \leq \mu^* (E)
$$

The first inequality follows easily since the Lebesgue outer measure follows from a countable cover of boxes while the Jordan outer measure is from a finite cover. With the freedom afforded by the countable cover, the inequality follows.

To prove the second inequality, we will use the Heine Borel theorem - for a bounded set such as $E$, every open cover will have a finite subcover. The boxes we choose to cover $E$ can be made open using the $\varepsilon/2^n$ trick. The volume of the  subcover on which $\mu(E)$ is based will be $\leq$  the volume of the conuntable cover of $E$ on which $\mu^*(E)$ is based.

Fill in details to make this proof rigorous.

---------------------

Below is a step‐by‐step proof that, for a bounded elementary set $E \subset \mathbb{R}^d$, its Lebesgue outer measure $\mu^*(E)$ equals its elementary (or Jordan) measure $\mu(E)$. The argument hinges on two inequalities:  

$$  
\mu^* (E) \;\le\; \mu(E)  
\quad\text{and}\quad  
\mu(E) \;\le\; \mu^* (E).  
$$  

We prove each in turn.  
  
1 **Proof that $\mu^*(E) \leq \mu(E)$** 
   
By definition,  
   
- $\displaystyle \mu^*(E) = \inf \Big\{ \sum_{k=1}^{\infty} \mathrm{vol}(B_k) \;\Big|\; E \subset \bigcup_{k=1}^{\infty} B_k,\, B_k\text{ are boxes} \Big\}$.  
   
- $\displaystyle \mu(E) = \inf \Big\{ \sum_{j=1}^n \mathrm{vol}(C_j) \;\Big|\; E \subset \bigcup_{j=1}^n C_j,\, C_j\text{ are boxes (finite cover)} \Big\}.$  
   
Because $\mu(E)$ is defined via finite covers and $\mu^*(E)$ via countable covers, each finite cover of $E$ by boxes is, in particular, also a countable cover (just add infinitely many empty boxes if one wishes). Hence any candidate sum of volumes that appears in the definition of $\mu(E)$ is also a candidate for $\mu^*(E)$. Taking the infimum over all finite covers in $\mu(E)$ and the infimum over all countable covers in $\mu^*(E)$ yields:  

$$  
\mu^* (E)\;\le\;\mu(E).  
$$  
   
2 **Proof that $\mu(E) \leq \mu^*(E)$**  
   
For each $\varepsilon > 0$, let  

$$  
\sum_{k=1}^{\infty} \mathrm{vol}(B_k) \;<\; \mu^*(E) + \varepsilon  
$$  

be a covering of $E$ by countably many boxes $\{B_k\}_{k=1}^\infty$. Thus  

$$  
E \;\subset\; \bigcup_{k=1}^{\infty} B_k.  
$$  
   
Since $E$ is given to be bounded, we can use the Heine–Borel Theorem, which states that every open cover of a bounded (and closed) set in $\mathbb{R}^d$ has a finite subcover. To apply it rigorously here, one often inflates each box $B_k$ slightly to ensure they are open sets (for instance, replace each closed interval factor $[a,b]$ in a box by an open interval $(a-\delta,b+\delta)$, adjusting $\delta$ to be arbitrarily small). In any case, we obtain an open cover of $E$. By Heine–Borel, there exists a finite subcollection $\{B_{k_1}, B_{k_2}, \ldots, B_{k_m}\}$ such that 

$$  
E \;\subset\; \bigcup_{\ell=1}^m B_{k_\ell}.  
$$  
   
Now, observe that the volume of the finite subcover cannot exceed the total volume of the original countable cover. Hence 

$$  
\sum_{\ell=1}^m \mathrm{vol}\bigl(B_{k_\ell}\bigr) \;\le\; \sum_{k=1}^{\infty} \mathrm{vol}(B_k)  
\;<\; \mu^*(E) + \varepsilon.  
$$  

Since $E\subset \bigcup_{\ell=1}^m B_{k_\ell}$ is a finite cover of $E$, by the very definition of the elementary (Jordan) measure, we have  

$$  
\mu(E)  
\;\le\;  
\sum_{\ell=1}^m \mathrm{vol}\bigl(B_{k_\ell}\bigr)  
\;\le\;  
\mu^*(E) + \varepsilon.  
$$ 

Because $\varepsilon>0$ was arbitrary, letting $\varepsilon \to 0$ yields 

$$  
\mu(E) \;\le\; \mu^*(E).  
$$  
   
**Conclusion** 
   
Combining both inequalities,  

$$  
\mu^*(E) \;\le\; \mu(E)  
\quad\text{and}\quad  
\mu(E) \;\le\; \mu^*(E),  
$$  

we conclude that

$$  
\mu^*(E) \;=\; \mu(E).  
$$  

Thus, for a bounded elementary set $E\subset \mathbb{R}^d$, its Lebesgue outer measure and its elementary (Jordan) measure coincide.


## Making the boxes open

Below is a more detailed explanation of how to inflate each box in a controlled way so that we still stay within a volume bound of $\mu^*(E) + \varepsilon$. This clarification fills in the gap needed prior to applying Heine–Borel in the proof.   
  
1) Setup: A countable cover by boxes  
   
Fix $\varepsilon > 0$. By the definition of the Lebesgue outer measure $\mu^*(E)$, there is a countable collection of boxes $\{B_k\}_{k=1}^{\infty}$ such that  

$$  
E \;\subset\; \bigcup_{k=1}^{\infty} B_k  
\quad\text{and}\quad  
\sum_{k=1}^{\infty} \mathrm{vol} \bigl(B_k\bigr) \;<\;\mu^*(E)\;+\;\frac{\varepsilon}{2}.  
$$  
   
We wish to modify each $B_k$ slightly into an open box $\widetilde{B}_k$ so that $\sum_{k=1}^{\infty} \mathrm{vol}(\widetilde{B}_k)$ remains bounded by $\mu^*(E) + \varepsilon$.  
   
2) Inflating each box in a controlled manner  
   
Each $B_k$ is typically a product of intervals. For simplicity, assume  

$$  
B_k \;=\; [a_{k,1},\,b_{k,1}]\,\times \cdots \times [a_{k,d},\,b_{k,d}]  
\;\subset\; \mathbb{R}^d.  
$$  

We now choose $\delta_k > 0$ sufficiently small so that the open box

$$  
\widetilde{B}_k  
\;=\;  
\bigl(a_{k,1} - \delta_k,\; b_{k,1} + \delta_k\bigr)\,\times \cdots \times   
\bigl(a_{k,d} - \delta_k,\; b_{k,d} + \delta_k\bigr)  
$$

still has volume close to $\mathrm{vol}(B_k)$. Specifically, the volume of $\widetilde{B}_k$ is

$$  
\mathrm{vol}\bigl(\widetilde{B}_k\bigr)  
\;=\;  
\prod_{i=1}^d \bigl((b_{k,i} - a_{k,i}) + 2\delta_k\bigr).  
$$  

Since $\prod_{i=1}^d (b_{k,i} - a_{k,i}) = \mathrm{vol}(B_k)$, we 
can make $\delta_k$ so small that  

$$  
\mathrm{vol}\bigl(\widetilde{B}_k\bigr)  
\;\le\;  
\mathrm{vol}(B_k) \;+\; \frac{\varepsilon}{2^{k+1}}.  
$$  

Such a choice is always possible because as $\delta_k \to 0$, $\mathrm{vol}(\widetilde{B}_k)$ continuously decreases to $\mathrm{vol}(B_k)$.  
   
3) Controlling the total volume of the inflated boxes  
   
By defining each $\delta_k$ as above, we have for all $k$:  

$$  
\mathrm{vol}\bigl(\widetilde{B}_k\bigr)  
\;\le\;  
\mathrm{vol}(B_k) + \frac{\varepsilon}{2^{k+1}}.  
$$  

Hence  

$$  
\sum_{k=1}^{\infty} \mathrm{vol}\bigl(\widetilde{B}_k\bigr)  
\;\le\;  
\sum_{k=1}^{\infty} \left(\mathrm{vol}(B_k) + \frac{\varepsilon}{2^{k+1}}\right)  
\;=\;  
\sum_{k=1}^{\infty} \mathrm{vol}(B_k)  
\;+\;  
\sum_{k=1}^{\infty} \frac{\varepsilon}{2^{k+1}}.  
$$  

Since   
$\sum_{k=1}^{\infty} \mathrm{vol}(B_k) < \mu^*(E) + \frac{\varepsilon}{2}$   
by hypothesis, and  
$\sum_{k=1}^{\infty} \tfrac{\varepsilon}{2^{k+1}} = \tfrac{\varepsilon}{2}$,  
we obtain  

$$  
\sum_{k=1}^{\infty} \mathrm{vol}\bigl(\widetilde{B}_k\bigr)  
\;\le\;  
\left(\mu^*(E) + \frac{\varepsilon}{2}\right) \;+\; \frac{\varepsilon}{2}  
\;=\;  
\mu^*(E) + \varepsilon.  
$$  
   
4) Applying Heine–Borel to the open cover  
   
Clearly,  

$$  
E  
\;\subset\;  
\bigcup_{k=1}^{\infty} B_k  
\;\subset\;  
\bigcup_{k=1}^{\infty} \widetilde{B}_k,  
$$  

and now $\{\widetilde{B}_k\}$ is an open cover of $E$. Because $E$ is bounded (and we can also assume it is measurable or at least the part to be covered is within a bounded region), the Heine–Borel Theorem implies there is a finite subcover  

$$  
E  
\;\subset\;  
\bigcup_{\ell=1}^m \widetilde{B}_{k_\ell}  
\;\subset\;  
\bigcup_{k=1}^{\infty} \widetilde{B}_k.  
$$  

Thus,  

$$  
\sum_{\ell=1}^m \mathrm{vol} \bigl(\widetilde{B}_{k_\ell}\bigr)  
\;\le\;  
\sum_{k=1}^{\infty} \mathrm{vol}\bigl(\widetilde{B}_k\bigr)  
\;\le\;  
\mu^*(E)\;+\;\varepsilon.  
$$  
   
Because $\bigl\{\widetilde{B}_{k_\ell}\bigr\}_{\ell=1}^m$ is a finite cover of $E$ by boxes (indeed, each $\widetilde{B}_{k_\ell}$ is still a box in the sense of having Cartesian product shape, just open intervals instead of closed), this finite subcover is admissible for the definition of the elementary (Jordan) measure $\mu(E)$. Taking the infimum over all such finite covers yields   

$$  
\mu(E)  
\;\le\;  
\sum_{\ell=1}^m \mathrm{vol}\bigl(\widetilde{B}_{k_\ell}\bigr)  
\;\le\;  
\mu^*(E)\;+\;\varepsilon.  
$$  

Since $\varepsilon > 0$ was arbitrary, letting $\varepsilon \to 0$ shows   

$$  
\mu(E) \;\le\; \mu^*(E).  
$$  
   
Summary of the inflation step  
   
The key point is that by carefully choosing for each box $B_k$ a small inflation parameter $\delta_k$ so that the volume $\mathrm{vol}(\widetilde{B}_k)$ exceeds $\mathrm{vol}(B_k)$ by at most $\frac{\varepsilon}{2^{k+1}}$, we ensure   

$$  
\sum_{k=1}^\infty \mathrm{vol}(\widetilde{B}_k)  
\;\le\;  
\mu^*(E) + \varepsilon  
$$  

while still having an open cover of $E$. This allows us to apply Heine–Borel to extract a finite subcover of total volume at most $\mu^*(E) + \varepsilon$.


## Disjoint boxes

**Result 1**

Thus far, we have considered elementary sets which are unions of pairwise disjoint boxes. Now, we introduce the notion of $\textit{almost disjoint}$ boxes which are boxes whose interiors are disjoint which means that they share boundary. 

For a set of almost disjoint boxes $B_i, i = 1, \cdots, n$, the elementary measure obeys the finite additivity property $\mu (B_1 \cup B_2 \cup \cdots \cup B_n) = |B_1| + \cdots + |B_n|$.

With this setup, let $E$ be a set such that it is a countable union of almost disjoint boxes. That is,

$$ 
E = \bigcup_{i=1}^{\infty} B_i 
$$

Then, we have to prove that:

$$
\mu^*(E) = \sum_{i=1}^{\infty} |B_i|
$$

__________________________________________________________________

Below is a step‐by‐step argument showing why, if a set    

$$  
E \;=\; \bigcup_{i=1}^{\infty} B_i  
$$    

is written as a countable union of “almost disjoint” boxes $B_i$ (i.e., boxes whose interiors are pairwise disjoint), then its Lebesgue outer measure is exactly the sum of the volumes of the $B_i$:    

$$  
\mu^*(E)  
\;=\;  
\sum_{i=1}^{\infty} |B_i|.  
$$    

Here, $|B_i|$ denotes the usual $d$‐dimensional volume of the box $B_i$.  
   
1) Two inequalities to prove  
   
We must show   

$$  
\mu^*(E)  
\;\le\;  
\sum_{i=1}^{\infty} |B_i|  
\quad\text{and}\quad  
\mu^*(E)  
\;\ge\;  
\sum_{i=1}^{\infty} |B_i|.  
$$  

Proving these two inequalities establishes   
$\mu^*(E)=\sum_{i=1}^\infty |B_i|$.  
   
2) Showing   
$\displaystyle \mu^*(E) \;\le\;\sum_{i=1}^\infty |B_i|$  
   
Recall the definition of Lebesgue outer measure:  

$$  
\mu^*(E)  
\;=\;  
\inf\Bigl\{  
\sum_{k=1}^{\infty} \mathrm{vol}(I_k)  
\;\Big|\;  
E \subset \bigcup_{k=1}^{\infty} I_k, \,  
\text{each } I_k \text{ a box}  
\Bigr\}.  
$$  

Because   
$\displaystyle E = \bigcup_{i=1}^\infty B_i$   
is itself a countable cover of $E$ by boxes,    

$$  
\sum_{i=1}^\infty |B_i|  
$$  

is automatically one of the (infinitely many) sums inside the “infimum” defining $\mu^*(E)$. Consequently,  
   
$$  
\mu^*(E)  
\;\le\;  
\sum_{i=1}^\infty |B_i|.  
$$  
   

3) Showing   
$\displaystyle \mu^*(E) \;\ge\;\sum_{i=1}^\infty |B_i|$  

   
This direction is more subtle.  We use the fact that finite unions of almost disjoint boxes are elementary sets, and for those we already know (or can easily prove) that “Jordan measure” $=$ “Lebesgue outer measure.”  Concretely:  
   
1. For each $n$, define the finite union  

$$  
E_n  
\;=\;  
\bigcup_{i=1}^n \,B_i.  
$$  

Because $B_1,\dots,B_n$ are almost disjoint (their interiors are pairwise disjoint), one can check (or recall) that the “elementary measure” $\mu(E_n)$ is exactly the sum of the volumes:  

$$  
   \mu(E_n) \;=\; \sum_{i=1}^n |B_i|.  
   $$  
   Moreover, “elementary measure” $\mu(E_n)$ coincides with the Jordan outer measure $\mu^{*,(J)}(E_n)$, and for these nice finite unions of boxes, we also know    
   $\mu^{*,(J)}(E_n) = \mu^*(E_n)$.    

Hence  

$$  
   \mu^*(E_n)  
   \;=\;  
   \mu(E_n)  
   \;=\;  
   \sum_{i=1}^n |B_i|.  
   $$  
   
2. Observe that each $E_n$ is contained in $E$.  By the monotonicity of outer measure,    

$$  
   E_n \;\subset\; E  
   \;\Longrightarrow\;  
   \mu^*(E_n)\;\le\;\mu^*(E).  
   $$  

Therefore  

$$  
   \sum_{i=1}^n |B_i|  
   \;=\;  
   \mu^*(E_n)  
   \;\le\;  
   \mu^*(E).  
   $$  

3. Since the above holds for every finite $n$, we let $n\to\infty$.  The partial sums $\sum_{i=1}^n |B_i|$ increase to $\sum_{i=1}^\infty |B_i|$.  Hence  

$$  
   \sum_{i=1}^\infty |B_i|  
   \;\;=\;\;  
   \lim_{n\to\infty} \,\sum_{i=1}^n |B_i|  
   \;\;\le\;\;  
   \mu^*(E).  
   $$  

Thus we obtain  

$$  
\mu^*(E) \;\ge\;\sum_{i=1}^\infty |B_i|.  
$$  
   
4) Conclusion  
   
Combining both inequalities,  
   
• From the covering definition:  
  $\displaystyle \mu^*(E)\;\le\;\sum_{i=1}^\infty |B_i|$.    
• From the monotonicity and finite‐union argument:  
  $\displaystyle \mu^*(E)\;\ge\;\sum_{i=1}^\infty |B_i|$.  
   
we conclude  

$$  
\mu^*(E)  
\;=\;  
\sum_{i=1}^\infty |B_i|.  
$$  
   
Hence, whenever $E$ is (by definition) a countable union of almost disjoint boxes $\{B_i\}$, its Lebesgue outer measure is exactly the sum of the volumes of those boxes.



 **Result 2**

For $E \subset R^d$ and bounded, let $E$ be the countable union of almost disjoint boxes. In this case, we have 

$$
\mu^*(E) = \mu_{*,(J)} (E)
$$

the Lebesgue outer measure is equal to the inner Jordan measure. We need to prove this.

Here are some initial thoughts on the proof.

Let $B_i, i = 1, \cdots, \infty$ be the almost disjoint boxes. We can show that

$$
\mu*(E) = \sum_{i=1}^{\infty} | B_i |
$$

where $|B_i| = \ell(B_i)$ is the usual $d$-dimensional volume of the box. So, it seems that we have
to prove two inequalities:

$$
\mu_{*,(J)}(E) \leq \sum_{i=1}^{\infty} | B_i | \qquad \mu_{*,(J)}(E) \geq \sum_{i=1}^{\infty} |B_i|
$$

the first inequality rough sketch:  we can choose a finite subset of the given $B_i$. Let $N$ be the number of the boxes. We have to choose $N$ and we have to take a supremum meaning we have to choose which $N$ of the countable boxes $B_i$ we choose.

Foramlize or modify this argument.


--------------------

Below is a succinct version of the proof with a simplified indexing in Step 2, removing any extraneous notation.  
   
───────────────────────────────  
1) Setting and Definitions  
───────────────────────────────  
   
Let $E \subset \mathbb{R}^d$ be bounded, and suppose  

$$  
E \;=\; \bigcup_{i=1}^{\infty} B_i,  
$$  

where each $B_i$ is a (Jordan-measurable) box and the $B_i$ are “almost disjoint” (their interiors are disjoint, and overlaps can only occur on boundaries of measure zero).  Let $\ell(B_i)$ denote the usual $d$-dimensional volume of $B_i$.  
   
We wish to show  

$$  
\mu^*(E) \;=\; \mu_{*,(J)}(E),  
$$  

where $\mu^*$ is the Lebesgue outer measure, and  

$$  
\mu_{*,(J)}(E)  
\;=\;  
\sup  
\Bigl\{  
\sum_{k=1}^{m} \ell(J_k)  
\;\Bigm|\;  
J_1,\dots,J_m \subset E,\;\; (J_k \text{ pairwise disjoint boxes})  
\Bigr\}  
$$  

is the inner Jordan measure.  In particular, a key step is to prove  

$$  
\mu_{*,(J)}(E)  
\;\;\le\;\;  
\sum_{i=1}^{\infty}  
\ell(B_i).  
$$  
   
───────────────────────────  
2) The Inequality  $\mu_{*,(J)}(E) \;\le\; \sum_{i=1}^\infty \ell(B_i)$  
─────────────────────────  
   
By definition,  

$$  
\mu_{*,(J)}(E)  
\;=\;  
\sup  
\Bigl\{  
\sum_{k=1}^{m} \ell(J_k)  
\;\Bigm|\;  
J_k\subset E,\;  
(J_k \text{ disjoint}),  
\;  
m\in\mathbb{N}  
\Bigr\}.  
$$  

Any finite family $\{J_1,\dots,J_m\}$ of disjoint boxes is contained in $E$.  In particular, we can also consider finite subcollections taken directly from our given family $\{B_i\}$.  Concretely,  
   
• Pick any finite subcollection of the $B_i$; for simplicity, label them   

$$  
B_1,\; B_2,\;\dots,\; B_N  
$$  

(which is just a finite subset of $\{B_i\}_{i=1}^\infty$).    
• Because the $B_i$ are almost disjoint, we have  

$$  
\sum_{k=1}^N \ell\bigl(B_k\bigr)  
\;\;\le\;\;  
\sum_{i=1}^\infty \ell\bigl(B_i\bigr).  
$$  

• By definition of $\mu_{*,(J)}(E)$, we take the supremum of such finite-sum volumes of disjoint boxes *inside* $E$.  But every finite subcollection from the $B_i$ is one of those valid families.  Thus each finite sum is at most $\sum_{i=1}^\infty \ell(B_i)$, and taking the supremum cannot exceed this same infinite sum.  
   
Hence  

$$  
\mu_{*,(J)}(E)  
\;\;\le\;\;  
\sum_{i=1}^\infty  
\ell(B_i),  
$$  

as desired.  
   
───────────────────────  
3) Remarks on the Reverse Inequality and Conclusion  
───────────────────────  
   
• One similarly shows  

$$  
\mu^*(E)  
\;=\;  
\sum_{i=1}^{\infty}\ell(B_i).  
$$  

(Here we use that $E$ is covered by the $B_i$, apply subadditivity of $\mu^*$, and argue each $B_i$ is Jordan measurable. By approximating each $B_i$ from the inside, we obtain that $\sum_{i=1}^\infty \ell(B_i)$ can be matched arbitrarily closely by finite disjoint unions inside $E$.)  
   
• Combining these, one arrives at   

$$  
\mu^*(E)  
\;=\;  
\sum_{i=1}^{\infty}\ell(B_i)  
\;=\;  
\mu_{*,(J)}(E),  
$$  

completing the proof that the Lebesgue outer measure of $E$ equals its inner Jordan measure (under the assumption that $E$ is covered by countably many almost disjoint Jordan-measurable boxes).


## Redux: Pairwise disjoint and Almost disjoint boxes

Previously, we defined an elementary set as the finite union of pairwise disjoint boxes in $\mathbb{R}^d$. We also define the notion of *almost disjoint* boxes where the interiors are pairwise disjoint but they possibly share a boundary. The difference seems subtle to me. Clarify the differences. Use simple examples if needed.

**Answer**

Let us use the term  

box =  a Cartesian product of one–dimensional intervals  
    (e.g. in \(\mathbb R^{2}\) a rectangle of the form  
    \([a_1,b_1]\times[a_2,b_2]\)).

Closed boxes will be used in all examples below.  
Write \(|B|\) for the usual Euclidean volume of a box \(B\).

Two notions of “disjointness” for a *family* of boxes \(\{B_i\}\):

1. pairwise disjoint  
 \(B_i\cap B_j=\varnothing\) whenever \(i\neq j\);

2. almost disjoint  
 \(\operatorname{int}(B_i)\cap\operatorname{int}(B_j)=\varnothing\)  
 whenever \(i\neq j\).

Because a box is the closure of its interior, “almost disjoint’’ allows
overlaps that are contained entirely in the \((d{-}1)\)-dimensional
boundaries of the boxes.

============================================================

Simple one–dimensional pictures

============================================================

• Disjoint intervals  

\[
[0,1]\quad\text{and}\quad[2,3]
\]

share no point at all.

• Almost disjoint but *not* disjoint  

\[
[0,1]\quad\text{and}\quad[1,2].
\]

The point \(x=1\) belongs to both intervals, yet  
\((0,1)\cap(1,2)=\varnothing\).

============================================================

Why the distinction matters

============================================================

A.  Definition of an elementary set  
 Traditionally an elementary set is a *finite* union of
*pairwise disjoint* boxes.
The disjointness guarantees

\[
\mu\!\Bigl(\,\bigcup_{i=1}^{n}B_{i}\Bigr)
  \;=\;\sum_{i=1}^{n}|B_{i}|
\tag{1}
\]

*without having to invoke any measure theory*: the volumes simply
add because no point is counted twice.

B.  Almost disjoint families  
 If the boxes overlap only on their boundaries, equation (1) is still
*true* for both Jordan and Lebesgue measure, because boundaries
have measure \(0\):

\[
|B_i\cap B_j|\;=\;0\quad(i\neq j)
\quad\Longrightarrow\quad
\Bigl|\bigcup_{i=1}^{n}B_i\Bigr|
  =\sum_{i=1}^{n}|B_i|.
\]

However, this statement already uses the measure–zero property of
boundaries (a result, not a definition).  Hence “pairwise disjoint’’ is
the safer primitive notion when one *defines* elementary sets.

C.  Practical reason to relax to “almost’’  
 Closed dyadic cubes tile \(\mathbb R^{d}\) in a way that forces boundary
contacts: each point on a common face belongs to two adjacent cubes.
Allowing “almost disjoint” lets us speak of such a tiling while still
having additivity of volume.

============================================================

Two–dimensional illustration

============================================================

Take in \(\mathbb R^{2}\)

\[
B_1=[0,1]\times[0,1],\quad
B_2=[1,2]\times[0,1].
\]

The squares share the vertical line segment \(\{1\}\times[0,1]\).
They are almost disjoint but not disjoint.
Their interiors—open unit squares—are disjoint.
We still have  
\(|B_1\cup B_2| = |B_1|+|B_2| = 1+1 =2\)
because the shared edge has area \(0\).

============================================================

Summary

============================================================

pairwise disjoint  = absolutely no overlap; primary notion in the  
          definition of an elementary set.  

almost disjoint   = interiors disjoint, boundaries may overlap;  
          convenient for tilings (e.g. dyadic cubes) and still gives additivity because boundaries have measure \(0\).

The two notions coincide *up to null sets*, but they are not the
same set–theoretically.

**Suppose we have a set $S = (0.5, \; 2] \in \mathbb{R}$. A pairwise disjoint cover is $[0, \; 1), \; \; [1, \; 3]$. Is this correct? If so, this suggests that there needs to be a mix of open and closed (or half open at least) boxes for a pairwise disjoint cover.**

**Answer**

Yes, the two intervals  

\[
[0,1)\quad\text{and}\quad[1,3]
\]

are pairwise disjoint (their intersection is empty) and their union does
indeed contain  

\[
S=(0.5,2].
\]

Why do they have to be chosen with different “open/closed’’ conventions?
Because if we kept both of them closed at the point \(1\) we would get an
overlap there:

\[
[0,1]\cap[1,3]=\{1\}\neq\varnothing .
\]

A single common convention avoids that problem completely.  
For instance, if in one dimension we agree always to take the interval
*closed on the left and open on the right*, then

\[
[0,1)\quad\text{and}\quad[1,3)
\]

are automatically disjoint.  
(The second interval still covers the point \(2\) because \(2<3\).)

Exactly the same trick works in higher dimensions: use half-open
*boxes*

\[
B=\prod_{k=1}^{d}[a_k,b_k),
\]

all closed on the “left’’ faces and open on the “right’’ faces.  
Any two such boxes either are disjoint or one lies completely to the left
of the other along some coordinate, so boundary overlaps never occur.
Hence there is no need to mix different kinds of brackets; one systematic
choice of half-open boxes is enough to obtain pairwise disjoint covers
whenever we want them.


**Clarify why a finite union of almost disjoint boxes is an elementary set cover. It seems that there are certain points (on the boundary of the boxes) are not in the cover.**

**Answer**

Let  

\[
\mathscr B=\{B_{1},\dots ,B_{N}\},\qquad 
B_{i}= \prod_{k=1}^{d}[a_{i,k},b_{i,k}]
\]

be a *finite* family of closed boxes whose interiors are
pair-wise disjoint:

\[
\operatorname{int}(B_{i})\cap\operatorname{int}(B_{j})=\varnothing
\quad(i\neq j).
\tag{1}
\]

Such boxes are usually called *almost disjoint*.
Two questions often arise.

(A)  Does the union \(\bigcup_{i=1}^{N} B_{i}\) leave “gaps’’ on the
     common boundary pieces?

(B)  Can this union be regarded as an *elementary* set, whose
     measure is simply the sum of the volumes of the boxes?

The answers are “No’’ to (A) (no gaps appear) and “Yes’’ to (B).  
Here are the details.

--------------------------------------------------------------------

1  No uncovered boundary points
   
--------------------------------------------------------------------

Because every \(B_{i}\) is *closed*, each of its boundary points is
itself an element of \(B_{i}\).  
If two boxes touch along a common face (or edge, or corner), every point
of that face belongs to *both* boxes, hence certainly to their
union.  Therefore

\[
\bigcup_{i=1}^{N}B_{i}
\text{ contains all boundary pieces; no point is missing.}
\]

Example in \(\mathbb R\):
\([0,1]\cup[1,2]=(0,2]\cup\{0,1\}=[0,2]\).  
The point \(1\) lies in each interval, so the union covers it.

--------------------------------------------------------------------

2    Turning “almost disjoint’’ into “disjoint’’
   
--------------------------------------------------------------------

Although the union already covers everything, measure theory sometimes
demands a family of *pair-wise disjoint* sets so that

\[
|B_{1}\cup\cdots\cup B_{N}|=\sum_{i=1}^{N}|B_{i}|
\tag{2}
\]

holds literally (without invoking “boundary has measure \(0\)’’).
A standard device is to give every box the same
half-open convention:

\[
\tilde B_{i}=\prod_{k=1}^{d}
                 [a_{i,k},b_{i,k})
\qquad(i=1,\dots ,N).
\]

Key facts

•  The half-open boxes \(\tilde B_{i}\) are pair-wise *disjoint*.
   Any point lies in *at most* one of them because, in the first
   coordinate where two boxes meet, one of the two half-open intervals
   uses “\([\,\,,\,)\)” and the other uses “\((\,\,,\,]\)”.

•  They still cover the same set, up to a measure-zero difference:

\[
\bigcup_{i=1}^{N}\tilde B_{i}
\;=\;
\bigl(\bigcup_{i=1}^{N} B_{i}\bigr)\setminus Z,
\]

where \(Z\) is contained in a union of the shared boundary faces, hence
\(|Z|=0\).

Therefore the family \(\{\tilde B_{i}\}\) is an *elementary cover*
in the strict sense (finite, pair-wise disjoint boxes) and satisfies

\[
\mu\!\Bigl(\,\bigcup_{i=1}^{N}B_{i}\Bigr)
    =\mu\!\Bigl(\,\bigcup_{i=1}^{N}\tilde B_{i}\Bigr)
    =\sum_{i=1}^{N}|\tilde B_{i}|
    =\sum_{i=1}^{N}|B_{i}|.
\]

(The second equality uses that \(Z\) has measure \(0\); the last equality
uses that removing an open face does not change a box’s volume.)

--------------------------------------------------------------------

3  Summary

--------------------------------------------------------------------

•  Having only “almost disjoint’’ boxes does *not* leave gaps; every
   boundary point is automatically covered (because the boxes are
   closed).

•  When one needs a *genuinely disjoint* family, convert the closed
   boxes \(B_{i}\) into half-open ones \(\tilde B_{i}\); the union and
   the total volume remain the same up to sets of measure \(0\).

Hence any finite union of almost-disjoint boxes can be regarded—​for all
measure-theoretic purposes—​as an elementary set (finite union of
pair-wise disjoint boxes).


## Closed Dyadic cubes in $R^d$

What is the concept of a closed dyadic cube in $R^d$? In particular a cube of side length $2^{-n}$ for some non-negative integer $n$.

**Answer**

Closed dyadic cubes are the standard “binary grid’’ blocks in \(\mathbb {R}^{d}\).

Fix an integer \(n\ge 0\).  
A (closed) dyadic cube of *generation \(n\)* (or *side–length \(2^{-n*\)}) is the Cartesian product of \(d\) closed “dyadic’’ intervals whose end-points are integer multiples of \(2^{-\,n}\):

\[
Q = \prod_{i=1}^{d}
        \Bigl[\,k_{i}\,2^{-n},\;(k_{i}+1)\,2^{-n}\Bigr],
\qquad
k_{1},\dots ,k_{d}\in\mathbb{Z}.
\]

Properties  

1.  Side length  
    \(\displaystyle \operatorname{side}(Q)=2^{-n}\).

2.  Volume (Lebesgue measure)  
    \(\displaystyle |Q|=(2^{-n})^{d}=2^{-nd}\).

3.  Nesting / subdivision  
    Every cube of generation \(n\) is the disjoint union of
    \(2^{d}\) cubes of generation \(n+1\); conversely, it is contained in
    exactly one cube of every generation \(m<n\).

4.  Tiling  
    The collection

    \[
      \mathcal D_{n}
        \;:=\;
      \Bigl\{
         \prod_{i=1}^{d}[k_{i}2^{-n},(k_{i}+1)2^{-n}]
         : k_{i}\in\mathbb Z
      \Bigr\}
    \]

    forms a partition (tiling) of \(\mathbb R^{d}\) into congruent cubes.

5.  Half-open and open versions  
    In many measure-theoretic constructions one prefers the half-open
    variant
    \(\prod_{i}[k_{i}2^{-n},(k_{i}+1)2^{-n})\)
    because these cubes are pairwise disjoint even along their
    boundaries.  
    The underlying geometric idea, however, is the same.

Thus, “a closed dyadic cube of side length \(2^{-n}\)” means precisely a
set of the form

\[
\boxed{
   Q=\prod_{i=1}^{d}
        [k_{i}2^{-n},(k_{i}+1)2^{-n}]
   \quad(k_{i}\in\mathbb Z).
}
\]

Such cubes play a central role in dyadic decompositions, martingale
theory, and many proofs in real analysis because they give a
binary-nested grid that meshes perfectly with Lebesgue measure.


## Lebesgue measurability with dyadic cube tiling

So, if one could partition or tile a bounded set $S \in \mathbb{R}^d$ with these dyadic cubes, then $S$ is Lebesgue measurable. Is this correct?

**Answer**

Yes—under a natural interpretation of “tile’’ the statement is correct.

Precise formulation  
Assume \(S\subset\mathbb R^{d}\) is bounded and that there exists a family  
\(\{Q_{i}\}_{i\in I}\) of closed dyadic cubes such that

1. (Tiling) \(S=\bigcup_{i\in I}Q_{i}\);  
2. (Almost disjointness) \(\operatorname{int}(Q_{i})\cap\operatorname{int}(Q_{j})=\varnothing\) for \(i\ne j\).

Then \(S\) is Lebesgue–measurable and  

\[
\mu(S)=\sum_{i\in I}|Q_{i}|\;(=2^{-nd}\text{ summed over the cubes}).
\]

Why this is true

Step 1.  Only countably many dyadic cubes are involved.  
Fix a large cube \(C=[-M,M]^{d}\) that contains \(S\).
For each generation \(n\ge 0\) there are at most  
\((2M\,2^{\,n}+1)^{d}<\infty\) cubes of side \(2^{-n}\) inside \(C\).
Hence the set of *all* dyadic cubes intersecting \(C\) (and a fortiori those tiling \(S\)) is a countable union of finite sets—therefore countable.  
So we may relabel

\[
\{Q_{i}\}_{i\in I}=\{Q_{1},Q_{2},Q_{3},\dots\}.
\]

Step 2.  Each \(Q_{k}\) is a Lebesgue–measurable set (it is closed).  
The σ–algebra of Lebesgue–measurable sets is closed under countable unions; hence

\[
S=\bigcup_{k=1}^{\infty}Q_{k}
\]

is Lebesgue–measurable.

Step 3.  Measure of the union.  
Because the interiors of the cubes are pairwise disjoint, the cubes themselves intersect only on sets of measure zero (their boundaries).  Consequently

\[
\mu(S)=\sum_{k=1}^{\infty}\mu(Q_{k})=\sum_{k=1}^{\infty}|Q_{k}|.
\]

Thus the ability to partition (tile) a bounded set by dyadic cubes indeed implies that the set is Lebesgue measurable.  (For unbounded sets one needs to check σ–finiteness, but the same idea works in each bounded slice.)


**Clarify with more detail Step1. Fix $M$ and $n =0, 1$. How many cubes are inside $C$?**

**Answer**

Let  

\[
C=[-M,M]^d\qquad(M>0)
\]

be the closed cube that contains the bounded set \(S\).
For every integer \(n\ge 0\) a *dyadic cube of generation \(n\)*
has side length \(2^{-n}\) and the form  

\[
Q=\prod_{i=1}^{d}
    \bigl[k_{i}2^{-n},\,(k_{i}+1)2^{-n}\bigr],
\qquad  k_{i}\in\mathbb Z .
\]

To find how many such cubes are fully contained in \(C\) we look at the
allowable indices \(k_i\).

----------------------------------------------------------------
**Range of each \(k_i\)**

----------------------------------------------------------------
The condition \(Q\subset C\) says

\[
-M\le k_{i}2^{-n}\qquad\text{and}\qquad
(k_{i}+1)2^{-n}\le M
\quad\;(i=1,\dots ,d).
\]

Multiply by \(2^{\,n}\):

\[
-\,M\,2^{\,n}\le k_{i}\le M\,2^{\,n}-1 .
\]

Thus each \(k_i\) can take the integer values

\[
k_{i}\in\Bigl\{-\lfloor M2^{\,n}\rfloor,\;
               -\lfloor M2^{\,n}\rfloor+1,\;
               \dots,\;
               \lceil M2^{\,n}\rceil-1\Bigr\}.
\]

----------------------------------------------------------------
**Number of possibilities**

----------------------------------------------------------------
The number of allowed integers for a single coordinate \(k_i\) is no
more than  

\[
\lfloor M2^{\,n}\rfloor+\lceil M2^{\,n}\rceil
\;\le\;
2M2^{\,n}+1 .
\]

Because each of the \(d\) coordinates can be chosen independently, the
*total* number of generation-\(n\) dyadic cubes inside \(C\) is at
most  

\[
\bigl(2M\,2^{\,n}+1\bigr)^{d}<\infty .
\]

----------------------------------------------------------------
**Concrete examples**

----------------------------------------------------------------
•  \(n=0\) (side length \(1\)).  
   At most \((2M+1)^{d}\) such cubes lie in \(C\).

•  \(n=1\) (side length \(1/2\)).  
   At most \((4M+1)^{d}\) such cubes lie in \(C\).

----------------------------------------------------------------
**Why this proves countability**

----------------------------------------------------------------
For each fixed \(n\) the set of generation-\(n\) cubes inside \(C\) is
finite.  The collection of *all* dyadic cubes in \(C\) is therefore
a countable union of finite sets (one finite set for each \(n=0,1,2,\dots\)),
hence countable.  Consequently any tiling of the bounded set \(S\subset
C\) by dyadic cubes involves only countably many cubes, as asserted in
Step 1.


## Lebesgue measure of open set

Let $E \in \mathbb{R}^d$ be open. Using the concept of closed dyadic cubes, show that the $E$ is the countable union of closed dyadic cubes and we can therefore write the Lebesgue outer measure of $E$ in terms of the volume of these cubes.

**Answer**

Notation and basic facts

•  A (closed) dyadic cube of generation \(n\in\mathbb{N}_0\) is a set  

\[
Q=\prod_{j=1}^{d}\bigl[k_{j}2^{-n},(k_{j}+1)2^{-n}\bigr],
\qquad k_{j}\in\mathbb{Z}.
\]

Its side length is \(2^{-n}\) and its volume is  
\(|Q|=(2^{-n})^{d}=2^{-nd}\).

•  For fixed \(n\) and a fixed bounded cube \(C=[-M,M]^{d}\) there are at
most \((2M\,2^{\,n}+1)^{d}<\infty\) generation–\(n\) dyadic cubes
contained in \(C\); hence the *whole* family of dyadic cubes in
\(\mathbb{R}^{d}\) is countable (a countable union of those finite
sets).

The goal  
If \(E\subset\mathbb{R}^{d}\) is open we shall  
(i)  write \(E\) as a *countable* union of closed dyadic cubes with
pairwise disjoint interiors, and  
(ii) express the (outer) Lebesgue measure of \(E\) as the sum of the
volumes of those cubes.

Step 1 – every point of \(E\) sits in some dyadic cube contained in \(E\)

Let \(x\in E\).  Because \(E\) is open, pick \(r>0\) such that the open
ball \(B(x,r)\subset E\).
Choose \(n\) large enough so that \(\sqrt{d}\,2^{-n}<r\).
Define integers \(k_{j}=\lfloor 2^{n}x_{j}\rfloor\) \((j=1,\dots,d)\) and
let  

\[
Q(x)=\prod_{j=1}^{d}[k_{j}2^{-n},(k_{j}+1)2^{-n}].
\]

The diameter of \(Q(x)\) is \(\sqrt{d}\,2^{-n}<r\), hence
\(Q(x)\subset B(x,r)\subset E\).  
Consequently

\[
E=\bigcup_{\;Q\subset E,\;Q\text{ dyadic}}Q.
\tag{1}
\]

The union on the right is taken over a
*countable* collection, because the whole dyadic grid is
countable.  Relabel those cubes as \(\{Q_{i}\}_{i\ge1}\).

Step 2 – choose maximal (hence disjoint–interior) cubes

Two closed dyadic cubes are either disjoint in their interiors or one is
contained in the other.
From the family \(\{Q_{i}\}_{i\ge1}\) choose the maximal members with
respect to inclusion:

\[
\mathcal{M}:=\bigl\{\,Q_{i}:\;
          Q_{i}\subset E,\;
          \nexists\;Q_{j}\subset E\text{ with }Q_{i}\subsetneq Q_{j}\bigr\}.
\]

•  Maximal cubes have pairwise disjoint interiors;  
   if their interiors met, one cube would lie inside the other, violating
   maximality.

•  Every point \(x\in E\) belongs to a cube in \(\mathcal{M}\):  
   indeed \(x\) lies in some dyadic cube \(Q\subset E\); enlarging \(Q\)
   step by step (still staying inside \(E\)) must stop after finitely
   many steps, producing a maximal cube that still contains \(x\).

Therefore

\[
E=\bigcup_{Q\in\mathcal{M}}Q
\quad\text{with}\quad
\operatorname{int}(Q)\cap\operatorname{int}(Q')=\varnothing
\ (Q\ne Q').
\tag{2}
\]

Because \(\mathcal{M}\) is a subset of the countable set of *all*
dyadic cubes, it is itself countable; write
\(\mathcal{M}=\{Q_{1},Q_{2},\dots\}\).

Step 3 – measure of the union

The boundaries of the cubes have Lebesgue measure \(0\), so the sets
\(Q_{i}\) intersect only on measure–zero sets.  Hence finite additivity
extends to countable additivity:

\[
\mu(E)=\sum_{i=1}^{\infty}\mu(Q_{i})=\sum_{i=1}^{\infty}|Q_{i}|.
\tag{3}
\]

(Since \(E\) is open, \(\mu(E)=\mu^{*}(E)\); thus the equality holds for
the outer measure as well.)

Conclusion  

Every open set \(E\subset\mathbb{R}^{d}\) can be written as a countable
union of closed dyadic cubes with disjoint interiors, and its Lebesgue
outer measure is

\[
\boxed{\;
   \mu^{*}(E)=\sum_{i=1}^{\infty}|Q_{i}|
 \;}
\]

where \(\{Q_{i}\}\) is the family of maximal dyadic cubes contained in
\(E\).

## $\mu^*(E) = \mu_{*,(J)}(E)$

In this case of an open set $E \in \mathbb{R}^d$, is $\mu^*(E) = \mu_{*,(J)}(E)$? Since we have just shown that $E$ can be written as the countable union of closed dyadic cubes with disjoint interiors, we should be able to use this property. Provide the details.

**Answer**

Let  

\[
E\subset \mathbb{R}^{d}\quad\text{be open}.
\]

In the previous result we constructed a countable family of closed
dyadic cubes with pairwise–disjoint interiors 

\[
\{Q_{i}\}_{i\ge 1},\qquad 
E=\bigcup_{i=1}^{\infty}Q_{i},\qquad  
|Q_{i}|=(2^{-n_{i}})^{d}
\]

and proved

\[
\mu^{*}(E)=\sum_{i=1}^{\infty}|Q_{i}|.
\tag{1}
\]

We now compare this to the *Jordan inner measure*  

\[
\mu_{*,(J)}(E):=\sup\Bigl\{\mu(F):F\subset E,\;F\text{ elementary}\Bigr\},
\]

(“elementary’’ = finite union of pairwise–disjoint rectangles).

For simplicity we first treat the bounded case; the unbounded case is
handled afterwards by approximation.

--------------------------------------------------------------------
1.  Bounded open set

--------------------------------------------------------------------

Assume \(E\) is bounded, hence the series in (1) is finite (or at least
convergent).  
Set, for every \(N\in\mathbb{N}\),

\[
F_{N}:=\bigcup_{i=1}^{N}Q_{i}.
\]

•  \(F_{N}\subset E\) and \(F_{N}\) is elementary (finite union of
boxes).  
•  Its (Jordan) measure is

\[
\mu(F_{N})=\sum_{i=1}^{N}|Q_{i}|.
\]

Because the interiors of the \(Q_i\) are disjoint the sequence
\(\mu(F_{N})\) is increasing and

\[
\lim_{N\to\infty}\mu(F_{N})=
\sum_{i=1}^{\infty}|Q_{i}|=\mu^{*}(E).
\tag{2}
\]

Taking the supremum over \(\{\mu(F_{N})\}\) yields

\[
\mu_{*,(J)}(E)\;\ge\;
\sup_{N}\mu(F_{N})
=\mu^{*}(E).
\tag{3}
\]

The reverse inequality is immediate:

\[
\mu_{*,(J)}(E)\le \mu^{*,(J)}(E)\le\mu^{*}(E),
\tag{4}
\]

because inner ≤ outer and Jordan outer ≤ Lebesgue outer.  

Combining (3) and (4) we get

\[
\boxed{\;\mu_{*,(J)}(E)=\mu^{*}(E)\;} .
\]

--------------------------------------------------------------------
2.  Unbounded open set

--------------------------------------------------------------------

Write \(E_{m}:=E\cap[-m,m]^{d}\) for \(m=1,2,\dots\).
Each \(E_{m}\) is bounded and open, so by the bounded case

\[
\mu_{*,(J)}(E_{m})=\mu^{*}(E_{m})\quad(m\ge 1).
\tag{5}
\]

The family \(\{E_{m}\}\) increases to \(E\):

\[
E=\bigcup_{m=1}^{\infty}E_{m},
\qquad 
E_{m}\subset E_{m+1}.
\]

Both \(\mu_{*,(J)}\) and \(\mu^{*}\) are monotone and σ–continuous from
below; hence

\[
\mu_{*,(J)}(E)=\lim_{m\to\infty}\mu_{*,(J)}(E_{m})
              =\lim_{m\to\infty}\mu^{*}(E_{m})
              =\mu^{*}(E).
\]

--------------------------------------------------------------------
3.  Conclusion

--------------------------------------------------------------------

For *every* open set \(E\subset\mathbb{R}^{d}\) we have

\[
\boxed{\;
     \mu_{*,(J)}(E)=\mu^{*}(E)
     }.
\]

The equality relied crucially on two facts:

1.  Every open set can be written as a countable union of closed dyadic
    cubes with disjoint interiors.

2.  Finite unions of those cubes approximate the whole union in measure,
    allowing the Jordan inner measure (which uses only *finite*
    unions) to reach the same value as the Lebesgue outer measure (which
    allows *countable* unions).


## Lebesgue outer measure of any set (Outer Regularity)

    
Let $E \in \mathbb{R}^d$ be any set.  Let $U$ be an open set such that $E \subset U$. We want to show that:

\[
\mu^*(E) = \text{inf}_{U, E \subset U} \mu^*(U)
\]

My idea is this: From monotonicity, $\mu^*(E) \leq \text{inf}_{U, E \subset U} \mu^*(U)$ is immediate.

We have previously shown that any open $U$ can be written as a union of dyadic cubes and that $\mu^*(U)$ is equal to the sum of the volumes of these dyadic cubes. It seems to me that we could use this to prove what we want. We start with a $U$ and associated dyadic cube tiling and refine the tiling by removing cubes and approaching $E$ from the outside. This always assures that we have an open set.

Does this make sense?

**Answer**

Let  

\[
\mu^{*}(A)=\inf\Bigl\{\,\sum_{j=1}^{\infty}|Q_{j}|\; :\;
                A\subset\bigcup_{j=1}^{\infty}Q_{j},
                \;Q_{j}\text{ boxes}\Bigr\}
\]

be the Lebesgue outer measure in \(\mathbb R^{d}\).
We prove the *outer regularity* formula  

\[
\boxed{\;
   \mu^{*}(E)=\inf\bigl\{\mu^{*}(U):U\text{ open},\;E\subset U\bigr\}.
\;}
\tag{1}
\]

(The “ inf ” on the right is often denoted \(\mu^{*o}(E)\).)

The inequality \(\mu^{*}(E)\le\inf_{U\supset E}\mu^{*}(U)\) is immediate
from monotonicity.  Thus it suffices to show:

\[
\forall\varepsilon>0\;\; \exists\text{ open }U\supset E
\quad\text{such that}\quad
\mu^{*}(U)\le\mu^{*}(E)+\varepsilon.
\tag{2}
\]

Below is a construction that uses the dyadic–cube decomposition of open
sets that was proved earlier.

**Step 1.  A near–optimal dyadic covering of \(E\)**

Fix \(\varepsilon>0\).
Because dyadic cubes form a countable family of boxes, the infimum in
the definition of \(\mu^{*}(E)\) can be restricted to them.  Hence there
is a countable collection of *closed* dyadic cubes
\(\{Q_{k}\}_{k\ge1}\) with  

\[
E\subset\bigcup_{k=1}^{\infty}Q_{k},
\qquad
\sum_{k=1}^{\infty}|Q_{k}|<\mu^{*}(E)+\frac{\varepsilon}{2}.
\tag{3}
\]

**Step 2.  Enlarge each cube slightly to make an open cover**

For every \(k\) choose a number \(\delta_{k}>0\) so small that the cube  

\[
Q_{k}^{\delta_{k}}
   =\{x\in\mathbb R^{d}:\operatorname{dist}(x,Q_{k})<\delta_{k}\}
\]

satisfies  

\[
|Q_{k}^{\delta_{k}}|\le |Q_{k}|+\frac{\varepsilon}{2^{k+1}}.
\tag{4}
\]

Each \(Q_{k}^{\delta_{k}}\) is an *open* box (still dyadic–shaped,
just slightly larger).  Define  

\[
U:=\bigcup_{k=1}^{\infty}Q_{k}^{\delta_{k}} .
\]

Then \(U\) is open and \(E\subset U\) because \(E\subset\cup Q_{k}\subset\cup Q_{k}^{\delta_{k}}\).

**Step 3.  Estimate \(\mu^{*}(U)\)**

Using the very cover \(\{Q_{k}^{\delta_{k}}\}\) in the definition of
outer measure,

\[
\mu^{*}(U)\le\sum_{k=1}^{\infty}|Q_{k}^{\delta_{k}}|
          \le\sum_{k=1}^{\infty}\Bigl(|Q_{k}|+\frac{\varepsilon}{2^{k+1}}\Bigr)
          =\sum_{k=1}^{\infty}|Q_{k}|+\frac{\varepsilon}{2}
          <\Bigl(\mu^{*}(E)+\frac{\varepsilon}{2}\Bigr)+\frac{\varepsilon}{2}
          =\mu^{*}(E)+\varepsilon.
\]

This is exactly the requirement (2).

**Conclusion**

For every \(\varepsilon>0\) we produced an open set \(U\supset E\) with
\(\mu^{*}(U)\le\mu^{*}(E)+\varepsilon\);
hence

\[
\inf_{U\supset E}\mu^{*}(U)\le\mu^{*}(E).
\]

Combined with the opposite inequality from monotonicity, we have proven
(1).  The dyadic–cube argument shows explicitly how one “refines’’ a
dyadic tiling to approach the given set \(E\) from outside while keeping
the measure arbitrarily close to \(\mu^{*}(E)\).

## Equivalence: $\mu^{*}(U)\le\mu^{*}(E)+\varepsilon$ equivalent to $\mu^*(U \backslash E) \leq \varepsilon$

$\forall\varepsilon>0\;\; \exists\text{ open }U\supset E$, is the expression
$\mu^{*}(U)\le\mu^{*}(E)+\varepsilon$ equivalent to $\mu^*(U \backslash E) \leq \varepsilon$?

**Answer**

Yes – for every set \(E\subset\mathbb R^{d}\) and every open
\(U\supset E\) the two inequalities  

\[
\text{(a)}\qquad 
\mu^{*}(U)\le \mu^{*}(E)+\varepsilon ,
\qquad\qquad
\text{(b)}\qquad 
\mu^{*}(U\setminus E)\le\varepsilon
\]

are equivalent.  The implication in each direction uses only
monotonicity and sub-additivity of the outer measure.

Forward direction  
Assume (a).  Because \(E\subset U\) we have monotonicity

\[
\mu^{*}(E)\le \mu^{*}(U).
\]

Hence

\[
0\le \mu^{*}(U)-\mu^{*}(E)\le\varepsilon .
\tag{1}
\]

Now write \(U = E\cup(U\setminus E)\).
By sub-additivity,

\[
\mu^{*}(U)\le \mu^{*}(E)+\mu^{*}(U\setminus E),
\]

so that

\[
\mu^{*}(U)-\mu^{*}(E)\le\mu^{*}(U\setminus E).
\]

Combine this with (1) to get \(\mu^{*}(U\setminus E)\le\varepsilon\),
i.e. (b).

Reverse direction  
Assume (b).  Using the same sub-additivity,

\[
\mu^{*}(U)=\mu^{*}\bigl(E\cup(U\setminus E)\bigr)
           \le\mu^{*}(E)+\mu^{*}(U\setminus E)
           \le\mu^{*}(E)+\varepsilon,
\]

which is (a).

Consequently

\[
\boxed{\;
   \forall\,\varepsilon>0,\;
   U\supset E\text{ open}:\;
   \mu^{*}(U)\le\mu^{*}(E)+\varepsilon
   \;\Longleftrightarrow\;
   \mu^{*}(U\setminus E)\le\varepsilon
 }.
\]

Thus the two formulations of outer regularity are interchangeable.


## Inner Regularity of Lebesgue measure

Let $E \in \mathbb{R}^d$ be Lebesgue measurable. Let $K \in \mathbb{R}^d$ be compact (closed and bounded) such that $K \subset E$. Then, 

\[
\mu(E) = \underset{K \subset E}{\text{sup}} \mu(K)
\]

This would be the inner regularity property. Prove it.

**Answer**

Let \(E\subset\mathbb{R}^{d}\) be a Lebesgue–measurable set and let  
\(\mu\) denote Lebesgue measure.  
We prove the inner (or compact) regularity of \(\mu\):

\[
\boxed{\;
   \mu(E)=\sup\bigl\{\mu(K):K\subset E,\;K\text{ compact}\bigr\}.
   \;}
\tag{1}
\]

(The right–hand side is understood to be \(+\infty\) if \(\mu(E)=+\infty\).)

**1  Reduction to the case \(\mu(E)<\infty\)**

If \(\mu(E)=\infty\) the equality (1) is immediate, because for
\(K_{n}=E\cap[-n,n]^{d}\) one has \(K_{n}\subset K_{n+1}\subset E\) and
\(\mu(K_{n})\to\infty\).
Hence we assume \(\mu(E)<\infty\) for the rest of the proof.

**2  From outer regularity to a bounded closed subset**

Fix \(\varepsilon>0\).
By outer regularity of Lebesgue measure
there exists an open set \(U\supset E\) with  

\[
\mu(U\setminus E)<\frac{\varepsilon}{3}.
\tag{2.1}
\]

Because \(E^{c}\) is also measurable,
apply outer regularity to \(E^{c}\) to obtain an open set  
\(V\supset E^{c}\) such that  

\[
\mu(V\cap E)=\mu(V\setminus E^{c})<\frac{\varepsilon}{3}.
\tag{2.2}
\]

Define  

\[
F:=\mathbb{R}^{d}\setminus V .
\]

Then \(F\) is *closed* and \(F\subset E\) by construction, while  

\[
\mu(E\setminus F)=\mu(E\cap V)<\frac{\varepsilon}{3}.
\tag{2.3}
\]

So far, nothing guarantees that \(F\) is bounded.  To fix this, set  

\[
F_{R}:=F\cap [-R,R]^{d}\quad(R>0).
\]

Because \(F\subset E\) and \(\mu(E)<\infty\), we can choose
\(R=R(\varepsilon)\) so large that  

\[
\mu\bigl(F\setminus F_{R}\bigr)<\frac{\varepsilon}{3}.
\tag{2.4}
\]

Now \(F_{R}\) is *closed and bounded*, hence compact, and
\(F_{R}\subset E\).
Put \(K:=F_{R}\).

**3  Measure estimate**

Combine (2.3) and (2.4):

\[
\mu(E\setminus K)
   \le\mu(E\setminus F)+\mu(F\setminus K)
   <\frac{\varepsilon}{3}+\frac{\varepsilon}{3}
   <\varepsilon.
\]

Equivalently,

\[
\mu(K)>\mu(E)-\varepsilon.
\tag{3.1}
\]

**4  Supremum equals \(\mu(E)\)**

Because \(\varepsilon>0\) was arbitrary, for every such \(\varepsilon\)
we have produced a compact \(K\subset E\) with
\(\mu(K)>\mu(E)-\varepsilon\).
Therefore  

\[
\sup_{K\subset E,\;K\text{ compact}}\mu(K)\;\ge\;\mu(E)-\varepsilon,
\]

and letting \(\varepsilon\downarrow 0\) gives

\[
\sup_{K\subset E,\;K\text{ compact}}\mu(K)\;\ge\;\mu(E).
\]

The opposite inequality is immediate since every \(K\subset E\)
satisfies \(\mu(K)\le\mu(E)\).
Thus equality holds, completing the proof of (1).

**5  Conclusion**

Lebesgue measure on \(\mathbb{R}^{d}\) is *inner regular*:

\[
\mu(E)=\sup\{\mu(K):K\subset E,\;K\text{ compact}\}
\quad\text{for every measurable }E\subset\mathbb{R}^{d}.
\]

This inner approximation by compact sets, together with outer
approximation by open sets, constitutes the full regularity of Lebesgue
measure.

## Lebesgue measure is Radon

The Lebesgue measure has inner and outer regularity. This makes it a Radon measure. Is this correct? What is the concept of a Radon measure?

**Answer**

Yes.  When it is restricted to the Borel sets of \(\mathbb R^{d}\) the Lebesgue measure is a Radon measure, precisely because it enjoys the two regularity properties you have already proved (and is locally finite).  Below is the precise definition and a short verification.

1 Locally-compact Hausdorff space  
Throughout let \(X\) be a locally compact Hausdorff space and let \(\mathscr B(X)\) denote its Borel \(\sigma\)-algebra.

2 Definition (Radon measure)  
A positive measure \(\mu\) on \(\mathscr B(X)\) is called a Radon measure if it satisfies

(a) (local finiteness) every compact set has finite measure:

\[
\forall K\subset X \text{ compact}\quad \mu(K)<\infty;
\]

(b) (inner regularity) each Borel set can be approximated from inside by compact sets:

\[
\forall E\in\mathscr B(X)\qquad
\mu(E)=\sup\bigl\{\mu(K):K\subset E,\;K\text{ compact}\bigr\}.
\]

Many authors include

(c) (outer regularity)  

\[
\forall E\in\mathscr B(X)\qquad
 \mu(E)=\inf\bigl\{\mu(U):E\subset U,\;U\text{ open}\bigr\},
\]

although for metrizable locally-compact spaces (in particular \(X=\mathbb R^{d}\)) property (c) follows automatically from (a) and (b).  Equivalently one can phrase (b)–(c) with the \(\varepsilon\)-version:

\[
\forall\varepsilon>0\;\exists\;K\subset E\subset U,\; 
K\ \text{compact},\ U\ \text{open},\ 
\mu(U\setminus K)<\varepsilon .
\]

3 Lebesgue measure is Radon  

Let \(\lambda\) denote Lebesgue measure on \(\mathbb R^{d}\).  
(The formal Radon object is \(\lambda\!\restriction_{\mathscr B(\mathbb R^{d})}\), i.e. its restriction to Borel sets; the later completion adds the usual null subsets but does not change the regularity statement.)

•  Local finiteness A compact set in \(\mathbb R^{d}\) is bounded, hence contained in a cube \([-M,M]^d\); \(\lambda([-M,M]^d)=(2M)^d<\infty\).

•  Outer regularity  
was proved earlier: for every measurable \(E\subset\mathbb R^{d}\)

\[
\forall\varepsilon>0\;\;\exists\ U\text{ open},\ E\subset U,\;
\lambda(U)\le\lambda(E)+\varepsilon .
\]

•  Inner regularity  
was also proved: for every measurable \(E\) and every \(\varepsilon>0\)
there exists a compact \(K\subset E\) with
\(\lambda(E)\le\lambda(K)+\varepsilon\).
Equivalently  

\[
\lambda(E)=\sup_{K\subset E,\;K\text{ compact}}\lambda(K).
\]

Because \(\lambda\) satisfies (a)+ (b) (+ (c)), it is a Radon measure.

4 Other examples  
Dirac measures \(\delta_x\), finite (or \(\sigma\)-finite) sums of such, counting measure on a discrete subset, and any finite Borel measure with a continuous (or merely locally integrable) density with respect to Lebesgue measure are all Radon on \(\mathbb R^{d}\).

5 Summary  
A Radon measure on a locally compact Hausdorff space is a locally finite Borel measure that is inner regular (and, in many presentations, also outer regular).  
Because Lebesgue measure on \(\mathbb R^{d}\) has those properties, it is indeed a Radon measure.