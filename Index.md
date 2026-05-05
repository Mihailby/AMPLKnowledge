# AMPL Knowledge Base — Content Index

A single-page navigation hub for all documentation notebooks and runnable examples. Use this to find the right notebook for a topic or to locate which example demonstrates a specific concept.

**Jump to:** [Documentation](#documentation-notebooks) · [Examples](#example-notebooks) · [Concept Index](#concept-index)

---

## Documentation Notebooks

| Section | Notebook | Topics covered |
|---------|----------|----------------|
| **1** | [Model Components](documentation/1%20Model%20components.ipynb) | Sets, parameters, variables, constraints, objectives; model vs. data separation |
| **1.1** | [Sets](documentation/1_1%20Sets.ipynb) | `set` declaration syntax, `SEXPR`, naming rules, reserved words, amplpy `Set` API |
| **1.1.1** | [Flat vs Indexed Sets](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) | Flat sets, indexed set families `set F {I}`, `within`, `setof` flattening, amplpy assignment patterns |
| **1.1.2** | [Set Declaration vs. Definition](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) | `=` (symbolic definition) vs. `:=` (data assignment) vs. `default`; string quoting rules; model vs. data file discipline |

---

## Example Notebooks

Examples are numbered `<section>__<n>` and open directly in Colab. Each example is a minimal, self-contained runnable notebook.

### §1.1 — Sets

| Example | File | What it demonstrates |
|---------|------|----------------------|
| 1.1 / 1 | [1_1__1](examples/1_1__1.ipynb) | amplpy `Set` API: `set_values()`, `members()`, `size()` |

### §1.1.1 — Flat vs Indexed Sets

| Example | File | What it demonstrates |
|---------|------|----------------------|
| 1.1.1 / 1 | [1_1_1__1](examples/1_1_1__1.ipynb) | Basic flat set forms: scalar, tuple, ordered, circular, `within`, inline definition |
| 1.1.1 / 2 | [1_1_1__2](examples/1_1_1__2.ipynb) | Indexed set families: `set ARCS {NODES}`, ragged structure, `default {}`, subset restriction |
| 1.1.1 / 3 | [1_1_1__3](examples/1_1_1__3.ipynb) | Flattening an indexed family to a 2-D set with `setof {i in I, j in F[i]} (i,j)` |
| 1.1.1 / 4 | [1_1_1__4](examples/1_1_1__4.ipynb) | amplpy set assignment: property form, method form, from dict keys |

### §1.1.2 — Set Declaration vs. Definition

| Example | File | What it demonstrates |
|---------|------|----------------------|
| 1.1.2 / 1 | [1_1_2__1](examples/1_1_2__1.ipynb) | Symbolic definition with `=`: literal sets, arithmetic ranges, filtered comprehensions, set-algebraic expressions |
| 1.1.2 / 2 | [1_1_2__2](examples/1_1_2__2.ipynb) | Data assignment with `:=`: data-file syntax and `let` command overrides |
| 1.1.2 / 3 | [1_1_2__3](examples/1_1_2__3.ipynb) | When to define in the model (`=`) vs. supply from a data file (`:=`) |
| 1.1.2 / 4 | [1_1_2__4](examples/1_1_2__4.ipynb) | amplpy data assignment: raw AMPL, property assignment, method form, DataFrame integration |
| 1.1.2 / 5 | [1_1_2__5](examples/1_1_2__5.ipynb) | Numeric vs. string type confusion: number `100` ≠ string `"100"`, empty intersection |

---

## Concept Index

Alphabetical list of every key concept, keyword, and pattern covered in the current notebooks. Each entry links to the notebook (and example, where relevant) where it is introduced or explained in detail.

### A

**amplpy `Set` API** (`set_values`, `members`, `size`, `get_values`) — [§1.1 Sets](documentation/1_1%20Sets.ipynb) · [ex 1.1/1](examples/1_1__1.ipynb) · [ex 1.1.1/4](examples/1_1_1__4.ipynb) · [ex 1.1.2/4](examples/1_1_2__4.ipynb)

**Anonymous indexing** (indexing without naming the dummy variable) — [§1.1 Sets](documentation/1_1%20Sets.ipynb)

**Arithmetic range (`..`, `by`)** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

### B

**`binary` keyword** — [§1.1 Sets](documentation/1_1%20Sets.ipynb) (reserved words table)

**Bounds on variables** (`>= 0`, `<= 500`) — [§1 Model Components](documentation/1%20Model%20components.ipynb)

### C

**`card()` (cardinality)** — [§1.1 Sets](documentation/1_1%20Sets.ipynb)

**Cartesian product (`cross`)** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

**`circular` attribute** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb)

**Collections of sets** → see *Indexed set families*

**Constraints** (`subject to`) — [§1 Model Components](documentation/1%20Model%20components.ipynb)

### D

**Data assignment (`:=`)** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/2](examples/1_1_2__2.ipynb) · [ex 1.1.2/3](examples/1_1_2__3.ipynb)

**Data file (`.dat`)** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/3](examples/1_1_2__3.ipynb)

**`default` attribute** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.1/2](examples/1_1_1__2.ipynb)

**`diff` operator** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

**`dimen` attribute** — [§1.1 Sets](documentation/1_1%20Sets.ipynb) · [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb)

### F

**Feasibility problem** (model without objective) — [§1 Model Components](documentation/1%20Model%20components.ipynb)

**Filtered comprehension / conditional indexing** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

**Flat set** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb)

### I

**Indexed set families** (`set F {I}`) — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/2](examples/1_1_1__2.ipynb)

**`inter` operator** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

### L

**`let` command** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/2](examples/1_1_2__2.ipynb)

### M

**Model components overview** — [§1 Model Components](documentation/1%20Model%20components.ipynb)

**Model vs. data file discipline** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/3](examples/1_1_2__3.ipynb)

**Multidimensional set (`dimen 2`, `dimen n`)** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb)

### N

**Naming rules** (identifiers, case-sensitivity) — [§1.1 Sets](documentation/1_1%20Sets.ipynb)

**Numeric vs. string members** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/5](examples/1_1_2__5.ipynb)

### O

**Objectives** (`minimize`, `maximize`) — [§1 Model Components](documentation/1%20Model%20components.ipynb)

**`ordered` attribute** — [§1.1 Sets](documentation/1_1%20Sets.ipynb) · [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb)

### P

**Parameters** (`param`) — [§1 Model Components](documentation/1%20Model%20components.ipynb)

**Pitfall — assigning data to a `=`-defined set** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb)

**Pitfall — indexed family vs. flat tuple set confusion** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb)

**Pitfall — reserved word as set name** — [§1.1 Sets](documentation/1_1%20Sets.ipynb)

**Pitfall — string literal without quotes in model context** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb)

### Q

**Quoting rules** (model context vs. data context) — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb)

### R

**Ragged structure** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/2](examples/1_1_1__2.ipynb)

**Reserved words** — [§1.1 Sets](documentation/1_1%20Sets.ipynb)

### S

**`set` declaration** — [§1.1 Sets](documentation/1_1%20Sets.ipynb) · [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb)

**`setof` operator** (flattening indexed families) — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/3](examples/1_1_1__3.ipynb)

**`SEXPR` (set expression)** — [§1.1 Sets](documentation/1_1%20Sets.ipynb)

**Simple (scalar) set** — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb)

**String quoting** → see *Quoting rules*

**Subset** (`within`) — [§1.1 Sets](documentation/1_1%20Sets.ipynb) · [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb)

**Symbolic definition (`=`)** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb) · [ex 1.1.2/3](examples/1_1_2__3.ipynb)

**`symdiff` operator** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

### T

**Tuple set** (`dimen 2`) — [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb)

**Type confusion (number vs. string)** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/5](examples/1_1_2__5.ipynb)

### U

**`union` operator** — [§1.1.2](documentation/1_1_2%20Set%20Declaration%20vs.%20Definition.ipynb) · [ex 1.1.2/1](examples/1_1_2__1.ipynb)

### V

**Variables** (`var`) — [§1 Model Components](documentation/1%20Model%20components.ipynb)

### W

**`within` (attribute / operator)** — [§1.1 Sets](documentation/1_1%20Sets.ipynb) · [§1.1.1](documentation/1_1_1%20Flat%20vs%20Indexed%20Sets.ipynb) · [ex 1.1.1/1](examples/1_1_1__1.ipynb) · [ex 1.1.1/2](examples/1_1_1__2.ipynb)

---

*Last updated: 2026-05-05 · Reflects content in `documentation/` (4 notebooks) and `examples/` (10 notebooks).*
