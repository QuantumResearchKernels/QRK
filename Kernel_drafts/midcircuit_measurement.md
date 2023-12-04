# Mid-Circuit Measurement

Make a choice of which sub-circuit to execute from the result of a measurement on a qubit.

## Definition

Define two $n$-qubit sub-circuits $A$ and $B$. Prepare an $n$-qubit state $\ket{\psi}$ . Prepare an additional qubit $d$ as the decision qubit.

Action:  Measure the state of $d$. Use the outcome of the observation to select which sub-circuit $A$ or $B$ is subsequently run.

## System features exposed

This probes the latency introduced by needing to check the outcome of a measurement to make a branching selection.

## Input data generation

Run the test with the decision qubit $d$ prepared in three different ways:

1. in $\ket{0}$ state
2. in $\ket{1}$ state
3. in $\frac{1}{\sqrt{2}}\ket{0} + \frac{1}{\sqrt{2}} \ket{1}$ state

## Output and Correctness

Test:  Measure the duration from the end of the preparation to the beginning of the sub-circuit execution. The maximum of the three durations is the decision latency.

## Discussion

This latency would impact the performance of algorithms of the Run-Until-Success type and quantum steering.

How do we handle the timing?

Do the values of $n$, $A$, $B$, and $d$ matter? 

Should we test on additional $d$ qubits?
