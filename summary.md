{% include mathjax.html %}

# A summary of some key ideas in the quantum theory 

(For a table of contents, visit the [home page](/README.md))


1. The state of a system is represented by a vector (or function).  In general, the vector (or function) is complex-valued.


1. Physical observables have corresponding operators which can be represented as matrices (or analytic operators).

1. The most often encountered physical observables are position, momentum, energy, angular momentum, and spin.

1. The time-dependent Schroedinger equation (TDSE) describes the time evolution of a quantum state. The equation in analytic form is

$$
   \hat{H}\Psi = i \hbar\frac{\partial{\Psi}}{\partial t}
$$

where $$\hat{H}$$ is the Hamiltonian operator---the operator corresponding to the total energy of the system.  It is given by the sum of the kinetic and potential energy operators.  The TDSE is analogous to an equation of motion encountered in classical systems.

1. A vector (or function) must be a solution to the time-dependent Schr\"{o}dinger equation in order to describe a physically realizable state.  In addition, the vector or function must be normalizable.

.1 Before writing down the elements of a vector representing a state, or writing down the elements of a matrix representing an operator, a choice of basis must be made.


.1 \label{basis1} The physical meaning of a state vector, or of an operator corresponding to an observable, does _not_ depend on the choice of basis. The system's state, or the value of an observable property, does not change if we adopt a different basis for its expression.

.1 \label{basis2} The values of the elements composing a vector or matrix \emph{does} depend on the choice of basis.  This means the vector representing a given state, or the matrix representing a given operator, can take on different forms (can have different elements) depending on the basis chosen. Combining points (\ref{basis1}) and (\ref{basis2}):  The basis choice does not affect the state described by a vector, or the observable property encoded by a matrix, but it does affect the way the vector or matrix is written.

.1 The result of an idealized measurement of some observable property of the system will always be one of the eigenvalues of the corresponding operator.  For example, if a particle's energy is measured, the experimental value obtained will be one of the eigenvalues of the energy operator.  An energy value which is not one of the eigenvalues of the energy operator will never be observed.  This is true only of idealized measurements because real measurements may not have sufficient resolution to distinguish eigenvalues with similar values.

Note: The energy operator differs from system to system, so the energy eigenvalues (the allowed energy values) vary from system to system.


.1 \label{lc} The probability of obtaining a particular eigenvalue when making a measurement is given by the squared modulus of the expansion coefficient corresponding to that eigenvalue.  For example, consider a particle in a state $$\vec{\psi}$$. To calculate the probability of obtaining a particular value when measuring momentum, the first step is to write $$\vec{\psi}$$ as a linear
combination of momentum eigenvectors,
\begin{eqnarray*}
\vec{\psi} &=& \sum_{j}c_{j}\vec{p_{j}}\\
\vec{\psi} &=& c_{1}\vec{p_{1}} + c_{2}\vec{p_{2}}+ \ldots \\
\vec{\psi} &=& \langle \vec{p_{1}}, \vec{\psi}\rangle \vec{p_{1}} +
\langle \vec{p_{2}}, \vec{\psi}\rangle \vec{p_{2}}+ \ldots
\end{eqnarray*}
where $$\vec{p_{j}}$$ is the $$j$$th eigenvector of the momentum operator, and $$c_{j}$$ is the $$j$$th expansion coefficient.  Notice that the expansion coefficients are equal to the inner products of the system's state vector with each of the basis vectors.

If $$\hat{\mathbf{P}}$$ is the momentum operator, and $$\lambda_{j}$$ is the $$j$$th momentum eigenvalue, the eigenvector and eigenvalue equation can be written

$$
\hat{\mathbf{P}}\vec{p_{j}} = \lambda_{j}\vec{p_{j}}
$$

Once the particle's state is expressed as a linear combination of momentum eigenvectors, the probability that any particular momentum eigenvalue will be obtained as a result of a momentum measurement can be calculated.  In particular, the probability that a momentum measurement will yield the value $$\lambda_{4}$$ is $$|c_{4}|^2$$.  In general, $$|c_{k}|^2$$ is the probability that a momentum measurement will yield the value $$\lambda_{k}$$.

.1 \label{welldef} The result of an individual measurement of an observable property is predictable with certainty only if the vector describing the system's state is an eigenvector of the operator for that observable.  For example, the value $$\lambda_{3}$$ (the third momentum eigenvalue) will be obtained with certainty from an individual momentum measurement only if the particle's state is $$\vec{p_{3}}$$ (the third eigenvector of the momentum operator).  To see that this follows from point (\ref{lc}), notice that if the particle is in the third momentum eigenstate, then

$$
\vec{\psi}=\vec{p_{3}}\]
$$

In this case the system's state can be expressed as the following linear combination of momentum eigenvectors,

$$
\vec{\psi} = 0\vec{p_{1}} + 0\vec{p_{2}} + 1\vec{p_{3}} +  0\vec{p_{4}}+\ldots\\
$$

Notice that only the third expansion coefficient is nonzero.
When the probability of obtaining each of the eigenvalues is evaluated,
the results are
\begin{center}
\begin{tabular}{c c}
eigenvalue & probability\\ \hline
$$\lambda_{1}$$ & $$|0|^2=0$$\\
$$\lambda_{2}$$ & $$|0|^2=0$$\\
$$\lambda_{3}$$ & $$|1|^2=1$$\\
$$\lambda_{4}$$ & $$|0|^2=0$$\\
$$\vdots$$ & $$\vdots$$\\
\end{tabular}
\end{center}
Thus, with a probability of one (certainty) the value $$\lambda_{3}$$ will be obtained if a momentum measurement is made.

.1 A matrix representing a physical observable is Hermitian. A Hermitian matrix is equal to its complex conjugate transpose.  In other words, a matrix representing a physical observable is unchanged if a combination of two operations is performed on it:  (1) its rows and columns are exchanged, and (2) any occurrences of $$i=\sqrt{-1}$$ are replaced by $$-i=-\sqrt{-1}$$.


.1 A Hermitian operator has real eigenvalues, and eigenvectors which form an orthonormalizable basis.
This is convenient because it guarantees that predicted measurement results will be real valued.  It also implies that eigenvectors of quantum mechanical operators form very convenient bases.
