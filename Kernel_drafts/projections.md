
# Projective measurement

Checks the value of a subset of qubits mid-circuit

## Definition

In an n-qubit circuit, identify if $k (\le n)$ qubits have a value {0,1} $^k$

## System features exposed

This kernel checks (i) if users can directly specify values to test, or if they need to encode the projections themselves, and (ii) the performance of projective measurements.

## Input data generation

Initialize all qubits to $\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$. Provide a test value {0,1} $^k$ if possible, or provide the circuit to check for the test value. The latter is less user-friendly.

## Output and Correctness

The output is a bit indicating whether the test state can be directly given, if the test state is found, and the latency of measurement. 

## Discussion

Projective measurements are used in many scenarios: absorbing walks, post-selection, and conditional execution. Such projections could be implemneted in software, and perhaps in future hardware. This kernel checks for the programmability and performance of this feature.

TBD: How to validate the output?

TBD: How to score programmability?



