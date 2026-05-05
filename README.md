# AMPL Knowledge Base — Documentation Notebooks

An interactive Jupyter notebook documentation series covering the AMPL modeling language, built from the official AMPL book, reference manual, and API guides.

## Structure

```
documentation/   — Jupyter notebooks: one per section of the AMPL reference
examples/        — Runnable example notebooks that accompany each section
Index.md         — Full content index: all notebooks, examples, and concept lookup
```

### Documentation chapters

| Section | Notebook | Topics |
|---------|----------|--------|
| 1 | [Model Components](documentation/1%20Model%20components.ipynb) | Sets, parameters, variables, constraints, objectives; model vs. data separation |
| 1.1 | [Sets](documentation/1_1%20Sets.ipynb) | `set` declaration syntax, `SEXPR`, naming rules, reserved words, amplpy `Set` API |
| 1.1.1 | [Flat vs Indexed Sets](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) | Flat sets, indexed set families `set F {I}`, `within`, `setof` flattening, amplpy patterns |
| 1.1.2 | [Set Declaration vs. Definition](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) | `=` (symbolic definition) vs. `:=` (data assignment) vs. `default`; string quoting; model vs. data file |

### Examples

Each example is a minimal, self-contained runnable notebook. Filenames follow the pattern `<section>__<n>`.

| Example | Section | What it demonstrates |
|---------|---------|----------------------|
| [1_1__1](examples/1_1__1.ipynb) | §1.1 | amplpy `Set` API: `set_values()`, `members()`, `size()` |
| [1_1_1__1](examples/1_1_1__1.ipynb) | §1.1.1 | Basic flat set forms: scalar, tuple, ordered, circular, `within`, inline definition |
| [1_1_1__2](examples/1_1_1__2.ipynb) | §1.1.1 | Indexed set families: `set ARCS {NODES}`, ragged structure, `default {}`, subset restriction |
| [1_1_1__3](examples/1_1_1__3.ipynb) | §1.1.1 | Flattening an indexed family to a 2-D set with `setof {i in I, j in F[i]} (i,j)` |
| [1_1_1__4](examples/1_1_1__4.ipynb) | §1.1.1 | amplpy set assignment: property form, method form, from dict keys |
| [1_1_2__1](examples/1_1_2__1.ipynb) | §1.1.2 | Symbolic definition with `=`: literal sets, ranges, filtered comprehensions, set algebra |
| [1_1_2__2](examples/1_1_2__2.ipynb) | §1.1.2 | Data assignment with `:=`: data-file syntax and `let` command overrides |
| [1_1_2__3](examples/1_1_2__3.ipynb) | §1.1.2 | When to define in the model (`=`) vs. supply from a data file (`:=`) |
| [1_1_2__4](examples/1_1_2__4.ipynb) | §1.1.2 | amplpy data assignment: raw AMPL, property assignment, method form, DataFrame |
| [1_1_2__5](examples/1_1_2__5.ipynb) | §1.1.2 | Numeric vs. string type confusion: number `100` ≠ string `"100"`, empty intersection |

## Index

[Index.md](Index.md) is a single-page reference that covers everything in this knowledge base:

- **Documentation table** — all notebooks with section numbers and topic summaries.
- **Examples table** — all example notebooks grouped by section, with a one-line description of what each demonstrates.
- **Concept index** — alphabetical lookup of every keyword, operator, pattern, and pitfall covered in the notebooks, with direct links to the relevant notebook and example.

Use `Index.md` when you know the concept you're looking for but not which notebook covers it (e.g., searching for `setof`, `quoting rules`, or `ragged structure`).

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
