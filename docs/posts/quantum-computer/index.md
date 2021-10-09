<!--
.. title: Quantum computer
.. slug: quantum-computer
.. date: 2021-10-06 21:30:20 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

<!-- TEASER_END -->

A quantum computer is a machine that lives in a remote datacenter.
You send it quantum circuits and it returns you series of measurements.

This is the input:

<!-- Hardware efficient ansatz. Src: https://quantaggle.com/algorithms/ansatz/ -->
![](/images/HEA.png)

Measurement of each qubit yields `0` or `1`.
Measuring multiple qubits yields a bitstring, like `0010` or `1010`.
You tell the quantum computer to run the circuit multiple times and record how each qubit were measured.
It responds with a list of measured bistrings.

If you ran the above 4-qubit circuit 1000 times, output from the quantum computer could look like this:

{{% listing bitstrings.csv %}}

You can then plot the distribution of measured bistrings.
It's a sample-based estimate of what are the underlying probabilities of measuring a given bitstring.
These probabilities are often considered the output of a quantum computation.

{{% chart
    Bar
    title="number of measurements"
    x_labels="['0000', '0001', '0010', '0011', '0100', '0101', '0110', '0111', '1000', '1001', '1010', '1011', '1100', '1101', '1110', '1111']" %}}

None, [46, 285, 978, 323, 626, 117, 18, 145, 391, 483, 896, 587, 904, 607, 77, 991]

{{% /chart %}}

