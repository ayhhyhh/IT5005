## Chapter 2 Propositional Logic

Definition: A system of symbols, formal language, operators and inference rules that lets you draw sound conclusions about the world around you.

Two major classes of logic:

- Propositional Logic (命题逻辑): 研究命题之间的逻辑关系，使用与或非($\and, \or, \neg$), 组成复合命题.
- First Order Logic (一阶逻辑, aka Predicate Logic 谓词逻辑): 除命题外，引入了谓词，变量和量词的概念.

Knowledge Base: Observations(Truth), A set of inference rules, and conclusions drawn from observation.

### Propositional Logic

#### Basic Statement

Terminology:

- Negation: 命题的否定，逻辑非($P, \neg P$​)
- Conjunction: 逻辑乘(与)(and $\and$)
- Disjunction: 逻辑或 (or $\or$​​)
- Exclusive-or: 与非(XOR) $p\  \text{xor}\ q = (p\or q)\and \neg(p\or q)$

**Attention: Negation is performed first, Conjunction and Disjunction must use parentheses**

- Logical Equivalence: 逻辑等价 $a \and b$ and $b \and a$​ have the same truth values, so they are logically equivalent. To find not logical equivalent: find one counter example.
- De Morgan’s Laws:
  - $\neg(p\and q) = \neg p \or \neg q$
  - $\neg (p\or q)=\neg p \and \neg q$​



- Tautologies: 重言式，始终为真，存在冗余信息($A \or \neg A$)
- Contradictions: 矛盾，始终为否，($a \and \neg a$​)

- Laws:

$$
\begin{array}{|c|c|c|}
\hline 
\text{Commutative laws 交换律}  & p \and q = q\and p & p \or q = q\or p \\
\hline
\text{Associative Laws 结合律} & (p\and q)\and r = p\and (q \and r) &(p\or q)\or r = p\or (q \or r) \\
\hline
\text{Distributive Laws 分配律} & p \and (q \or r)=(p \and q) \or (p\and r) &p \or (q \and r)=(p \or q) \and (p\or r)\\
\hline 
\text{Identity Laws} & p \and \text{true} = p & p\or \text{false} = p\\
\hline
\text{Negation Laws} & p \or \neg p = \text{true}& p\and \neg p = \text{false}\\
\hline
\text{Double Negative Law} & \neg(\neg p) = p &\\
\hline
\text{Idempotent Laws} & p \and p = p & p\or p = p\\
\hline 
\text{Unvieral Bound Laws} & p \or \text{true} = \text{true} & p \and \text{false} = \text{false}\\
\hline
\text{De Morgan's Laws} & \neg(p\and q) = \neg p \or \neg q &\neg (p\or q)=\neg p \and \neg q \\
\hline
\text{Absorption Laws} & p \or (p \and q) = p & p\and (p\or q) = p\\
\hline
\text{Negation of True and False} & \neg \text{true} = \text{false} & \neg \text{false} = \text{true}\\
\hline
\end{array}
$$

**Attention: Remember to cite the law in every step in your workings.**





#### Conditional Statement

Conditional Statement: If p, then q: $p\rarr q$​

Truth Values:
$$
\begin{array}{|c|c|c|}
\hline 
p & q & p\rarr q\\
\hline 
T & T & T\\
\hline 
T & F & F\\
\hline 
F & * & T\\
\hline
\end{array}
$$
So, we have: $p\rarr q \lrarr \neg p \or q$ (Implication Law)

- Contrapositive: 逆否命题  $P\rarr Q$的逆否命题$\neg Q \rarr \neg P$
- Converse: 逆命题 $P\rarr Q$ 的逆命题 $Q \rarr P$
- Inverse: 否命题 $P\rarr Q$ 的否命题 $\neg P \rarr \neg Q$
- Note: For conditional Statement $p\rarr q$​, its Inverse Statement are the contrapositive statement of its Converse Statement.

$$
q\rarr p \lrarr \neg p \rarr \neg q
$$



- Necessary Condition: 必要条件 
  - r is a sufficient condition for s: $r\rarr s$

- Sufficient Condition: 充分条件
  - r is a necessary condition for s: $\neg r \rarr \neg s \lrarr s\rarr r$

- Biconditional/Necessary and Sufficient Condition: 充分必要
  - p if and only if q: $p\lrarr q$



- Order: 1. not   2. and/or   3. if-then/if and only if

#### Argument

**Argument** Form is a sequence of statements. All statements in an arguments except for the final one, are called **promises**(or **assumptions **or **hypothesis**). The final statement is called **conclusion**. An argument is **valid** means that if all **premise **are true, then the conclusion are true.

A row of the truth table in which all the premises are true is called a **critical row**. If all critical row the conclusion are true, the argument is valid, else invalid. Example:

<img src="https://cdn.jsdelivr.net/gh/ayhhyhh/IMGbed@master/imgs/202403092243952.png" alt="image-20240309221709083" style="zoom:50%;" />

**Syllogism**: An argument form consisting of two premises and a conclusion. 

**Modus ponens**: One kind of syllogism with the following form. It is **valid **argument.
$$
p\rarr q&\text{promise 1}\\
p&\text{promise 2}\\
·q &\text{conclusion}
$$
**Modus tollens**: Another kind of syllogism. **Valid**.
$$
p\rarr q&\text{promise 1}\\
\neg q&\text{promise 2}\\
·\neg p &\text{conclusion}
$$
**Rulers of Inference**:

- Modus ponens and Modus tollens.
- Generalization.

$$
p &\text{promise}\\
·p\or q&\text{conclusion}
$$

- Specialization.

$$
p\and q &\text{promise}\\
·p&\text{conclusion}
$$

- Elimination.

$$
p\or q &\text{promise 1}\\
\neg q &\text{promise 2}\\
·p&\text{conclusion}
$$

- Transitivity.

$$
p\rarr q & \text{promise 1}\\
q\rarr r & \text{promise 2}\\
·p\rarr r & \text{conclusion}\\
$$

- Proof by Division into cases.

$$
p\or q & \text{p 1}\\
p\rarr r& \text{p 2}\\
q\rarr r& \text{p 3}\\
· r &\text{c}
$$

- Proof by Contradiction:

$$
\neg p\rarr \text{false} &\text{p}\\
·p&\text{c}
$$



A **fallacy**(谬误) is an error in reasoning that results in invalid argument.

- Ambiguous
- Circular reasoning.
- Jumping.

Examples:

- The argument below is valid by modus ponens. But its major premise is false, and so is its conclusion.
  - p1: If Joseph Schooling is a Singaporean, then Joseph Schooling is a badminton player.
  - p2: Joseph Schooling is a Singaporean.
  - c:    Joseph Schooling is a badminton player.
- The argument below is invalid by the converse error, but it has a true conclusion.
  - p1: If Singapore is a garden city, then Singapore has lots of trees.
  - p2: Singapore has lots of trees.
  - c  : Singapore is a garden city.

An argument is called **sound** if, and only if, it is **valid **and all its premises are true.

An argument that is not sound is called **unsound**.