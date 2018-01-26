{% include mathjax.html %}

# Vectors and Quantum States

(For a table of contents, visit the [home page](/README.md))

The following discussion of the use of vectors to describe quantum states will rely heavily on the following concepts from linear algebra.  If you do not yet feel comfortable with these concepts, please brush up on the problematic areas before trying to apply them to the quantum theory.


1. Scalar multiplication of vectors
1. Addition of vectors
1. The inner product of vectors (also called dot product or scalar product)
1. Calculating the length of a vector using inner products
1. Normalizing a vector (making its length 1)
1. Basis vectors
1. Linear combination of vectors
1. Orthogonality and orthonormality
1. Projections of vectors

### Eigenvectors and Eigenvalues
Eigenvectors and eigenvalues lie at the heart of the quantum theory. Consider an $$n\times n$$ matrix $$\mathbf{O}$$ that represents a quantum mechanical operator. Because the matrix is $$n\times n$$, there will be $$n$$ eigenvectors, each of which comprises $$n$$ elements. There will also be $$n$$ eigenvalues. (Not all matrices have this property, but all the matrices that represent quantum mechanical operators do.) We can express this mathematically with a compact equation:

\begin{equation}\label{eig}
    \mathbf{O}\vec{v_i}=\lambda_i \vec{v_i}
\end{equation}

where the index $$i$$ simultanteously specifies a particular eigenvector $$\vec{v_i}$$ and its matching eigenvalue, $$\lambda_i$$. We said $$\mathbf{O}$$ is an $$n\times n$$ matrix so we expect our set of  eigenvectors to include $$\vec{v_1}, \vec{v_2}, \dots \vec{v_n}$$, and the matching set of eigenvalues to be $$\lambda_1,\lambda_2, \dots \lambda_n$$. You should think of each eigenvector and its corresponding eigenvalue as a pair---a matched set.

In the quantum theory the states of a system are encoded as vectors. More specifically, it is actually the _orientation_ of each vector that encodes a state. It is therefore important to know which mathematical operations change a vector's orientation, and which do not. Those that change a vector's orientation imply a change in quantum state while those that leaves a vector's orientation unchanged correspond to quantum mechanical processes or events that leave a quantum state unchanged.

Equation \ref{eig} says that when a matrix multiplies one of its eigenvectors the effect is equivalent to multiplying that eigenvector by a scalar (which we call its eigenvalue). But scalar multiplication of a vector only changes the vector's length, not its orientation. (Causing a vector to point in exactly the opposite direction is not considered a change in orientation for our purposes.) We can therefore conclude that when a matrix representing an observable multiplies one of its eigenvectors, it leaves the orientation of the eigenvector unchanged. This, in turn, corresponds to leaving the quantum state unchanged. It is important to remember that _only_ if the vector is an eigenvector of the matrix does multiplication by the matrix leave the vector's orientation unchanged.  This is a _special case_.  In other cases, matrix multiplication changes the vector's orientation which corresponds to a change in quantum state.

Eigenvectors and eigenvalues are particularly important when we describe making a measurement on a quantum system.  Assume for concreteness that our $$n \times n$$ matrix $$\mathbf{O}$$ corresponds to an observable property, $$O$$, of the system.   We can now state one of the central ideas in the quantum theory. Note that the newly introduced word _eigenstate_ simply refers to a state represented by an eigenvector:

> **_An idealized measurement of property $$O$$ of a system will yield one of the $$n$$ eigenvalues of the operator $$\mathbf{O}$$ as a  result. If the eigenvalue $$\lambda_{i}$$ is obtained, then after the measurement the system is left in the corresponding eigenstate,  represented by $$\vec{v}_{i}$$._**


So, if we choose to measure a system's energy, for example, the measurement will yield as a result one of the eigenvalues of the energy operator. After the measurement the system will be left in the energy eigenstate corresponding to that eigenvalue. If we choose to measure some other property, such as position, we will obtain a position eigenvalue and force the system into a position eigenstate. As we will see later, position eigenstates cannot also be energy eigenstates so if we first measure energy and then measure position we can be sure that we are forcing the system to change states as a result of our prodding.

Next up, some applications of these ideas. To continue, go to [Applications](/Applications.md).
