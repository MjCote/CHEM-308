{% include mathjax.html %}

# [Vectors and Quantum States](/Vectors-and-Quantum-States.md) 

(For a table of contents, visit the [home page](/README.md))

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


If we normalize our eigenvectors then we can be confident that they have length 1. The vector $$\vec{\alpha}$$ should be as shown in the left diagram in the figure. Notice it has length 1 and that in this $$ud$$ coordinate system it can be written (1, 0). This states that $$\vec{\alpha}$$ has projections of 1 on $$u$$ and 0 on $$d$$. Similarly, $$\vec{\beta}$$ is as shown in the middle diagram.

The point you should now pause to digest is that $$\vec{\alpha}$$ and $$\vec{\beta}$$ are the only two energy eigenvectors for this system but they are emphatically \emph{not} the only two possible states of the system.

Consider another vector in the same $$ud$$ space. Let's call it $$\vec{\psi}$$.  It is shown in the third diagram in the figure.  Since $$\vec{\psi}$$ exists in the same space as $$\vec{\alpha}$$ and $$\vec{\beta}$$, and since $$\{\vec{\alpha},\vec{\beta}\}$$ form a basis (which the figure shows to be orthonormal), we must be able to represent $$\vec{\psi}$$ as a linear combination of $$\vec{\alpha}$$ and $$\vec{\beta}$$.  The figure shows $$\vec{\psi}$$ lying midway between $$\vec{\alpha}$$  and $$\vec{\beta}$$ so it must have equal amounts of $$\vec{\alpha}$$ and $$\vec{\beta}$$ ``character.''  This is captured by the fact that when we write $$\vec{\psi}$$ as a column of numbers in the $$\vec{\alpha}$$, $$\vec{\beta}$$ basis, the two elements of $$\vec{\psi}$$ have the same absolute value. The graph also shows that $$\vec{\psi}$$ has length 1. Applying what we learned about calculating the lengths of vectors we conclude that $$\vec{\psi}$$ can be written in this $$ud$$ space as ($$\sqrt{1/2}, \sqrt{1/2})$$. The next section reminds you how to calculate vector lengths in case you need a reminder.


To reinforce the very important connections between the arrow graphics, the expression of vectors as columns of numbers, and the use of linear combinations of basis vectors, take the time to verify that the following expressions are both internally consistent and also consistent with the graphs in the figure. Don't move on to the next section until you see clearly how the elements comprised by the vectors, the expansion coefficients, and the projections in the graphs all say the same things!

$$
\eqalign{
\vec{\alpha}  &=
\begin{pmatrix}
  1 \\
  0 \\
\end{pmatrix}\\
&= 1\begin{pmatrix}
  1 \\
  0 \\
\end{pmatrix}
+ 0\begin{pmatrix}
  0  \\
  1 \\
\end{pmatrix}\\
&= 1\cdot\vec{\alpha} + 0\cdot\vec{\beta} \\
}
$$

___

$$
\eqalign{
\vec{\beta}  &=
\begin{pmatrix}
  0 \\
  1 \\
\end{pmatrix}\\
&= 0\begin{pmatrix}
  1 \\
  0 \\
  \end{pmatrix}
+ 1\begin{pmatrix}
  0 \\
  1 \\
\end{pmatrix}\\
&= 0\cdot\vec{\alpha} + 1\cdot\vec{\beta} \\
}
$$

___

$$
\eqalign{
\vec{\psi} &=
\begin{pmatrix}
   \frac{1}{\sqrt{2}} \\
 \frac{1}{\sqrt{2}} \\
 \end{pmatrix}\\
&= \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\
  0 \\
  \end{pmatrix}
+  \frac{1}{\sqrt{2}}
\begin{pmatrix}
  0 \\
  1 \\
\end{pmatrix}\\
&=  \frac{1}{\sqrt{2}}\cdot\vec{\alpha} +  \frac{1}{\sqrt{2}}\cdot\vec{\beta}\\
}
$$


|----|-----|-----|
|
$$
\eqalign{
\vec{\alpha}  &=
\begin{pmatrix}
  1 \\
  0 \\
\end{pmatrix}\\
&= 1\begin{pmatrix}
  1 \\
  0 \\
\end{pmatrix}
+ 0\begin{pmatrix}
  0  \\
  1 \\
\end{pmatrix}\\
&= 1\cdot\vec{\alpha} + 0\cdot\vec{\beta} \\
}
$$
|
$$
\eqalign{
\vec{\beta}  &=
\begin{pmatrix}
  0 \\
  1 \\
\end{pmatrix}\\
&= 0\begin{pmatrix}
  1 \\
  0 \\
  \end{pmatrix}
+ 1\begin{pmatrix}
  0 \\
  1 \\
\end{pmatrix}\\
&= 0\cdot\vec{\alpha} + 1\cdot\vec{\beta} \\
}
$$
|
$$
\eqalign{
\vec{\psi} &=
\begin{pmatrix}
   \frac{1}{\sqrt{2}} \\
 \frac{1}{\sqrt{2}} \\
 \end{pmatrix}\\
&= \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\
  0 \\
  \end{pmatrix}
+  \frac{1}{\sqrt{2}}
\begin{pmatrix}
  0 \\
  1 \\
\end{pmatrix}\\
&=  \frac{1}{\sqrt{2}}\cdot\vec{\alpha} +  \frac{1}{\sqrt{2}}\cdot\vec{\beta}\\
}
$$
|
