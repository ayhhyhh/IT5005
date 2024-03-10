# Chapter 3 Predicates Logic

**Predicates **are statements that contain variables and represent properties or relationships. Example:
$$
P(x)=\text{"x is a student at NUS"}
$$
such objects are referred to as a **propositional functions** or **open sentences**.

**Domain**: The domain of a predicate variable is the set of all values that may be substituted in place of the variable.

**Truth Set**: The set of elements that makes predicate true.
$$
\{x\in D| P(x)\}
$$
**Universal Quantifier**: $\forall$

**Universal Statement**: statements of the form $\forall x\in D, Q(x)$

- True: iff $Q(x)$ is true for **every **$x \in D$

- False: iff $Q(x)$ is false for **at least one** $x \in D$​
  - The x make $Q(x)$ be false is called **counterexample**.

**Existential Quantifier**: $\exist$, $\exist !$: There exist a **unique**, or there is **one and only one**.



**Skolemization**: One way to eliminate $\exist$ in statements. 
$$
\exist x\  Female(x) \lrarr Female (c)
$$
c refers to one particular person in the universe of discourse. Aka **Skolem Constant**



Equivalent Form of Universal and Existential Statements: **Narrowing Domain**
$$
\forall x\in U, P(x)\rarr Q(x) \lrarr\forall X\in D, Q(x)
$$
where $D$ is the subset of $U$ that makes $P(x)$



**Negation**:
$$
(\text{Origin}) & \forall x \in D, P(x) \\
(\text{Negation}) & \exist x\in D, \neg P(x)\\
\hline
&\neg(\forall x \in D, P(x)) \lrarr \exist x\in D, \neg P(x)
$$
**Vacuously True**: 
$$
\forall x\in D, P(x) \rarr Q(x)
$$
is called **Vacuously True** or **true by default** iff $P(x)$ is false for every $x\in D$



**Contrapositive**, **Converse**, **Inverse**: Similar to Chapter 2, No change in quantifier. Example:
$$
\text{Origin} & \forall x \in \mathrm R, x > 2\rarr x ^2 > 4\\
\text{Converse} & \forall x \in \mathrm R, x ^2 > 4\rarr x > 2\\
\text{Inverse} & \forall x \in \mathrm R, x \leq 2\rarr x ^2 \leq 4\\
\text{Contrapositive} & \forall x \in \mathrm R, x ^2 \leq 4\rarr x \leq 2\\
$$
**Sufficient Condition**: $r(x)$ is a sufficient condition for $s(x)$ means
$$
\forall x, r(x) \rarr s(x)
$$
**Necessary Condition**: $r(x)$ is a Necessary  condition for $s(x)$ means
$$
\forall x, \neg r(x) \rarr \neg s(x)
$$
**Only If**: $r(x)$ only if $s(x)$ means
$$
\forall x, \neg s(x)\rarr \neg r(x)
$$


