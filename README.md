# density-matrix-simulator

Work in progress for a density matrix simulator


## Motivation of the choices

- support different Hilbert dimensions for each qubit (which reduces the density matrix size and thus improves speed)
- the usefulness of a density-matrix simulator is closely related to the usefulness of its noise models (so include nice noise models)
- only support measurements in the Z basis for fast mid-cycle measurements (sample the outcomes from the density-matrix diagonal)
- work with Pauli vectors and Pauli transfer matrices (why?)
- when multiplying PTM and PV, do not expand PTM as a full system matrix; instead, multiply just the correct rows and columns (reduce memory usage)
- pre-compile blocks of the circuit that are repeated often (is this worth it? see previous point)
- support numpy and cuda backends
- pre-compile PTMs (see `quantumsim` trick)
