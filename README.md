# Assignment 1

**COMP 596: Network Science**

_Prof Reihaneh Rabbany_

Student: Albert M Orozco Camacho

- All the code is in the `ipynb` that is next to this README. It was created on _Google Colab_,
thus, to access it, one may go to https://colab.research.google.com/drive/1IzsP4EGqJNSV770VkwIG02NWCJQp18xX
- The results are in https://drive.google.com/drive/folders/1-dmih-b748bLdJx_WthOIPFV8eKPQGKF?usp=sharing
- For the larger graphs, most of the required computation couldn't be accomplished because of RAM restrictions.
  Although, it seems that degree distributions are the overall most feasible statistic to compute.
  
------

## BONUS

_Prove that the number of the Laplacian's eigenvalues zero correspond to the number of connected components._

Let $L$ be the laplacian matrix for graph $G = (V, E)$.

Firstly, we observe that the sum of each row of $L$ always gives 0, by its definition. This implies that the vector $(1, 1, \ldots, 1)$ (where its length depends on the number of nodes $|V|$) is an _eigenvector_ of $L$ with _eigenvalue_ 0.

Now let's suppose, without loss of generality that $G$ has $c$ components, whose number of vertices are $n_1, n_2, \ldots, n_c$. Consider reordering $L$, by shifting rows, such that every two adjacent rows correspond to vertices in the same component.

By the latter operation, we can "bound" each component $n_i$ and visualize it as a box. In fact, $L$ now has the form of a box diagonal matrix, having exactly $c$ boxes.

For each block $n_i$, observe that it, itself, is the laplacian for the $i$-th component of $G$. This means that each one has _eigenvector_ $(1, 1, \ldots, 1)$ (for $n_i$ elements) with eigenvalue 0.

By construction, there are $c$ different linearly independent _eigenvectors_ with _eigenvalue_ 0 (vectors have 1 in $n_i$ positions and 0 in $k \neq i$.

Therefore $G$ has $c$ eigenvalues 0.
 
 
