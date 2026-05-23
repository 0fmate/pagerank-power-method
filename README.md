# Power Method and Google PageRank

Numerical linear algebra project implementing and analysing the Power Method and the Google PageRank algorithm on a real web graph, developed as a group coursework project for the MSc in Data Science and Engineering at Politecnico di Torino.

## Overview

The goal of this project is to study the algebraic and computational aspects of PageRank starting from first principles:

- formulate PageRank as an eigenvector problem for a stochastic matrix,
- implement the Power Method to approximate the dominant eigenvector,
- analyse convergence properties and damping,
- apply the algorithm to a real web graph and interpret the resulting ranking.

The repository contains both the Jupyter notebook with the full implementation and the final written report.

## Repository structure

```text
pagerank-power-method/
├── README.md
├── requirements.txt
├── .gitignore
├── notebook/
│   └── pagerank_power_method_notebook.ipynb
├── report/
│   └── pagerank_power_method_report.pdf
└── data/
    └── README.md
```

- `notebook/pagerank_power_method_notebook.ipynb`  
  Full implementation of the Power Method and PageRank, with experiments and plots.
- `report/pagerank_power_method_report.pdf`  
  Written report discussing theory, numerical results and conclusions.
- `data/README.md`  
  Notes about the expected format and location of the web graph dataset (not included).

## Mathematical background

The project revisits PageRank in terms of:

- stochastic adjacency matrices and Markov chains,
- eigenvalue problems for the dominant eigenvector,
- the Power Method for large sparse matrices,
- the teleportation model and the Google matrix \( M = (1 - m)A + mS \),
- convergence and spectral gap considerations.

These ideas are then applied to rank pages in a real web graph.

## Implementation highlights

The notebook covers:

- construction of the stochastic matrix from link data,
- handling dangling nodes and normalisation,
- implementation of the generic Power Method,
- specialisation of the Power Method to the PageRank matrix,
- experiments with different damping factors and tolerances,
- ranking of pages and interpretation of the top-ranked nodes.

The focus is on clarity of the numerical linear algebra rather than on production-grade software.

## Setup

Create a virtual environment (optional) and install dependencies:

```bash
pip install -r requirements.txt
```

Then open the notebook:

```bash
jupyter notebook notebook/pagerank_power_method_notebook.ipynb
```

or with JupyterLab:

```bash
jupyter lab notebook/pagerank_power_method_notebook.ipynb
```

## Data

The original web graph dataset used in the assignment is **not** included in this repository.

To reproduce the experiments:

1. Obtain a compatible link dataset (e.g. the Hollins University web graph used in the course).
2. Place it under the `data/` directory.
3. Update the corresponding file path in the notebook if necessary.

The expected format and any preprocessing steps are documented in `data/README.md` and in the notebook.



## Course context

This project was developed as part of the course **Computational Linear Algebra for Large Scale Problems** (a.y. 2025/2026), MSc in Data Science and Engineering, Politecnico di Torino.

It is a **group project** developed by **Davide D’Amico** and **Gerardo Rainone**.
