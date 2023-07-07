# Quantum Research Kernels

Applications and Application-programmers need to drive the development of quantum computing; both the hardware and the programming envionments used to write code.  While the concept of a co-design effort is easy to sell, making it work in practice is difficult.

In High Performqance computing (HPC), we did this with the *parallel research kernels* (PRK).  These simple programs expose the performance bottlenecks of an HPC system that would limit usefulness of a system for scientific computing applications.  If a system did well for all the PRK, that system would most likely be an effective system for HPC. Individual PRK do not mimic kernels from applications so they are not useful as benchmarks.  It is best to think of them as software probes of a system.

We, the people working on this repository, are exploring the following hypothesis:  Can we use an approach like the PRK to support the design of systems for quantum computing?   Can we create a set of *system probes* that will define the needs of programmers developing applications for quantum computers?  Based on experience with the PRK, we know that for each quantum research kernel (QRK) we need:

* An informative or even ``catchy'' name
* A brief statement of what this kernel does
* A brief statement of what feature of a quantum computer this kernel stresses
* A detailed defintion of the kernel itself
* The input for the kernel
* The output and how it will be tested for correctness

At this point, we have defined the following kernels

