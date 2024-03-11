# Chapter 4 Inference Mechanisms

This chapter is to show how to automate proofs. (Check if a statement is capable in one specific system(model))

Model: A set of true/false assignments to individual relevant statements.

- If a statement $s$ is true, then “M satisfies s” or “M is a model of s”, written as $M(s)$
- If statement a **entails **b, if in every model in which a is true, b is also true.
  - $a\models b \lrarr M(a)\subseteq M(b)$

Similarly, a knowledge base KB entails a statement $a$,  iff any model that make KB true also make $a$ true.
$$
KB \models b \lrarr M(KB) \subseteq M(b)
$$


**Resolution **is a method for test if $KB \models a$​.

**Conjunctive Normal Form**(CNF) Require:

1. Every clause in KB must be statements joined by disjunctions. (OR)
2. All clauses are joined by conjunctions. (AND)
3. Also know as product-of-sums(POS) representation.

Example:
$$
(P\or Q) \and(Q\or R\or S)\and (T\or U)
$$
Resolution: To see if $KB\models a$

1. Introduce $\neg a$ to the set of clauses.
2. If a series of resolution steps reduces a clause to an empty set, that means:
   - adding $\neg a$ to the knowledge base resulted in a contradiction
   - Thus $\neg a$ cannot be true, and a must be true. $KB\models a$

 **Definite Clause**: A definite clause is a clause that has **exactly** one **positive** literal. For example:

- $$
  P\or \neg Q\or \neg R&\text{yes, only P}\\
  P\or Q \or \neg R&\text{no, P, Q}
  $$

**Horn clause**: A horn clause is a clause that has **at most** one **positive** literal. For example:

- $$
  P\or \neg Q\or \neg R&\text{yes, only P}\\
  \neg P\or \neg Q \or \neg R&\text{yes, no literal is positive}
  $$

These two kinds of clauses interest us because they can be represent by implication.
$$
P\or \neg Q\or \neg R\equiv \neg(Q\and R) \or P \equiv(Q\and R) \rarr P
$$


**Forward Chaining**: 

1. Given the knowledge base KB consisting of Horn clauses, and query U
2. While True: When all the premises of an implication are true, add the consequent to the KB
3. Stop When:
   1. U is added to KB, then $KB\models U$
   2. Ran out of Horn Clauses, then $KB \nvDash U$

4. Sometimes calculates irrelative clauses.

**Backward Chaining**:

1. Start from the goal, see if its premises can be satisfied.
2. If premises is false, then KB may not entail the goal.(Why may not)
3. Otherwise, for each unknow term of premise, set that term as a sub-goal and recursively find its truth value.



**Unification**: substitute variable $x$ to a instance $x_0$, 类似于实例化. 接着用Generalized Modus Ponens处理.

