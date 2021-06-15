# Project Description
This repository contains two projects developed by myself, David Castells Graells and Eleftherios Tselentis during a hackathon on quantum computing at ETH Zurich in 2019. We won the competition and provided the solutions to the following problems: 

[link to the challange](http://squids.ch/2018/12/no-1-in-c-not-major/)

### 1. Quantum pigeon hole simulation
The pigeonhole principle is naturally intuitive in the classical world: if you put three pigeons in two pigeonholes at least two of the pigeons end up in the same hole. However, it turns out that this is not necessarily true in the quantum world!  [1]

In this task, you will have to model the quantum pigeonhole principle, an example of so-called pre- and post-selection logical paradoxes which occur in quantum mechanics [2].

Resources
[1] Y. Aharonov, F. Colombo, S. Popescu, I. Sabadini, D. C. Struppa: “The quantum pigeonhole principle and the nature of quantum correlations”, 2014; arXiv:1407.3194.

[2] Matthew F. Pusey, Matthew S. Leifer: “Logical pre- and post-selection paradoxes are proofs of contextuality”, 2015, EPTCS 195, 2015, pp. 295-306; arXiv:1506.07850. DOI: 10.4204/EPTCS.195.22.

Subtasks
Your program should simulate the experiment, which in principle can be done at different levels of abstraction.

**Mandatory**

- Simulate the counterfactual paradox in [1].
- Compute the weak values for the paradox.
- Allow for different pre- and post-selections.

**Extra**

- Model the pointer as a quantum system undergoing a joint evolution with the system measured.
- For a given arbitrary setting, try to find whether there are pre- and post-selections that lead to a pre- and post-selection.



### 2. Quantum transversals
We start with the set G of all N-bit strings, for example for N=3,
G={000,001,010,100,011,101,110,111}.
Now we consider a symmetry group acting on N elements; for example the fully symmetric group
S3={123,132,213,231,312,321},
 which represents all permutations of the three elements. There could be other groups, like S2×S1={123,213}, which only allow for permutations of the two first elements.

Our original set G can be partitioned into a maximal collection of subsets, each one invariant under the action of the permutation group. In the case of S3 we have 
G0={000},G1={001,010,100},G2={011,101,110},G3={111}.
A transversal is then a set containing exactly one element from each member of the collection, for example
T={000,010,110,111}.
Another possible transversal could be for example T′={000,100,110,111}=(213) T, which is the result of acting with the permutation (213) from the symmetry group on the elements of T.

A uniform quantum superposition of the elements of the transversal T (“quantum transversal”  for short) would be the 3-qubit state
12(|000⟩+|010⟩+|110⟩+|111⟩).
In this task, you should write a program that receives as input the number of qubits N and a symmetry group acting on N elements, and outputs a quantum circuit that generates a quantum transversal. You are free to choose the format of the input. See [1] for a classical algorithm to find a transversal, which can be used as a preparatory step.

 

Resources
[1] Nicolas Borie: “Generating tuples of integers modulo the action of a permutation group and applications”, 2012; arXiv:1211.6261.

 
**Mandatory**

- Output the final state (a uniform superposition of a transversal) for the fully symmetric group SN.
- The program should also output the circuit that generates the quantum transversal.
- Allow for an extra input π∈S, which is a permutation in the symmetry group, and output the effect of this permutation on the transversal.

**Extra**

- Allow for any symmetric group on N elements.
- Find a way to order the transversal, and let the user also input their preferred transversal (e.g. whether they want a superposition of the elements of T or T′ in the example above).
