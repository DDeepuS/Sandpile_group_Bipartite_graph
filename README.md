# Sandpile Groups of Random Bipartite Graphs

This repository contains code and data for numerical experiments supporting the conjectures in the paper  
**“Sylow \(p\)-subgroups of Sandpile Groups of Random Bipartite Graphs”**  
by **Jason Fulman, Nathan Kaplan, Deepesh Singhal, and Ole Warnaar**.  

In that paper we study random bipartite Erdős–Rényi graphs \(G(n,\alpha,u)\), where the vertex set is partitioned into two parts \(V_1\) and \(V_2\) with \(|V_1| = n\) and \(|V_2| = \lfloor \alpha n \rfloor\), and each possible edge between \(V_1\) and \(V_2\) is included independently with probability \(u\) (no edges are allowed within a part).  For such a graph \(G\), its **sandpile group** (also called the critical group or Jacobian) is the finite abelian group given by the cokernel of any reduced Laplacian matrix of \(G\).  The paper conjectures a Cohen–Lenstra–type description of the distribution of the Sylow \(p\)-subgroups of these sandpile groups, and of their \(p\)-ranks.  The experiments in this repository numerically investigate these conjectural distributions for various primes \(p\), values of \(\alpha\), and edge probabilities \(u\).


## Contents

- `Sandpile Groups of random Bipartite Graphs.ipynb`  
  Sage/Jupyter notebook that:
  - samples random bipartite graphs,
  - computes sandpile groups and their Sylow \(p\)-subgroups,
  - records the partition type and \(p\)-rank,
  - compares empirical frequencies with the conjectural measures,
  - writes results to CSV files.

- `results for p=2/`  
  CSV files with partition-level data, rank distributions, and \(\mathbb{E}(2^{\mathrm{rank}})\) for experiments with \(p=2\), \(n_1=100\), and various \((\alpha,u)\).

- `results for p=3/`  
  CSV files with analogous data for \(p=3\).

## Requirements

- SageMath (used via the Jupyter notebook interface)
- Python libraries available inside Sage (no extra packages beyond the standard Sage installation are needed).

## Usage

1. Open the notebook in Jupyter with SageMath as the kernel.
2. Run the cells to reproduce the experiments or modify parameters (prime \(p\), number of samples \(N\), values of \(\alpha\) and \(u\), etc.).
3. The notebook will regenerate CSV files in the corresponding `results for p=2` or `results for p=3` folders.

The CSV files can be post-processed (e.g., in a separate Python notebook) to produce LaTeX tables and plots for the manuscript.
