{% include mathjax.html %}

# Vectors and Quantum States


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
We mentioned previously that eigenvectors and eigenvalues lie at the heart of the quantum theory. Let's revisit what we have mentioned already but go into a bit more detail.

Consider an $$n\times n$$ matrix $$\mathbf{O}$$ that represents a quantum mechanical operator. Because the matrix is $$n\times n$$, there will be $$n$$ eigenvectors, each of which comprises $$n$$ elements. There will also be $$n$$ eigenvalues. (Not all matrices have this property, but all the matrices that represent quantum mechanical operators do.) We can express this mathematically with a compact equation:

\begin{equation}\label{eig}
    \mathbf{O}\vec{v_i}=\lambda_i \vec{v_i}
\end{equation}

where the index $$i$$ simultanteously specifies a particular eigenvector $$v_i$$ and its matching eigenvalue, $$\lambda_i$$. We said $$\mathbf{O}$$ is an $$n\times n$$ matrix so we expect our set of  eigenvectors to include $$\vec{v_1}, \vec{v_2}, \dots \vec{v_n}$$, and the matching set of eigenvalues to be $$\lambda_1,\lambda_2, \dots \lambda_n$$. You should think of each eigenvector and its corresponding eigenvalue as a pair---a matched set.

We  said previously that in the quantum theory the states of a system are encoded as vectors. We will now be more specific.  It is actually the _orientation_ of a vector that encodes a state.  That is why it is important to know which mathematical operations leave a vector's orientation unchanged: changing a vector's orientation implies a change in quantum state.  Conversely, a mathematical operation that leaves a vector's orientation unchanged corresponds to a quantum mechanical process or event that leaves a quantum state unchanged.

Equation \ref{eig} says that when a matrix multiplies one of its eigenvectors the effect is equivalent to multiplying that eigenvector by a scalar (which we call its eigenvalue). But scalar multiplication of a vector only changes the vector's length, not its orientation. (Causing a vector to point in exactly the opposite direction is not considered a change in orientation for our purposes.) We can therefore conclude that when a matrix representing an observable multiplies one of its eigenvectors, it leaves the orientation of the eigenvector unchanged. This, in turn, corresponds to leaving the quantum state unchanged. It is important to remember that _only_ if the vector is an eigenvector of the matrix does multiplication by the matrix leave the vector's orientation unchanged.  This is a _special case_.  In other cases, matrix multiplication changes vector orientation which implies a change in quantum state.

Eigenvectors and eigenvalues are particularly important when we describe making a measurement on a quantum system.  Assume for concreteness that our $$n \times n$$ matrix $$\mathbf{O}$$ corresponds to an observable property, $$O$$, of the system.   We can now state one of the central ideas in quantum theory. Note that the newly introduced word _eigenstate_ simply refers to a state represented by an eigenvector:

> **_An idealized measurement of property $$O$$ of a system will yield one of the $$n$$ eigenvalues of the operator $$\mathbf{O}$$ as a  result. If the eigenvalue $$\lambda_{i}$$ is obtained, then after the measurement the system is left in the corresponding eigenstate,  represented by $$\vec{v}_{i}$$._**


So, if we choose to measure a system's energy, for example, the measurement will yield as a result one of the eigenvalues of the energy operator. After the measurement the system will be left in the energy eigenstate corresponding to that eigenvalue. If we choose to measure some other property, such as position, we will obtain a position eigenvalue and force the system into a position eigenstate. As we will see later, position eigenstates cannot also be energy eigenstates so if we first measure energy and then measure position we can be sure that we are forcing the system to change states as a result of our prodding.


### Applications
#### Orbitals and Energy Levels
You are already familiar with some of these concepts, but may not have encountered them expressed in the language of linear algebra.  For example, the energies of the levels available to an electron in a hydrogen atom are the _eigenvalues_ of the energy operator for a hydrogen atom.  The orbitals of the hydrogen atom are the states with well defined energy.  They are the _energy eigenstates_---the states represented by eigenvectors of the hydrogen atom energy operator.

Since there are an infinite number of energy levels and orbitals, the energy operator for the hydrogen atom must be represented by an $$\infty\times \infty$$ matrix.  Fortunately we can usually truncate this matrix when tackling chemical problems, and focus on a small subset of the energy levels and orbitals (energy eigenvalues and eigenstates).

#### Electron Spin
We are now ready to apply all this to a (superficially) simple system. Every chemistry student has encountered the fact that electrons are said to have two spin states with well-defined energy, "spin up" and "spin down." In the simplest level of description we think of these two states as corresponding to the particle's magnetic dipole being aligned with or against an external magnetic field, respectively. (Later we will refine this description of the orientation of a magnetic moment with respect to particular axes.) Because there are only two states with well-defined energy we can immediately draw the following conclusions:

  * Energy in this system is represented by a 2 $$\times$$ 2 matrix
  * There are two energy eigenvectors
  * Each eigenvector has two elements
  * There are two energy eigenvalues.


We can now rewrite our eigenvector equation as it applies to this situation.  First we adopt the following mathematical notation:

|:----:|-----|
| $$\mathbf{H}$$ | total energy operator, or hamiltonian operator |
|  $$\vec{\alpha}$$ | vector representing a spin up electron |
|  $$\lambda_{\alpha}$$ | energy of an electron in the spin up state  |
|  $$\vec{\beta}$$ | vector representing a spin down electron |
|  $$ \lambda_{\beta}$$ |  energy of an electron in the spin down state |

Rewriting equation \ref{eig} separately for each of the two eigenvectors and eigenvalues yields  
\begin{equation}
    \mathbf{H}\vec{\alpha}=\lambda_{\alpha}\vec{\alpha}\label{Hspin1}\\
   \mathbf{H}\vec{\beta}=\lambda_{\beta}\vec{\beta}\label{Hspin2}
\end{equation}

From the previous discussion we know that equation \ref{Hspin1} implies that if we place an electron in the spin state $$\vec{\alpha}$$ and measure its energy, we will definitely obtain the energy value $$\lambda_\alpha$$.  Equation \ref{Hspin2} implies that if the electron is in the state $$\vec{\beta}$$ and we measure its energy we can be 100\% confident that we will obtain the energy value $$\lambda_\beta$$.

#### Graphical Representation
To highlight some key features of $$\vec{\alpha}$$ and  $$\vec{\beta}$$ we can use the common ``arrow'' representation of vectors.  Since our vectors each have two elements, we must use a two-dimensional space to draw them.

In this example we will define our coordinates so that our $$\vec{\alpha}$$ vector lies along the horizontal axis (labeled $$u$$ for up) and $$\vec{\beta}$$ lies along the vertical axis (labeled $$d$$ for down). We could have chosen other coordinates, as we will see later, but these are convenient for now.
![alt text][vector1]
[vector1]: https://github.com/MjCote/Quantum-Chaos/blob/master/vectors2018.png "vector1 graphic"
