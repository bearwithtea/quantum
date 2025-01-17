## Single Systems
### Classical Information
The mathematical descriptions between [classical](https://www.techtarget.com/whatis/definition/classical-computing) and quantum computer are more similar than they are distinct.
* Classical also acts as a simple point of reference when approaching quantum ideas.

It is hard to understand quantum information without understanding classical information.
#### Classical States & Probability Vectors
Suppose that we have a system that stores information with a *limited* number of classical states.
* A **classical state** is a configuration that can be recognized and described unambiguously. 
	* This is usually represented either as a $1$ or a $0$.

In mathematical terms, the specification of the class ical states of a system are the starting point: we *define* a bit to be a system with the classical states $0$ or $1$.

A **classical state set** is finite and nonempty where:
1. $X$ is the name of the system being considered.
2. $\sum$ is the set of classical states of $X$.

If $X$ is a bit, then $\sum = \{0, 1\}$.
* This is the *binary alphabet*.

When thinking about $X$ as a carrier of information, the different classical states of $X$ could be assigned certain meanings, leading to different outcomes or consequences.
* In these cases, it is sufficient to describe $X$ as simply being in one of its classical state

However, in many cases, knowledge is uncertain and one way to represent out knowledge of the classical state of a system $X$ is to associate *probabilities* with its different possible classical states, resulting in a **probabilistic state**. 

Suppose $X$ is a bit and based on what we know or expect about what has happened to $X$ in the past, we might believe that $X$ is in the classical state $0$ with $3/4$ probability, and in the $1$ state with $1/4$ probability.
* This can be shown at $Pr(X = 0) = \frac{3}{4}$ and $Pr(X=1)=\frac{1}{4}$ or, more succinctly $\left( \begin{array}{c} \frac{3}{4} \\ \frac{1}{4} \end{array} \right)$.
In general, it is possible to represent a probabilistic state, like the one above, having any classical state set in the same way: as a vector of probabilities (**probability vectors**).
* There are two constraints for this:
	1. All entries of the vectors are *nonnegative real numbers*.
	2. The sum of the entries is equal to $1$.

The advantage of representing these probabilistic states in such a way is that they can be manipulated with *[matrix-vector multiplication](https://en.wikipedia.org/wiki/Matrix_multiplication)*.
#### Measuring Probabilistic States
**Measuring** a state can be abstracted to <u>looking at a system and recognizing whatever classical state is is in without unambiguity</u>.
* We cannot “see” a probabilistic state of a system; when we look at it, we just see one of the possible classical states.

By measuring a system, we can change our knowledge of it, and therefore the probabilistic state we associate with it can change.
* If we recognize that $X$ is in the classical state $a \in \sum$, then the new probability vector representing our knowledge of the state of $X$ becomes the vector having a $1$ in the entry corresponding to $a$ an and $0$ for all other entries.
	* $\sum$ → all possible classical states that $X$ could be in.
	* $a$ → what $X$ becomes when it is observed.
		* Therefore, $X$ is in the classical state $a$ because the system collapsed into a $1$.
			* This is represented by a “ket” notion ($\vert a \rangle$), which describes a **basis state** or **quantum state vector**.

In our system, the standard basis vectors are given by $\vert 0 \rangle = \left( \begin{array}{c} \frac{1}{0}\end{array} \right)$ and $\vert 1 \rangle \left( \frac{0}{1} \right)$ 
* For $\vert 0 \rangle$, the quantum state $0$ is represented by $1$ in the first position.
	* These can be combined to represent a two-dimensional column vector as a linear combination between these two vectors as such: $\left( \begin {array}{c} \frac{3}{4} \\ \frac{1}{4} \end{array}\right) = \frac{3}{4}\vert0\rangle + \frac{1}{4}\vert1\rangle$ . 
		* This naturally generalizes to any classical state set: any column vector can be written as a linear combination of standard basis states.

In another example, the classical state of our set is $\{\text{heads},\text{tails}\}$, represented as $\vert\text{heads}\rangle=\left(\frac{1}{0}\right)\text{ and } \vert\text{tails}\rangle(\frac{0}{1})$.
* If we were to uncover the coin and look at it, the result would, obviously, be either heads or tails. If the result was tails, we could update our description of the probabilistic state of the coin so that it becomes $\vert\text{tails}\rangle$.
	* If we were to cover up the coin again and then uncover it, the classical state would still be tails, meaning that the probabilistic state is consistent with the vector $\vert\text{tails}\rangle$.

While this might seem trivial, quantum states behave in entirely analogous ways but their measurement properties are strange.
* Establishing the analogous properties of classical systems, the way quantum information works might seem less unusual.