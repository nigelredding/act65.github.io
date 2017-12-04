---
layout: post
title: Generate a histogram efficiently
---

Suppose you have a book (with $n$ words total, not the unique count), and you want to 
make a histogram counting the frequencies of each word. If we allow a very small 
chance of failure, we can do this using $O(n)$ bits of memory and $O(n \log n)$ running time.

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
When we create a node, we set ``word`` to the word we want, ```hashval``` to the the hash
of the word, and ```count``` to ```1```.

 
