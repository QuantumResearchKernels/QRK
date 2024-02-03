# GHZ Fidelity <working title>

## Definition

Create a Greenberger–Horne–Zeilinger state on $n$ qubits.

Measure $1$ qubit to collapse the GHZ state to one of its basis states. Subsequently measure the remaining $n-1$ qubits.

## System Features exposed

The resulting error in the final state that comes from compounding individual errors in performing each gate.

## Input data generation

A list of the $n$ qubits to be entangled.

## Output and Correctness

Any observation in the set of $n-1$ subsequent observations that doesn't match the first observation is an error. Any error causes the test to Fail.

## Discussion

### As a Software Check

This could be run as a pre-condition to continue with a real workload:  A test can be planned to run before the desired quantum algorithm and could trigger a "fail early exit" or a calibration routine.
The test size and placement can be comprehended from the workload's details.

E.G., for a workload that requires $w$ work qubits and $a$ ancilla qubits, a GHZ of size $n = w + a$ qubits is selected.

### As a Hardware Diagnostic

Run as a comprehensive suite of tests, analysis can identify a given qubit that performs badly.
For quantum hardware composed of $n$ qubits, for each possible subset of qubits $s$, where $2 < s <= n$, prepare GHZ states by implementing all possible combinations of connected pairs of qubits.	

E.G., for a $3$ qubit system with "all-to-all" connectivity, we construct $3! = 6$ circuits.

E.G., for a $4$ qubit system with $2$-qubit gates for hardware qubit pairs $1-2$, $2-3$, $3-4$, and $1-4$, then we construct the $8$(?) circuits:

H(1)
CNOT(1,2)
CNOT(2,3)
CNOT(3,4)

H(1)
CNOT(1,4)
CNOT(4,3)
CNOT(3,2)

H(2)
CNOT(2,3)
CNOT(3,4)
CNOT(4,1)

H(2)
CNOT(2,1)
CNOT(1,4)
CNOT(4,3)

etc. 
(mutatis mutandi)
