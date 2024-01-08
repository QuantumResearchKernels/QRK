
# Hamiltonian simulation

Checks for Hamiltonian simulation capabilities. 

## Definition

This kernel has a Hamiltonian that is to be a programmed and executed on a quantum computer.

## System features exposed

The kernel checks if a given quantum system can be programmed directly using a Hamiltnonian, and if it can natively simulate it.
 
## Input data generation

No additional input is needed for the kernel

## Output and Correctness

The output is a bit indicating if the target natively accepts Hamiltonians, and execution times for Hamiltonian simulation vs alternative circuit-decomposition.

## Discussion

Hamiltonians are the natural forms of problem specification in many fields, even beyond physics and chemistry, such as with certain cognitive models. However, most quantum computers today require being programmed in unitaries obtained after exponentiating the Hamilotnian. This increases compilation time, and the resulting quantum system runs poorly. 
Supporting native quantum programming and execution improves programmability and performance.

Related reference: SimuQ https://arxiv.org/pdf/2303.02775.pdf

TBD: How to check for native Hamiltoninan execution?



