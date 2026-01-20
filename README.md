# Advanced Data Structures Implementation

This repository contains custom implementations of complex data structures in **Python** and **Java**, focusing on asymptotic efficiency, memory management, and tree-balancing algorithms.

## 📂 Implementations

### 1. AVL Tree (Python) (`/AVLTree.py`)
A self-balancing Binary Search Tree (BST) that guarantees $O(\log n)$ time complexity for Lookups, Insertions, and Deletions.
* **Key Features:**
    * **Self-Balancing:** Implements `left_rotate` and `right_rotate` logic to maintain the balance factor $[-1, 0, 1]$.
    * **Rank & Select:** Supports Order Statistic operations ($k$-th smallest element) in $O(\log n)$ by augmenting nodes with subtree sizes.
    * **Range Queries:** Efficient `max_range(a, b)` function to find properties within a specific key interval.

### 2. Binomial Heap (Java) (`/BinomialHeap.java`)
A priority queue implementation optimized for merging operations.
* **Key Features:**
    * **Fast Melding:** Implements `meld()` in $O(\log n)$ to union two heaps, a distinct advantage over standard Binary Heaps ($O(n)$).
    * **Decrease Key:** Supports standard priority queue operations (`deleteMin`, `decreaseKey`).
    * **Memory Efficient:** Uses a linked-node structure (parent/child/sibling pointers) for dynamic memory usage.

## 🛠️ Complexity Analysis
| Operation | AVL Tree (Average/Worst) | Binomial Heap (Worst) |
| :--- | :--- | :--- |
| **Insert** | $O(\log n)$ | $O(\log n)$ (Amortized $O(1)$) |
| **Delete** | $O(\log n)$ | $O(\log n)$ |
| **Find Min** | $O(\log n)$ | $O(\log n)$ |
| **Meld (Union)**| $O(n)$ | **$O(\log n)$** |

## 🚀 Usage
* **Python:** Import the class: `from AVLTree import AVLTree`
* **Java:** Compile with `javac BinomialHeap.java`
