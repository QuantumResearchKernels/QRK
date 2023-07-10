
# Encode

Define a set of values on a classical computer.  Encode them as qubits and apply a simple operation (a phase shift).  Read them back onto the classical computer and verify that they have the correct results.

## Definition

Define $N$ complex numbers.

$$ Cval[k] = e^{i\frac{k \pi}{N}} $$

Load these onto the quantum computer as a set of $N$ qubits
values.  Apply a constant phase shift of $\phi$.   Read them back onto the classical computer and verify that the results are:

$$ Cval[k] = e^{i(\frac{k \pi}{N}+\phi)} $$

The metric for this kernel is the maximum value of $N$ such that the operation is correct.

## System features exposed

Stresses the ability to move data between the classical and quantum computer. It also stresses the error correction features of the system.  

## Input data generation

The input data is a set of complex numbers on the classical computer:

$$ Cval[k] = e^{i\frac{k \pi}{N}} $$

## Output and Correctness

The output is the input complex numbers with the phase shifted by the a constant value, $\phi$.

## Discussion

This is the most basic need of a practical quantum computer; the ability to describe an input state on the classical computer and then encode the corresponding qubits on the quantum computer.  We need a symmetrical relation, that is, we need to encode the qubits (move them from the classical computer to the quantum computer) and the opposite (move them from the quantum computer to the classical computer).   

Describe the rationale for this kernel both in terms of the system features it exposes but also the relevance it holds for applications.


