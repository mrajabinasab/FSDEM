# FSDEM: Feature Selection Dynamic Evaluation Metric

FSDEM is a novel evaluation metric designed to address the limitations of existing metrics in the field of feature selection. It provides a dynamic approach to evaluate both the performance and stability of feature selection algorithms.

## Installation

You can install the package using pip:

```bash
pip install fsdem
```
## Usage

Here, you can see an example of how to use fsdem:

```python
from fsdem import approx_func, fsdem, stability

# Observations of the metric and corresponding number of features
x = [1, 2, 3, 4, 5]
y = [0.1, 0.4, 0.6, 0.8, 0.9]

# Approximate the function and its derivative
f, df = approx_func(x, y)

# Calculate FSDEM score
fsdem_score = fsdem(f, start=1, end=5)
print("FSDEM Score:", fsdem_score)

# Calculate stability score
stability_score = stability(df, start=1, end=5)
print("Stability Score:", stability_score)
```

### Citation

If you use FSDEM in your research, please cite the original paper:

```
@inproceedings{rajabinasab2024fsdem,
  title={A Dynamic Evaluation Metric for Feature Selection},
  author={Rajabinasab, Muhammad and Lautrup, Anton D. and Hyrup, Tobias and Zimek, Arthur},
  booktitle={International Conference on Similarity Search and Applications (SISAP 2024)},
  pages={65--72},
  year={2024},
  organization={Springer}
}
```
