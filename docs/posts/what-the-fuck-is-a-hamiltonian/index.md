<!--
.. title: What the fuck is a Hamiltonian?
.. slug: what-the-fuck-is-a-hamiltonian
.. date: 2021-10-10 09:50:01 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. has_math: true
.. type: text
-->

<!-- TEASER_END -->

Hamiltonian describes dynamics of a quantum mechanical system.
It pops up in a lot of seemingly unrelated places, but its occurrence usually hints there's the notion of energy involved.

Knowing how Hamiltonian looks like for a system is useful because:

- We can solve the Schrödinger Equation. Not very useful on its own, but almost everything else in Quantum Mechanics follows from this.

{{% lmath display=true %}}
H \ket{ \psi(t) } = i \hbar \frac{d}{dt} \ket{ \psi(t) } \\

\dots \\

\ket{ \psi(t) } =\ ?

{{% /lmath %}}

- We can track how the state of the system changes through time (time evolution).

{{% lmath display=true %}}
\ket{ \psi(t) } = e^{-i H t} \ket{ \psi(0) } 
{{% /lmath %}}


- We can calculate what would be expectation value of *the energy* of the system in a given state. It's an expectation value, not a single definite value, because the energy is a random variable. If you had an experiment where you would measure the energy of the system, this would be the mean of the results:

{{% lmath display=true %}}

E[E(\ket{\psi})] = \bra{\psi} H \ket{\psi}

{{% /lmath %}}

- We can calculate *what state* yields the minimum expected energy.

{{% lmath display=true %}}

\psi_{min} = \underset{\psi}{argmin}\ E[E(\ket{\psi})]

{{% /lmath %}}

All of the above can be summed up by stating that the Hamiltonian is a quantum operator associated with the system energy ([ref](http://hyperphysics.phy-astr.gsu.edu/hbase/quantum/hamil.html)).


# Discrete systems

If the system under consideration consists of discrete variables the Hamiltonian is a matrix.

$$
H = 
\begin{bmatrix}
1 & 2 & 3 & 4 \\\\
1 & 2 & 3 & 4 \\\\
1 & 2 & 3 & 4 \\\\
1 & 2 & 3 & 4
\end{bmatrix}
$$

The eigenvectors of this matrix provide an orthonormal basis for the state Hilbert space; the eigenvectors span the state space.
Corresponding eigenvalues give the allowed energy levels of the system ([ref](https://en.wikipedia.org/wiki/Hamiltonian_(quantum_mechanics)#Dirac_formalism)).

