# Quantum Random Number Generator

> **Category**: utilities &nbsp;|&nbsp; **Difficulty**: beginner &nbsp;|&nbsp; **Qubits**: 4 &nbsp;|&nbsp; **Gates**: 4 &nbsp;|&nbsp; **Depth**: 1

A quantum random number generator (QRNG) produces genuinely random bits by preparing qubits in superposition (|+⟩ = (|0⟩+|1⟩)/√2) and measuring. Unlike pseudo-random number generators, the randomness is intrinsic to quantum mechanics — no hidden pattern exists. This circuit generates 4 independent random bits simultaneously. Real QRNGs are commercially available and used in cryptography and scientific simulation.

## Expected Output

Uniformly random 4-bit string in {0000,...,1111}

## Circuit

The OpenQASM 2.0 circuit is in [`circuit.qasm`](./circuit.qasm).

```
OPENQASM 2.0;
include "qelib1.inc";
// 4-bit quantum random number generator
qreg q[4];
creg c[4];
h q[0];
h q[1];
h q[2];
h q[3];
measure q[0] -> c[0];
measure q[1] -> c[1];
measure q[2] -> c[2];
measure q[3] -> c[3];
```

## Tags

`random` `utilities` `superposition` `measurement` `cryptography`

## References

- [Jennewein et al. (2000). A Fast and Compact Quantum Random Number Generator. Rev. Sci. Instrum. 71, 1675](https://doi.org/10.1063/1.1150518)

## License

MIT — part of the [OpenQC Algorithm Catalog](https://github.com/openqc-algorithms).
