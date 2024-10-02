# ED-AD
This project studies the performance of entanglement-based QKD with a two-stage distillation process (Entanglement distillation + Advantage distillation).

# Prerequisites

In order to execute the notebooks in this repo, install and configure the SageMath environment (<https://www.sagemath.org/>) and the Sympy package (<https://www.sympy.org/>).

# Code Description

## CNOTs
Contains Clifford operators that correspond to repetition code in the symplectic matrix for n = 2, 3, 4 qubits.

## ED_transversal
Contains transversal (Clifford operators in symplectic matrix form) for bi-local Clifford entanglement distillation protocol for n = 2, 3, 4 pair. (<https://quantum-journal.org/papers/q-2022-05-19-715/>)

Note that the **ED2_11.sobj** is the operator that corresponds to the DEJMPS protocol.

## data
The results contain fidelity, key rate, and success probability for various protocols (Dephase state and the Werner state). Due to the file size limitation, the data for protocol 4-2-1 and protocol 4-1 are uploaded. Readers are required to generate locally by running corresponding protocol analyzers.

## dephase
Protocol analyzers for dephase input state, $\rho = F|\Phi^+\rangle \langle \Phi^+| + \left(1-F \right)|\Phi^-\rangle \langle \Phi^-|$. Files with two-digit names are analyzers for $m$-$n$-$1$ protocol. Files with single-digit names are analyzers for $m$-$1$ entanglement distillation only protocol. Each analyzer generates `distilled_states_mn.npy` (`distilled_states_m.npy` ) and `success_probabilities_mn.npy` (`success_probabilities_m.npy`).

## werner
Protocol analyzers for dephase input state, $\rho = F|\Phi^+\rangle \langle \Phi^+| + \frac{1-F}{3}  \left( |\Psi^+\rangle \langle \Psi^+| + |\Psi^-\rangle \langle \Psi^-| + |\Phi^-\rangle \langle \Phi^-| \right)$. Files with two-digit names are analyzers for $m$-$n$-$1$ protocol. Files with single-digit names are analyzers for $m$-$1$ entanglement distillation only protocol. Each analyzer generates `distilled_states_mn.npy` (`distilled_states_m.npy` ) and `success_probabilities_mn.npy` (`success_probabilities_m.npy`).

## cnot_symbolic_calculation.ipynb
Generate results about the repetition code analysis in the paper  in the appendix.

## visualizer_dephase.ipynb
Generate graphs for the dephase state in the paper.

## visualizer_werner.ipynb
Generate graphs for the Werner state in the paper.




