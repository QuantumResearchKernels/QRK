
# LOCC execution

Checks for a parallel execution on a quantum computer, synchronized with classical measurements (Local Operations and Classical Communication)

## Definition

Runs an embarassingly parallel kernel, e.g., a variational kernel, on a quantum system. The quantum system could be a cloud that connects to multiple quantum processing units (QPUs), or a single QPU that supports multi-tenancy.

## System features exposed

This kernel checks if a quantum system supports parallel execution.

## Input data generation

One possible kernel is the subspace variational algorithm to find multiple eigenstates. Another is the computation of Pauli expectations. In either case, tasks are run in parallel and aggregated after classical measurements.

## Output and Correctness

The test passes if the comptuiations run separately and aggregated, match the expected output.

## Discussion

Many quantum algorithms contain classical parallelism. Being able to exploit such easily available parallelism provides a significant boost to quantum applications in the near term. This kernel quantifies parallel execution capability.

TBD: There seems to be an overlap with the mid-circuit measurements kernel. Do we merge them?




