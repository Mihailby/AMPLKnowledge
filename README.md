# AMPL Knowledge Base — Documentation Notebooks

An interactive Jupyter notebook documentation series covering the AMPL modeling language, built from the official AMPL book, reference manual, and API guides.

## Structure

```
documentation/   — Jupyter notebooks: one per section of the AMPL reference
examples/        — Runnable example notebooks that accompany each section
```

### Documentation chapters

| Notebook | Topic |
|---|---|
| [1 Model components](documentation/1%20Model%20components.ipynb) | Overview of AMPL model components |
| [1_1 Sets](documentation/1_1%20Sets.ipynb) | Sets chapter overview |
| [1_1_1 Set Declaration vs. Definition](documentation/1_1_1%20Set%20Declaration%20vs.%20Definition.ipynb) | `=` vs. `:=`, symbolic definitions, defaults |
| [1_1_2 Indexing expressions](documentation/1_1_2%20Indexing%20expressions.ipynb) | `{i in S}`, filtered indexing, dummy variables |
| [1_1_3 Set membership operations](documentation/1_1_3%20Set%20membership%20operations.ipynb) | `in`, `not in`, `within`, `card()` |
| [1_1_4 set_operations](documentation/1_1_4%20set_operations.ipynb) | `union`, `inter`, `diff`, `symdiff`, `cross` |
| [1_1_5 unordered_sets](documentation/1_1_5%20unordered_sets.ipynb) | Unordered sets: semantics and valid operations |
| [1_1_6 Unordered sets](documentation/1_1_6%20Unordered%20sets.ipynb) | Sets of strings: quoting rules, `symbolic` keyword |
| [1_1_7 Sets of numbers](documentation/1_1_7%20Sets%20of%20numbers.ipynb) | Arithmetic ranges, `..`, `by`, integer/real sets |
| [1_1_8 Ordered sets](documentation/1_1_8%20Ordered%20sets.ipynb) | `ordered`, `circular`, `first`/`last`/`prev`/`next`/`ord` |
| [1_1_9 Predefined sets and interval expressions](documentation/1_1_9%20Predefined%20sets%20and%20interval%20expressions.ipynb) | `Integers`, `Reals`, `Binary`, `a..b by k`, exclusive bounds |
| [1_1_10 Sets of ordered pairs](documentation/1_1_10%20Sets%20of%20ordered%20pairs.ipynb) | 2-D sets, `dimen 2`, `within`, sparse vs. full Cartesian |
| [1_1_11 Subsets and slices of ordered pairs](documentation/1_1_11%20Subsets%20and%20slices%20of%20ordered%20pairs.ipynb) | Slice notation `S[i,*]`, projections, filtered subsets |
| [1_1_12 Sets of longer tuples](documentation/1_1_12%20Sets%20of%20longer%20tuples.ipynb) | 3-D+ sets, `dimen n`, chained `cross` |
| [1_1_13 Operations on sets of tuples](documentation/1_1_13%20Operations%20on%20sets%20of%20tuples.ipynb) | `setof`, projections, multi-dim set operators |
| [1_1_14 Indexed collections of sets](documentation/1_1_14%20Indexed%20collections%20of%20sets.ipynb) | `set ARCS {NODES}`, ragged families, nested indexing |
| [1.2. Parameters](documentation/1.2.%20Parameters.ipynb) | Parameter declarations and attributes |
| [1.3. Variables](documentation/1.3.%20Variables.ipynb) | Variable declarations and bounds |

## Prerequisites

- [AMPL](https://ampl.com/) (free Community Edition works for all examples)
- Python 3.9+
- [amplpy](https://amplpy.readthedocs.io/) — `pip install amplpy`
- Jupyter — `pip install notebook` or `pip install jupyterlab`

## Notebook conventions

Each documentation notebook follows a consistent structure:
1. **Syntax reference** — formal grammar and attribute table
2. **Conceptual explanation** — semantics and when to use each construct
3. **Numbered examples** — complete, runnable AMPL model fragments
4. **Best practice boxes** — recommended patterns
5. **Pitfall boxes** — common mistakes and how to avoid them
6. **Edge cases** — boundary conditions and subtle behavior

Code cells contain AMPL model code. Cells marked `amplpy` show the equivalent Python API patterns.

## Source material

The notebooks are derived from:
- *AMPL: A Modeling Language for Mathematical Programming* (Fourer, Gay, Kernighan)
- AMPL Reference Manual
- amplpy API documentation
- AMPL community forum
