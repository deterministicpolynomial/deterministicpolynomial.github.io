# What Is a Proof? (And What Makes It Rigorous?) CS Fundamentals Part 2

Welcome back to the CS Fundamentals series! In [Part 1]([2025-04-07-what-is-discrete-math.md](https://deterministicpolynomial.github.io/2025/04/07/what-is-discrete-math.html)), we took a look at discrete mathematics — the language of computer science. We explored how CS problems are built on **discrete structures** like graphs, sets, and logic. This time, we’re diving into something equally foundational: **proofs**.

---

Computer science is full of big ideas: algorithms that sort, compress, or encrypt; programs that control airplanes or diagnose diseases. But how do we know these ideas actually work? How can we be sure an algorithm always returns the right answer? That a function always finishes running? That a security system can’t be broken?

We don’t just guess. We **prove** it.

Proofs are the tools we use to reason rigorously. They’re the formal backbone behind correctness, safety, and efficiency. Whether you’re designing an algorithm, analyzing a data structure, or studying computation itself, you’ll run into proofs all the time.

## What Is a Proof?

At its core, a **proof** is a structured argument that shows why something must be true. It starts from a set of known facts — definitions, assumptions, or earlier results — and uses **logical steps** to reach a conclusion.

Think of it like writing a recipe: each step must follow logically from the previous one, and by the end, you’ve baked a guaranteed result.

A good proof gives us certainty. It says, “This algorithm works — not just on the test cases I tried, but on *all* valid inputs.”

## Why Do Computer Scientists Care About Proofs?

Proofs matter because **certainty matters**. In computer science, we often want to know things like:

- Will my algorithm always return the correct output?
- Will my program always terminate?
- Is this problem solvable, or is it fundamentally impossible?
- Can this encryption be broken?

These aren’t things you can answer with a few test cases. You need to **prove** it.

Here’s where proofs show up in real-world computer science:

- **Correctness**: Proving your code works for every valid input, not just the ones you’ve tested.
- **Complexity**: Proving your algorithm runs in O(n log n) time — not just “seems fast enough.”
- **Security**: Proving your cryptographic scheme is as strong as a well-known hard problem.
- **Termination**: Proving that recursive calls eventually bottom out.

In short: proofs give us confidence. And confidence is critical when systems scale, fail, or affect real lives.

## Types of Proofs

Let’s break down a few common proof techniques you'll see over and over in CS:

### 1. **Direct Proof**
This is the simplest version of a proof. We start from known truths and logically work toward the thing you want to prove. Clean, straightforward, and often your first go-to.

> **Example**: Proving that the sum of two even numbers is even.  
> Let $$a = 2m$$ and $$b = 2n$$. Then:  
> $$a + b = 2m + 2n = 2(m + n)$$ — which is divisible by 2. Done!

### 2. **Proof by Contradiction**
This is intuitively quite a simple technique, but it is surprisingly powerful. We assume that the opposite of what we want to prove is true, and show that this leads to something impossible or absurd. Hence, our assumption must be false, and we have proven our statement. Because of the absurd nature of the eventual contradiction, this type of proof is sometimes called **reductio ad absurdum**.

> **Example**: Proving that $$\sqrt{2}$$ is irrational.  
> 
> Assume the opposite: that $$\sqrt{2}$$ *is* rational.  
> That means we can write it as a fraction $$\frac{a}{b}$$ in lowest terms, where $$a$$ and $$b$$ are integers with no common factors.  
> 
> Then:
> $$\sqrt{2} = \frac{a}{b} \Rightarrow 2 = \frac{a^2}{b^2} \Rightarrow a^2 = 2b^2$$
>
> So $$a^2$$ is even, which implies $$a$$ is even (because the square of an odd number is odd).  
> Let $$a = 2k$$ for some integer $$k$$. Then:
> $$a^2 = (2k)^2 = 4k^2$$
>
> Substituting back in:
> $$4k^2 = 2b^2 \Rightarrow 2k^2 = b^2$$
>
> This implies $$b^2$$ is even, and thus $$b$$ is even as well.  
> 
> But now both $$a$$ and $$b$$ are even — which contradicts our assumption that $$\frac{a}{b}$$ was in lowest terms!  
> Therefore, our assumption must be false, and $$\sqrt{2}$$ is irrational.

Proof by contradiction often comes in handy when the direct path is hard to see. It lets us work backward from the “wrong world” until something breaks — revealing that our original claim must have been right all along.

### 3. **Proof by Contrapositive**
Instead of proving “if A, then B,” you prove “if not B, then not A.” These are logically equivalent, but one is sometimes much easier to work with.

### 4. **Proof by Induction**
Mathematical induction is one of the most used, and most powerfull proving techniques. It is especially applicable when reasoning about recursion, loops, or data structures like trees.

We’ll cover induction in more depth in a later post, but here’s the general idea. Mathematical induction is a method for proving that a statement $$P(n)$$ is true for every natural number $$n$$, that is, that the infinitely many cases $$P(0),P(1),P(2),P(3),...$$ all hold. This is done by first proving a simple case, then also showing that if we assume the claim is true for a given case, then the next case is also true. Informal metaphors help to explain this technique, such as falling dominoes or climbing a ladder. The idea is that we can climb as high as we want on the ladder, by proving that we can climb onto the bottom rung, and that from each rung we can climb up to the next one.

## Proofs in the Bigger Picture

Proofs aren’t just for showing your homework is right — they’re a cornerstone of **theoretical computer science**. Every field uses them:

- **Algorithms**: Proving correctness, bounds, and guarantees.
- **Cryptography**: Proving hardness and security.
- **Formal verification**: Proving programs behave exactly as specified.
- **Computability theory**: Proving what can and can’t be computed at all.

As you go deeper into CS, you’ll see that the best engineers, researchers, and developers don’t just know *how* things work — they know *why*.

## Conclusion

Proofs are more than math exercises — they’re what let us build systems we can trust. In a world full of complexity, ambiguity, and edge cases, proofs give us something rock solid: certainty. Whether you're proving that an algorithm terminates, that a function sorts correctly, or that a security protocol holds up under attack — formal reasoning is your best friend. In the next part of this series, we’ll take a deeper look at **mathematical induction** — one of the most powerful tools in a computer scientist’s toolkit. It’s how we reason about recursion, loops, and sequences — and it’s used everywhere from algorithm analysis to automata theory.
