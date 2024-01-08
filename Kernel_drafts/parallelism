
# Parallel execution

Checks for an embarassingly parallel execution on a quantum system

## Definition

Runs an embarassingly parallel kernel, e.g., a variational kernel, on a quantum system to identify its performance scaling. The quantum system could be a cloud that conencts to multiple quantum processing units (QPUs), or a single QPU that supports multi-tenancy.

## System features exposed

This kernel checks if a quantum system supports parallel execution, and how performance scales with parallelism.

## Input data generation

Any kernel can be deployed to test this feature, but a useful kernel is subspace variational algorithm to find multiple eigenstates. Another is the computation of Pauli expectations.

## Output and Correctness

The output is a series of measurements showing performance (accuracy relative to exact computation, latency) with increasing number of parallel kernels.

## Discussion

Many quantum algorithms contain classical parallelism. Being able to exploit such easily available parallelism provides a significant boost to quantum applications in the near term. This kernel quantifies parallel execution capability.




