
# Projective measurement

This kernel checks if a quantum computer supports subspace projections, which are part of many quantum applications and algorithms, without explicit synthesis by the user. This is done by measuring along a subset of basis states (subspace projective measurement).  

## Definition

The kernel prepares an n-qubit quantum state, measures it in the subspace spanned by a subspace $\Pi$ of the space of $2^n$ basis states. The components of the state outside $\Pi$ should be unaffected. 

## System features exposed

The ability to natively specify subspace projections. Note that "native" is used in the sense of user-transparent, i.e., it doesn't have to be intrinsic to hardware and could be emulated by the software.   

## Input data generation

Initialize the n qubits to a known state $\psi$. Measure with the operator $\Pi$, with an ancilla. Then, measure again for all the states outside $\Pi$. Repeat this to constuct a probability distribution.   

## Output and Correctness

The test passes if the measured probability of the ancilla being 1 in the first step matches with $||\Pi\psi||^2_2$, and the probability distribution of the second step matches the corresponding normalized probabilities of $(I-\Pi)\psi$. 

## Discussion

Projective measurements are used in many scenarios: absorbing walks, post-selection, and conditional execution. Such projections could be implemneted in software, and perhaps in future hardware. This kernel checks for presence of this feature.

TBD: What state ($\psi$) to prepare, and $\Pi$ to use?

TBD: Tolerance to identify a match?



