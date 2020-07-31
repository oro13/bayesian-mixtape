[Probabilistic Systems Analysis and Applied Probability](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-041-probabilistic-systems-analysis-and-applied-probability-fall-2010)                            



## Course Arc

- 


## Broad Course Objectives

- develop the art of describing uncertainty in terms of probabilistic models
- develop the skill of probabilistic reasoning







## Specific Learning Objectives

- describe the generic structure of probabilistic models and their basic properties



#### Additional Resources

The Bayesian New Statistics: Hypothesis testing, estimation,meta-analysis, and power analysis from a Bayesianperspective [paper](https://link.springer.com/content/pdf/10.3758/s13423-016-1221-4.pdf)

Combinatorial principles [wiki](https://en.wikipedia.org/wiki/Combinatorial_principles)





### Notes on [Reading](https://www.vfu.bg/en/e-Learning/Math--Bertsekas_Tsitsiklis_Introduction_to_probability.pdf)



#### 1.1 Sets

Amusing anecdote on tension of general use of the word probability

define probability in terms of freqency of occurence, as a percentage of sucesses in a moderately large number of similar situations

- this may be appropriate in some situations with uncertainty, but many where its not
  - e.g. a scholar who says the iliad and odyssey were composed by the same person with a probability of 90%, this doesnt convey information based on frequencies, because the subject is a one-time event (*difference*), rather this probability is an expression of the scholar's subjective belief
  - many argue subjective beliefs aren't interesting for math and science POVs
    - however people are often making decisions in the presence of uncertainty, and a systematic way of making use of their beliefs is a prereq for successful, or at least consistent decision making
    - the choices and actions of rational people can reveal a lot about the inner held subjective probabilities (*I see another layer of why I want to do this, we're walking into a realm of new possibilities, and dont want to resort to status quo tactics, but also dont want to be wrong/unviable/nonexistent/unreal*)

probabilistic models (in the scope of this material) assign probabilities to collections (sets) of possible outcomes

- that is why set notation & operations are foundational to probability theory and models

#### sets

- a collection of objects which are the elements of the set,
- If $S$ is a set and $x$ is an element of $S$, 
  - we write $x{\in}S$ 
- If $x$ is not an element of $S$, we write
  - $x{\notin}S$
- A set can have no elements, the empty set, ${\empty}$
- if $S$ contains a finite number of elements, we write it in braces
  -  $S=\{x_{1},x_{2},{\dots},x_{n}\}$.
  - eg set of possible outcomes of a die role is $\{1,2,3,4,5,6\}$, the set of possible outcomes of a coin toss is $\{H,T\}$ where $H$ is 'heads' and $T$ is 'tails'
- if $S$ contains infinitely many elements which can be enumerated in a list (ie there are as many elements are there are positive integers), we write
  - $S=\{x_{1},x_{2},{\dots}\}$
  - and we say $S$ is countably infinite
    - e.g. the set of even integers can be written as $\{0,2,-2,4,-4,{\dots}\}$ and is countably infinite
- we can consider the set of all $x$ that have a certain property $P$, and denote it by
  - $\{x {\mid} x\ \text{satisfies}\ P\}$
    - symbol "${\mid}$" is to be read "such that"
  - eg the set of even integers can be written as $\{k{\mid}k/2\ \text{is integer}\}$
  - e.g. the set of all scalars $x$ in the interval $[0,1]$ can be written as $\{x{\mid}0{\leq}x{\leq}1\}$.
    - elements $x$ take a continuous range of values, and cannot be written down in a list (theres a proof for this)
    - such as set is said to be **uncountable**

- if every element of a set $S$ is also an element of a set $T$, we say that $S$ is a subset of $T$, and we write $S \subset T$ or $T \supset S$ 
  - if  $S \subset T$ &  $T \subset S$, the two sets are equal $S=T$
- the universal set, denoted by ${\Omega}$, which contains all objects that could conceivably be of interest in a particular context
  - when context is specified in terms of set $\Omega$, we only consider sets $S$ that are subsets of $\Omega$, $S \subset \Omega$

#### Set Operations

- The **complement** of a set $S$ with respect to the universe $\Omega$ is the set $\{x \in \Omega \mid x \notin S\}$ 
  - of all elements of $\Omega$ that do not belong to $S$ and is denoted by $S^c$
  - note: $\Omega^c = \empty$.
- The **union** of two sets $S$ and $T$ is the set of all elements that belong to $S$ or $T$ (or both), and is denoted by $S \cup T$
  - $S \cup T = \{x\mid x \in S\  \text{or}\  x \in T\}$
- The **intersection** of two sets $S$ and $T$ is the set of all elements that belong to both $S$ and $T$, and is denoted by $S \cap T$
  - $S \cap T = \{x\mid x \in S\  \text{and}\  x \in T\}$
- When considering the union of several, even infinitiely many sets
  - e.g. if for every positive integer $n$, we are given a set $S_{n}$
    - $\displaystyle\bigcup_{n=1}^\infin S_{n} = S_{1} \cup S_{2} \cup \dots = \{x \mid x \in S_{n} \text{ for some n}\}$ and,
    - $\displaystyle\bigcap_{n=1}^\infin S_{n} = S_{1} \cap S_{2} \cap \dots = \{x \mid x \in S_{n} \text{ for all n}\}$
- Two sets are said to be **disjoint** if their intersection is empty, or more generally, several sets ar said to be disjoint if no two of them have a common element
  - a collection of sets is said to be a *partition* of a set $S$ if the sets in the collection are disjoint and their union is $S$
- if $x$ and $y$ are two objects, we use $(x,y)$ to denote the **ordered pair** of $x$ and $y$, 
- the set of scalars (real numbers) is denoted as $\real$, the set of pairs (two dimensional plane)  is denoted as $\real^2$or triplets (three dimensional plane) is denoted as $\real^3$
- Sets and operations visualized:

![](set-operations)



#### The algebra of Sets

Some examples:

| $S \cup T = T \cup S$                     | $S \cup (T\cup U) = (S \cup T) \cup U$           |
| ----------------------------------------- | ------------------------------------------------ |
| $S\cap(T\cup U)=(S\cap T)\cup (S \cap U)$ | $S \cup (T \cap U) = (S \cup T) \cap (S \cup U)$ |
| $(S^c)^c = S$                             | $S \cap S^c = \empty$                            |
| $S \cup \Omega = \Omega$                  | $S \cap \Omega = S$                              |



Two particularly useful properties are given by **de Morgan's laws**:

| The first law                                                | The second law                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| $(S \cup T)^c = S^c \cap T^c$                                | $(S \cap T)^c = S^c \cup T^c$                                |
| Alternative notation: $\overline{A \cup B} = \bar{A}\cap \bar{B}$ | Alternative notation: $\overline{A \cap B} = \bar{A}\cup \bar{B}$ |
| "The complement of the union is equal to the intersection of the complements" | "The complement of the intersection is equal to the union of the complements" |
| Set notation (for n number of sets): $\left(\displaystyle\bigcup_{n}S_{n}\right)^c = \displaystyle\bigcap_nS_{n}^c$ | Set notation: $\left(\displaystyle\bigcap_{n}S_{n}\right)^c = \displaystyle\bigcup_nS_{n}^c$ |
| **The Set notation proof:**                                  | **The converse proof:**                                      |
| Suppose: $x \in (\cup_{n}S_{n})^c                            | $x \in (\cap_{n}S_{n})^c$                                    |
| Then, $x \notin \cup_{n}S_{n}$                               | $\implies$ $x \notin \cap_{n}S_{n}$                          |
| which implies for every n, we have $x \notin S_{n}$          | $\implies$ for every n,  $x \notin S_{n}$                    |
| thus, $x$ belongs to the complement of every $S_{n}$         | $\implies$ $x$ belongs to the complement of every $S_{n}$    |
| and, $x_{n} \in \cap_{n} S_{n}^c$                            | $\implies$  $x_{n} \in \cup_{n} S_{n}^c$                     |
| $\therefore (\cup_{n}S_{n})^c \sub \cap_{n}S_{n}^c$          | $\therefore (\cap_{n}S_{n})^c \sub \cup_{n}S_{n}^c$          |

Note: this proof is for n Sets, it's helpful to think of just 2 sets as a baseline, though the proof is the same, the proof of 2 sets explained [here](https://www.youtube.com/watch?v=ro1yGNEFSaE)

These laws can be stated in terms of logical convention as

| First Law                                     | Second Law                                 |
| --------------------------------------------- | ------------------------------------------ |
| $\neg(p \and q) = \neg p \or \neg q$          | $\neg(p \or q) = \neg p \and \neg q$       |
| "Neither p nor q is equal to not p and not q" | "Not (p and q) is equal to Not p or Not q" |

where $\neg$ means not, $\and$ means and, $\or$ means or

Note: it's helpful to recreate de Morgan's laws visually, with venn diagrams

#### 1.2 Probabilistic Models

A **probabilistic model** is a mathematical description of an uncertain situation (in accordance to a fundamental framework, explained in this section)

#### The two main elements of a probabilistic model:

- the **sample space** $\Omega$ (Omega), which is the set of all possible outcomes of an experiment
- the **probability law**, which assigns to a set of $A$ possible outcomes (also called an **event**) a nonnegative number $P(A)$ (Called the *probability of $A$) that encodes our *knowledge or belief about the collective 'likelihood'* of the elements of $A$.
- **The probability law** must satisfy certain properties, as we'll see

![](prob-models)

#### Sample Spaces and Events

- Every probabilistic model involves an underlying process, called the **experiment**, that produces exactly ONE out of several possible **outcomes**
  - no restrictions on what constitutes an experiment
    - a single coin toss, three tosses, an infinite sequence of tosses
    - however in this formulation of a probabilistic model, theres only a single experiment, rather than 3 experiments

- The set of all possible outcomes is called the **sample space** of the experiment, and is denoted by $\Omega$
  - sample space of an experiment may consist of a finite or infinite number of possible outcomes
    - finite spaces are conceptually and mathematically simpler
    - sample spaces with an infinite number of elements are quite common
      - e.g. throwing a dart on a square target and viewing the point of impact as the outcome
- A subset of the sample space, that is, a collection of possible outcomes, is called an **event**
  - in practice, any collection of possible outcomes, including the entire sample space $\Omega$ and its complement, the empty set $\empty$, may qualify as an event
    - there are theoretical examples in uncountably infinite sample spaces, where this is not the case, but this theoretical point can ignored in practice
- choosing an appropriate sample space
  - regardless of their number, different elements of the sample space should be distinct and **mutually exclusive**
    - the experiment must have have a unique outcome
    - e.g. the sample space of a die cannot contain "1 or 3" as a possible outcome and "1 or 4" as another outcome, when the roll is a 1 the outcome of the experiment would not be unique
  - a given physical situation can be modeled in several different ways, depending onthe kind of questions we're interested in
  - generally, the sample space must be **collectively exhaustive**
    - i.e. no matter what happens in the experiment, we always obtain an outcome that has been included in the sample space
    - the sample space should have enough detail to distinguish between all outcomes of interest to the modeler, while avoiding irrelevant details

- example: a game where you receive $1 each time a head comes up for 10 tosses
  - only the total number of heads in a ten toss sequence matters
  - the sample space consists of ten possible outcomes 1,...,10
- example 2: a game where you receive $1 for *every* coin toss, up to and including the first time a head comes up, then the amount you get doubles each time a head comes up after
  - in this game the order of heads and tails is also important
  - a more detailed sample space is necessary, consisting of every possible ten-long sequence of heads and tails

#### Sequential Models

many experiments are sequential in character

- e.g. tossing a coin 3 times, observing stock prices for 5 subsequent days, receiving a code with 8 digits
- useful to use a **tree-based sequential description**

![](seq-tree.png)



#### Probability Laws

to complete the probabilistic model, we must introduce

- this specifies the 'likelihood' of any outcome, or any set of possible outcomes (an event)
- the probability law assigns to every event $A$ a number $P(A)$, called the probability of $A$, satisfying the following axioms:

*Probability Axioms*

| Name          | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| Nonnegativity | $P(A) \geq 0 \text{ for every event } A$                     |
| Additivity:   | If $A$ and $B$ are two **disjoint** events, then the probability of their union satisfies<br /> $P(A\cup B) = P(A) + P(B)$.<br /> Furthermore, if the sample space has an infinite number of elements and $A_{1},A_{2},\dots$ is a sequence of disjoint events, then the probability of their union satisfies<br />$P(A_{1} \cup A_{2}\cup \dots) = P(A_{1}) + P(A_{2})+\dots$ |
| Normalization | The probability of the entire sample space $\Omega$ is equal to 1, that is $P(\Omega)=1$ |

