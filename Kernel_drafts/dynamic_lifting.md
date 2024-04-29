
# Dynamic Lifting

Read a qubit or qubits from a quantum computer. Compute some continuation classically while maintaining the state of existing qubits. Resume control on the quantum device.

## Definition


## System features exposed

Stresses the ability to exchange classical and quantum control while maintaining quantum states.

## Input data generation

Teleportation:

1. Prepare a Bell state and quantum state $\psi$.
2. Perform a Bell measurement on $\psi$ and the first qubit in the Bell state, producing the bits $x$ and $y$.
3. Send the qubits to the classical computer while retaining the coherence of the remaining qubit.
4. Compute a correction on the classical computer to apply to the last qubit.
5. Apply corrections on the quantum computer.
6. Read out the result $\psi$.

## Output and Correctness


## Discussion

This is an important but often hard to implement feature. Beyond just measuring qubits, we want to maintain quantum state while performing classical computation, and then resume computation.   

## Sources

Green, Alexander S., et al. "Quipper: a scalable quantum programming language." Proceedings of the 34th ACM SIGPLAN conference on Programming language design and implementation. 2013.


