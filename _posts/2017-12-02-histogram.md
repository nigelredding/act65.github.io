---
layout: post
title: Random binary trees and histograms
---
NB: This is a draft.
    See https://github.com/nigelredding/histogram for the code.

Suppose you have a book (with $n$ words total, not the unique count), and you want to make a histogram counting the frequencies of each word. If we allow a very small chance of failure, we can do this using $O(n)$ bits of memory and $O(n \log n)$ running time.

Let $h$ be a $p=64$ bit hash function. Create a tree where each node is given by
```go
type Tree struct {
        word  string
        hashval  uint64
        count uint64
        left  *Tree
        right *Tree
}
```
When we create a node, we set ``word`` to the word we want, ```hashval``` to the the hash of the word, and ```count``` to ```1```. We call the first three items of the struct the "word data".

We start by putting the word data of the first word of the book in a root node. Then, we iterate through every word of the book. We insert into the binary tree in the usual way with respect to ```hashval```, except that if we hit a hash of the same value, we increase the counter by ```1```. If the hash is less than the root hash, insert on the left. If they are equal, increase ```count``` by one. If it's greater, insert on the right. Repeat recusively.

Then we've got our book in our tree. $O(n)$ bits of space were used. How long did it take to insert each item? We'll set up some machinery to solve this problem. In the end we show that after the insertion of the entire book, the expected depth is $O(\log n)$. From this we conclude that inserting all elements of the book takes $O(n \log n)$ expected running time.

For the sake of discussing memory and running time, we can assume the all the words are unique. Repetitions do not change the shape of the resulting tree,
and multiple elements are only stored once. We can further assume that if there are $n$ unique words, then inserting the book (in its order)
gives the same binary tree (in shape) as inserting some specific permutation of $\{1,2,\ldots,n\}$. We discuss this below. 


## Random Binary trees

Suppose $S=\\{1,2,\ldots,n\\}$. For each permutation $\pi$ of $S$ there is an $n$-tuple $S_\pi = (\pi(1), \pi(2), \ldots, \pi(n))$. There is also a corresponding binary tree $T_\pi$, which is the binary tree formed by inserting all the entries in the order of $S_\pi$. Clearly different permutations can correspond to the same binary tree.
Our goal is to show that the expected depth of any tree is $O(\log n)$.

Fix some $x \in S$. For each $i \in S \setminus \{x\}$, we can let $I_i$ be the random variable given by

$$
I_i(\sigma)  =
\begin{cases}
	1 & \text{if $i$ appears in the search path for $x$ in $T_\sigma$} \\
	0 & \text{otherwise}
\end{cases}
$$

What is the probability that $I_i=1$? In other words, what is the probability that
$i$ is on the search path of $x$? We could use a counting argument (**haven't tried it yet, do this**), but instead we'll
use a trick from [here](http://opendatastructures.org/versions/edition-0.1d/ods-java/node40.html).
First suppose $1 \leq i < x$. Let $[i,x]$ denote the intererval $\\{i,i+1,\ldots,x\\}$. 
A moment of thought will reveal that $I_i=1$ if and only if $i$ is the first element from $[i,x]$
to be inserted. Each element from $[i,x]$ has an equal chance of $(x-i+1)^{-1}$ of being inserted first. So $P(I_i=1)=(x-i+1)^{-1}$.
The similar argument shows that if $x < i \leq n$ then $P(I_i=1)=(i-x+1)^{-1}$. Hence

$$
P(I_i=1) =
\begin{cases}
        (x-i+1)^{-1} & \text{if } 1 \leq i < x \\
        (i-x+1)^{-1} & \text{otherwise}
\end{cases}
$$

Which imediately implies (as there are only two outcomes, $0$ and $1$) that for each $1 \leq i \leq n$,
we have $E[I_i] = P(I_i=1)$. 

Then we have a random variable $L_x$ which gives the length of the search path from the root to $x$, which is given by
\\[
L_x(\sigma) = \sum\limits_{i \in \\{1,2,\ldots,n\\} \setminus \\{x\\}} I_i
\\]

By the linearity of expectations, we get

$$
	E[L_x] = \sum\limits_{i=1}^{x-1} E[I_i] + \sum\limits_{j=x+1}^n E[I_j]
$$

Recall that the sum $H_k := \sum_0^k i$ is called the $k$-th *Harmonic number*. By computing upper
and lower Reimann sums, we can show 
that for any $k>0$, we have

\\[
	\ln k \leq H_k \leq \ln k + 1
\\]

Rewriting our sum, we get 

\\[
	E[L_x] = H_x + H_{n-x+1}-2
\\]

So by our inequality

\\[
	\ln(x) + \ln(n-x+1) -2 \leq E[L_x] \leq 2\ln(n)
\\]

## The program, again
So we've shown that the inserting all words in a book has an expected running time of $O(n \log n)$. 
So, if the data is uniformly distributed, we don't need any other techniques (like
self-ballancing trees) to insert the data efficiently.

Let's try our program out:

```bash
go run histogram.go leviathan.txt out.txt
```

which gives us a histogram
```bash 
the 15144
of 10986
hobbes 15
produced 14
white 5
where 334
perhaps 33
hindreth 1
instant 2
reconning 1
experiment 1
agenor 1
infinitive 1
covetousness 1
ordeyned 1
anxiety 4
infinitely 1
.
.
.
```
