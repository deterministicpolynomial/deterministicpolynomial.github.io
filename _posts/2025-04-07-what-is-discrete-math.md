# What Is Discrete Math? CS Fundamentals Part 1

Welcome to the first series I will be doing on this blog, called "CS fundamentals"! In this series, we will cover some of the basic principles of theoretical computer science, such as logic and set theory, discrete mathematics, big-oh notation, and much more!

---

Computer Science is built on math. Whether you are working with algorithms, automata, logic circuits, or even quantum computing, at its core we are dealing with mathematics. The mathematics that most of us learned in high school is called calculus. This is the type of math that deals with continuous change, curves, and slopes. While calculus is incredibly important and has countless applications, computer science relies heavily on a different branch of mathematics: discrete math. Discrete math focuses on distinct, separate objects rather than continuous quantities. It plays a crucial role in areas such as algorithms, data structures, cryptography, and much more. In this world of discrete math, we're working with things like whole numbers, graphs, and logical reasoning — all of which are essential for building efficient computer systems and solving complex problems. 

## What Is Discrete Math?

Discrete math is the branch of mathematics that deals with discrete objects — things that are separate and distinct. Unlike calculus, which works with continuous functions (think curves and slopes), discrete math is all about whole numbers, graphs, and structures that can be counted. This includes:

- **Sets**: Collections of objects (e.g., the set of all whole numbers).
- **Relations**: Ways in which different objects are related to each other (Person A likes Person B).
- **Graphs**: Networks of vertices and edges that can represent anything from social networks to the internet.
- **Logic**: The study of reasoning — how we draw conclusions from premises.

In essence, it’s the language you will use to design algorithms, systems, and proofs you’ll encounter in CS.

## Why Do Computer Scientists Care About Discrete Math?

Great question! Here's the deal: most of what you’ll do in computer science revolves around structures and processes that are naturally **discrete**, that is, they are countable or otherwise distinct and separable. Whether you're analyzing algorithms, working on cryptography, or designing software systems, you're almost always dealing with objects that are distinct and finite. So, discrete math provides a way to formally reason about these systems.

- **Algorithms**: Discrete math helps you understand how algorithms work, how they behave, and how they can be optimized. For instance, analyzing the time complexity of an algorithm is deeply rooted in discrete structures like sets and graphs.
  
- **Complexity**: Ever wondered why some problems are easier to solve than others? Discrete math is key to classifying problems by how “hard” they are — think of P vs NP (we’ll dive into that later, promise).

- **Proofs and Reasoning**: Without discrete math, we wouldn’t have the formal proofs that guarantee our software behaves as expected. Proofs allow us to rigorously prove the correctness and efficiency of algorithms.

## Real-World Example: Modeling a Network

To see why discrete math matters, let’s use a simple example: modeling a network. Suppose you’re working on designing a routing algorithm for a computer network. The network can be thought of as a **graph**, where each computer is a **vertex** and the connections between them are **edges**. Let us take a brief look at how we can model such a network using discrete math.

Consider a small network of 5 computers. These computers are connected as follows:

- Computer A is connected to B and C.
- Computer B is connected to A, C, and D.
- Computer C is connected to A, B, and E.
- Computer D is connected to B.
- Computer E is connected to C.

We can represent this network as a discrete object $$G = (V, E)$$, where:

- **V** is the set of **vertices** (the computers), so $$V = \{A, B, C, D, E\}$$.
- **E** is the set of **edges** (the connections between the computers), so $$E = \{(A, B), (A, C), (B, C), (B, D), (C, E)\}$$.

This graph visually looks something like this:

<p align="center">
  <img src="/assets/images/cs-fundamentals-1-graph.png" alt="Discrete Object Representing Our Graph">
</p>

Once the network is modeled in this manner, an algorithm can be developed to identify the most efficient path for data transmission between two vertices. For instance the famous [Dijkstra's algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm).

## Conclusion
Discrete mathematics is the backbone of computer science, providing the foundational tools and concepts needed to model, analyze, and optimize systems. Discrete math equips computer scientists with the formalism and precision required to solve real-world problems effectively. From graph theory and set theory to logic and reasoning, discrete mathematics is an indispensable part of the discipline. As you continue exploring these fundamental concepts, you'll find that discrete math is essential for nearly every aspect of computer science. In the next part of this series, we'll dive into an important concept in computer science: "What Is a Proof? (And What Makes It Rigorous?)" Stay tuned to see how the power of formal reasoning and proof structures plays a critical role in ensuring that algorithms and systems function correctly and efficiently.
