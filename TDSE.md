{% include mathjax.html %}



(For a table of contents, visit the [home page](/README.md))

The equation that describes time evolution in quantum mechanics is the time-dependent Schr\"{o}dinger equation (TDSE)
\begin{equation}\label{tdse}
\mathcal{H}\Psi(x,t) = i \hbar \frac{\partial}{\partial t}\Psi(x,t)
\end{equation}
where $$\mathcal{H}$$ is the Hamiltonian operator formed by the sum of the kinetic and potential energy operators, and  $$\Psi(x,t)$$ is a time- and space-dependent wavefunction.
Since all physically realizable states are solutions to the TDSE, this equation covers the time-evolution of all states.

We previously encountered the time-_independent_ Schroedinger equation (TISE)
\begin{equation}\label{tise}
    \mathcal{H}\psi(x)=E\psi(x)
\end{equation}
whose solutions are the only states with well-defined energy.  For reasons that will become clear as you explore the time evolution of energy eigenfunctions, the energy eigenfunctions are also called _stationary states_.  Bear in mind that while the stationary states are the only solutions to the TISE, they are _not_ the only solutions to the TDSE.  Many quantum states that do not have well-defined energy, and are therefore not solutions to the TISE, are still solutions to the TDSE.  They are therefore perfectly valid quantum states.  So, in summary, a wavefunction must satisfy the TDSE to represent a physically realizable state. It must satisfy _both_ the TDSE and the TISE in order to be one of those special physically realizable states that also has well-defined energy.   Put in yet another way, all energy eigenfunctions are solutions to the TDSE, but not all solutions to the TDSE are energy eigenfunctions.

We will see that while the time-evolution of stationary states always turns out to be very simple, the time-evolution of non-stationary states can range from simple to very complicated.  To see why this is so it is easiest to begin with the stationary states.  An understanding of their behavior will shed light on the more variable non-stationary states which will be considered afterward.

### Time-evolution of stationary states

 By choosing to write the wavefunctions in equations \ref{tdse} and \ref{tise} as a function of position (and time) we are adopting the _position_ basis for our description.  This implies the Hamiltonian operator should be expressed in the position basis as well; the kinetic energy operator is expressed with the familiar second space derivative, and the potential energy operator is simply the potential energy written as a function of position.
\subsection*{Separation of Variables}
  We are looking for functions that are solutions to the time-dependent Schr\"{o}dinger equation and those functions will depend on both space and time. For example, if the wavefunction $$\Psi$$ depends on only one space dimension we could write $$\Psi$$ as a function of $$x$$ and $$t$$: $$\Psi(x,t)$$. Both a position and a time must be specified to evaluate the value of $$\Psi$$.

  It will be easiest to find suitable functions $$\Psi(x,t)$$ if we can separate the space-dependence from the time-dependence rather than tackling them together. To so we will apply a technique that we will encounter many times this semester: a separation of variables. Our goal will be to rewrite $$\Psi(x,t)$$ as a product of two functions, each of which depends on only _one_ variable. To make the notation easier to follow we will call the function that depends only on $$x$$, $$\psi(x)$$ and the function that depends only on $$t$$ will be symbolized $$T(t)$$. We therefore seek a product of functions $$\psi(x)$$ and $$T(t)$$ that is equal to  $$\Psi(x,t)$$:
  \begin{equation}\label{sep}
   \Psi(x,t) = \psi(x)\cdot T(t)
 \end{equation}
 Since we asserted at the outset that we are looking for a function $$\Psi(x,t)$$ that is a solution to the particular form of the TDSE we are working with, we are now looking for a product of two functions that solves the TDSE.

_Note carefully that there is not just a single form of the TDSE. Because the TDSE contains the hamiltonian, $$\mathcal{H}$$, which is different in different contexts, the TDSE will be different in different contexts._ The basic form of the TDSE will always be the same,
  \begin{equation}
  \mathcal{H}\Psi(x,t) = i \hbar \frac{\partial}{\partial t}\Psi(x,t)
  \end{equation}
but since the hamiltonian $$\mathcal{H}$$ for a free particle is different from that of a particle in a box which, in turn, is different from the hamiltonian for a particle in a box with a tilted bottom, we have a different TDSE for each of those contexts.


The first step after writing the time-dependent wavefunction as a product of two single-variable functions is to substitute the product of functions into the TDSE wherever $$\Psi(x,t)$$ appears.
\begin{eqnarray}
    \mathcal{H}\Psi(x,t) &=& i \hbar \frac{\partial}{\partial t}\Psi(x,t) \\
  \mathcal{H}\psi(x)\cdot T(t) &=& i \hbar \frac{\partial}{\partial t}\psi(x)\cdot T(t)
  \end{eqnarray}

We might pause at this point and notice that the reason the $$x$$-dependence can be separated from the $$t$$-dependence is that $$\mathcal{H}$$ contains only $$x$$-dependent operators such as $$-\frac{\hbar^2}{2m}\frac{\partial ^2}{\partial x^2}$$ and $$V(x)$$, while the operator on the right hand side, $$i \hbar \frac{\partial}{\partial t}$$, depends only on $$t$$. We will see as we proceed that this neat separation of time and space dependence works only when the functions we are working with are energy eigenfunctions. Fortunately, those eigenfunctions form a basis so we can use them to describe anything we'd like.

Back to the mathematical details. To perform the separation of variables we take advantage of the fact that $$T(t)$$ can be pulled out in front of $$H$$ because $$H$$ operates only on $$x$$-dependent functions.  The same logic applies to the right hand side, where $$\psi(x)$$ can be pulled in front of the time derivative. Since $$\psi(x)$$ depends only on $$x$$ and not on $$t$$ it looks like a constant as far as $$\frac{\partial}{\partial t}$$ is concerned.

After performing the allowed rearrangements we have
\begin{equation}
\frac{T(t)H\psi(x)}{\psi(x)T(t)} = \frac{\psi(x)i \hbar \frac{\partial}{\partial t}T(t) }{\psi(x)T(t)}
\end{equation}
Do not be tempted to cancel functions carelessly! Remember that you cannot cancel identical functions in the numerator and denominator if one of them is operated on by an operator such as $$H$$ or $$\frac{\partial}{\partial t}$$.  On the other hand, if the functions are simply multiplied by other functions, by constants, or by variables, then canceling is possible. Performing the allowed cancelations yields
\begin{equation}
\frac{H\psi(x)}{\psi(x)} = \frac{i \hbar \frac{\partial}{\partial t}T(t) }{T(t)}
\end{equation}
Notice that we have successfully separated the variables. The space and time dependence lie on opposite sides of the equals sign.

We now apply a key argument in the separation of variables technique.  We have two sides of an equation that each depend exclusively on a different variable. \textbf{The only way the $$x$$-dependent left hand side and the $$t$$-dependent right hand side can be equal, no matter which values of $$x$$ or $$t$$ we might consider, is if both sides of the equation are equal to one and the same constant.} Think that through before proceeding; it is an important point.  We will call the constant $$E$$ in this case, for reasons that will become clear in a moment.  At this point we have
\begin{equation}
\frac{H\psi(x)}{\psi(x)} = \frac{i \hbar \frac{\partial}{\partial t}T(t) }{T(t)} = E
\end{equation}

We can now consider separately the two expressions that we assert are equal to $$E$$.  After a bit of rearrangement we're left with
\begin{eqnarray}
H\psi_n(x) &=& E_n\psi_n(x)\label{TISE}\\
\frac{\partial}{\partial t}T(t) &=& (-iE_n/\hbar)\,T(t) \label{time}
\end{eqnarray}
where we've made use of the fact that $$1/i = -i$$.

First consider equation \ref{TISE}. This is just the familiar time-independent Schr\"{o}-dinger equation.  Its solutions are the energy eigenfunctions, which from now on we will also call stationary states.  Their form depends on the form of the potential energy operator in the Hamiltonian.  Once the potential energy function is specified, the set of  functions, $$\{\psi_n(x)\}$$, and the corresponding set of energy eigenvalues, $$\{E_n\}$$, can be found.

Equation \ref{time} also has a familiar form. It is solved by a function whose derivative is equal to the same function multiplied by a constant.  We have seen before that some exponential functions possess this property.  Taking the derivative of an exponential function yields the original exponential function, times the derivative of whatever appears in the exponent. So if the exponent is just a collection of constants times the variable, then the derivative of the exponential function will simply be the function multiplied by the collection of constants.   In the current problem we see that the constants we expect to obtain  are $$-i E_n/\hbar$$.  Since the variable is $$t$$, the exponential functions that satisfies equation \ref{time} have the form
\begin{equation}\label{time2}
T_n(t) =  e^{-i E_n t/\hbar}
\end{equation}
where the values of $$E_n$$ are the energies of the states $$\psi_n(x)$$ that are solution to the TISE.  Notice that if $$\psi_n(x)$$ weren't an energy eigenstate, there would be no well-defined energy value to insert into the right-hand side of equation \ref{time2}.  _We conclude that  equation \ref{time2} only describes the time evolution of stationary states_---the only states that have well-defined energy.  We will be unable to find a similarly simple expression describing the time evolution of states that are not represented by eigenfunctions of the energy operator.  We can still describe the time evolution of such nonstationary states, but the energy and position dependence will not be neatly separable as they are here.

Putting the separation of variables results back together, we obtain an expression describing the space- and time-dependence of any state $$\Psi_n(x,t)$$ that has well-defined energy
\begin{equation}
\Psi_n(x,t) = \psi_n(x)e^{-iE_nt/\hbar}
\end{equation}
The space-dependence is contained in $$\psi_n(x)$$, which satisfies $$H\psi_n=E_n\psi_n$$, and the time-dependence is contained in the $$e^{-iE_nt/\hbar}$$.
The key point is that in the case of stationary states---and _only_ in the case of stationary states---the space- and time-dependence are separable.  That means a plot of the wavefunction at any time looks like the plot at any other time, except that it may be rotated in the complex plane as a result of the $$e^{-iE_nt/\hbar}$$ factor.  The frequency of that rotation, $$\omega_n$$, is given by $$\omega_n =E_n/\hbar$$, which has units of rad$$\cdot$$s$$^{-1}$$ (radians per second).  Notice the very important fact that the rotation rate in the complex plane is higher for high energy states than it is for low energy states.  This fact has major implications for chemistry.

### Non-stationary states
If we want to explore the time evolution of _non_-stationary states---wavefunctions that are not solutions to the time independent Schroedinger equation---we have two approaches at our disposal.  The first is to express any state of interest as a linear combination of stationary states (whose time evolution we've already worked out).  The second approach is to use numerical methods, implemented using software such as Matlab.  Approaching the problem numerically, we discretize both space and time, and then make animated plots of $$\Psi$$ showing how it changes over time.  Before turning to the numerical methods let's briefly apply the analytical approach.

Hamiltonian operators are hermitian. This means that the eigenvectors of any given Hamiltonian form  an orthonormalizable basis which we can use to express any other vector in the same space. (We clearly can't use the energy eigenstates of a particle in a one-dimensional box to describe the states of an electron in a three-dimensional atom, for example.)  Given the orthonormal set of energy eigenvectors as a basis, we can write the vector describing an arbitrarily chosen state $$\Psi$$ (written here as a vector) as a linear combination of the energy eigenvectors, $$\Psi_{j}$$
\begin{equation}
\Psi = c_{1}\Psi_{1}+c_{2}\Psi_{2}+c_{3}\Psi_{3}+\dots
\end{equation}
Having expressed $$\Psi$$ in the stationary state basis we can easily incorporate its time dependence.  We just worked out the time dependence of each of the basis vectors;  those are the states whose space and time dependence are separable.  We need only tack on a factor of $$\exp(-iE_j t/\hbar)$$ to each basis vector, where $$E_j$$ is the energy eigenvalue associated with the $$j$$th eigenvector.
\begin{equation}
\Psi = c_{1}\Psi_{1}e^{-iE_{1}t/\hbar}+c_{2}\Psi_{2}e^{-iE_{2}t/\hbar}+c_{3}\Psi_{3}e^{-iE_{3}t/\hbar}+\dots
\end{equation}
Each stationary state vector evolves in time by rotating in the complex plane at its own rotational frequency of $$\omega_{j}=E_{j}/\hbar$$ where $$E_{j}$$ is the energy of $$\Psi_{j}$$.  The time evolution of the overall state $$\Psi$$ can then be viewed as the result of the time-varying constructive and destructive interference among the various energy eigenstates as they rotate at their own individual energy-determined rates.  As a result of all the interferences that are possible, very complicated time evolution of the overall state $$\Psi$$ can result even though the rotation of each individual energy eigenvector is very simple. 
