
# Encode

Define a set of values on a classical computer.  Encode them as qubits and apply a simple operation (negate a bunch of qubits).  Read them back onto the classical computer and verify that they have the correct results.

## Definition

Inputs: An $N$ bit nat $n \in \\{0,1\\}^N$, a subset of $S$ of indices less than $N$. 

Output: The nat $n$, with indices $S$ negated.

Load $n$ onto the quantum computer as a set of $N$ qubits.  Apply an $X$ gate to every qubit in $S$. Read them back onto the classical computer and verify that the appropriate bits have been negated.

OLD: The metric for this kernel is the maximum value of $N$ such that the operation is correct. (Still relevant?)

## System features exposed

Stresses the ability to move data between the classical and quantum computer. It also stresses the error correction features of the system.  

## Input data generation

The input data is a natural number on the classical computer:

$n \in \\{0,1\\}^N$

## Output and Correctness

The nat $n$, with indices $S$ negated.

## Discussion

This is the most basic need of a practical quantum computer; the ability to describe an input state on the classical computer and then encode the corresponding qubits on the quantum computer.  We need a symmetrical relation, that is, we need to encode the qubits (move them from the classical computer to the quantum computer) and the opposite (move them from the quantum computer to the classical computer).   



