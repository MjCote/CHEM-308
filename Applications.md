{% include mathjax.html %}

# [Vectors and Quantum States](/Vectors-and-Quantum-States.md) 

## Applications
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

Rewriting the key equation from [Vectors and Quantum States](/Vectors-and-Quantum-States.md)

\begin{equation}\label{eig}
    \mathbf{O}\vec{v_i}=\lambda_i \vec{v_i}
\end{equation}

separately for each of the two eigenvectors and eigenvalues yields  

\begin{equation}\label{Hspin1}
    \mathbf{H}\vec{\alpha}=\lambda_{\alpha}\vec{\alpha}
\end{equation}

\begin{equation}\label{Hspin2}
   \mathbf{H}\vec{\beta}=\lambda_{\beta}\vec{\beta}
\end{equation}

From the previous discussion we know that equation \ref{Hspin1} implies that if we place an electron in the spin state $$\vec{\alpha}$$ and measure its energy, we will definitely obtain the energy value $$\lambda_\alpha$$.  Equation \ref{Hspin2} implies that if the electron is in the state $$\vec{\beta}$$ and we measure its energy we can be 100\% confident that we will obtain the energy value $$\lambda_\beta$$.

#### Graphical Representation
To highlight some key features of $$\vec{\alpha}$$ and  $$\vec{\beta}$$ we can use the common ``arrow'' representation of vectors.  Since our vectors each have two elements, we must use a two-dimensional space to draw them.

In this example we will define our coordinates so that our $$\vec{\alpha}$$ vector lies along the horizontal axis (labeled $$u$$ for up) and $$\vec{\beta}$$ lies along the vertical axis (labeled $$d$$ for down). We could have chosen other coordinates, as we will see later, but these are convenient for now.



![vector1](/vectors2018.png)
