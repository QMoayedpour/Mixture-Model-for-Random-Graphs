# Mixture Model for Random Graphs
Implementation and experiments for **A Mixture Model for Random Graphs** (Daudin et al., 2006). The project explores stochastic block models, EM/VB inference, and practical initialization strategies on synthetic and real-world graphs.

## Project layout
- `src/`: core implementation (mixture model, SBM utilities, variational updates, visualizations)
- `ntbk/`: experiment notebooks (initialization, model selection, complexity, real graphs, VB)
- `data/`: example graphs (`polbooks.gml`, `sp_data_school_day_2_g.gexf`)
- `report.pdf`, `poster.pdf`: short write-up and poster

## Getting started
```bash
python -m venv .venv && source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt       # minimal deps
# or: pip install -e .                # includes optional extras (torch, sklearn, tqdm, numba)
```

Open the notebooks in `ntbk/` to reproduce the experiments or import the package to run custom graphs:
```python
from src.mixturemodel import MixtureModel
```

Note: the code sometimes uses `K` and `Q` interchangeably for the number of clusters, mirroring the notation in the paper.
