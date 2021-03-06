{% include mathjax.html %}

# [Vectors and Quantum States](/Vectors-and-Quantum-States.md) 

(For a table of contents, visit the [home page](/README.md))

## Lengths of Vectors and the Inner Product

We emphasized that it is the orientation of a vector that encodes a quantum state.  The vectors $$\vec{\alpha}$$, $$2\vec{\alpha}$$, and $$-5\vec{\alpha}$$, all represent the same state because the vector orientations are the same; only the lengths are different.  Nonetheless, we will have to pay attention to vector lengths in some situations.  The Pythagorean theorem provides a way to measure the length of a vector, and the inner product is a more compact and easily generalizable alternative we will make more use of.

To use the Pythagorean formula to measure vector length, consider the arrow representing a vector to be the hypotenuse of a right triangle.  If we know the length of the arrow's projection onto each of the perpendicular axes defining the coordinate system then we can easily calculate the vector's length.  If we have a vector $$\vec{v} = (u,d)$$, its length is written $$\parallel\vec{v}\parallel$$, can can be computed by $$\parallel\vec{v}\parallel=\sqrt{u^{2}+d^{2}}$$.  By rewriting the squared terms as products we can emphasize an important feature of the length calculation.  Both forms are shown below.

$$
\eqalign{
\parallel\vec{v}\parallel &= \sqrt{u^{2}+d^{2}}\\
&= \sqrt{uu+dd} 
}
$$

The last form of the expression, in which $$uu$$ and $$dd$$ are used rather than $$u^2$$ and $$d^2$$, can be read as a manifestation of our mantra for multiplying vectors: "multiply corresponding elements and add up."   This serves to remind us that a more compact notation is available:

\begin{equation}\label{eq2}
\parallel\vec{v}\parallel=\sqrt{\langle \vec{v},\vec{v} \rangle}
\end{equation}

where the angle bracket notation indicates an "inner product" or "scalar product" of vectors.  To compute an inner product we must perform three operations.(Notice that in this case we're taking the inner product of the vector $$\vec{v}$$ with itself, but we can also take the inner product of two different vectors, as long as they have the same number of elements.)  First, transpose the vector written on the left so that it becomes a row vector. Then take its complex conjugate, which simply means replace $$i=\sqrt{-1}$$ with $$-i=-\sqrt{-1}$$ everywhere $$i$$ appears. Here we're only using real numbers so complex conjugation leaves the left vector unchanged. Finally, perform the usual vector multiplication.  Writing out the steps we obtain

$$\eqalign{
\parallel\vec{v}\parallel &= \sqrt{\langle \vec{v},\vec{v} \rangle}\\
&=\sqrt{
\begin{pmatrix}
u^{\star} & d^{\star} \\
\end{pmatrix}
\begin{pmatrix}
  u \\
  d \\
\end{pmatrix}} \\
&=\sqrt{u^{\star}u+d^{\star}d}
}$$

where the star superscript implies complex conjugation.  Notice that we end up with the same result we obtained using Pythagoras's approach.  When we have vectors with more than two elements, the advantage of using the inner product will become obvious.  For now, to be sure you're keeping track of everything, try applying the inner product method to determine the lengths of the three vectors shown in the following figure.  If all goes well you should find that the lengths of all three vectors are 1.

![vector1](/vectors2018.png)

#### Normalization
We can make the length of any vector 1 by dividing the vector by its own length.  This process is called _normalization_ and we will perform it often.  Given a vector $$\vec{v}$$ with length $$ \parallel \vec{v}\parallel$$ we can create a new vector $$\vec{w}$$ with the same orientation as $$\vec{v}$$ but with length 1:

\begin{equation}
    \vec{w} = \frac{\vec{v}}{\parallel\vec{v}\parallel}
\end{equation}

Since the new vector has the same orientation as the original one, both vectors represent the same state.  However, the new normalized vector has the advantage that it can be used directly  to calculate the probabilities of measurement results---our next topic. 
