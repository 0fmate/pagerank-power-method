# Data

The original dataset used in this project is the **Hollins web graph dataset** (`hollins.dat`).

This file contains:
- URL definitions,
- link structure information between webpages,
- a graph with 6012 pages and 23875 links in the version used in the notebook.

The dataset is **not included** in this public repository.

To reproduce the experiments:

1. Place `hollins.dat` inside this `data/` folder.
2. Update the file path in the notebook if needed.
3. Run the notebook from start to finish.

The notebook also applies preprocessing steps such as:
- parsing the mixed file format,
- converting from 1-based indexing to Python indexing,
- building the column-stochastic transition matrix,
- correcting dangling nodes with uniform probabilities.