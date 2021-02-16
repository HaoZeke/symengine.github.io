---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.0
kernelspec:
  display_name: R
  language: R
  name: ir
---

# First Steps [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/symengine/symengine.github.io/sources?filepath=docs%2Fuse%2Fapi%2FR%2Fexpressions.myst.md)

This is meant to be a gentle introduction to the `symengine` C++ library wrappers for `R`. We will load some standard packages. Note that the [vignette covers the core R syntax much better](https://symengine.org/symengine.R/articles/quick_start.html). The focus here is on usage with standard libraries.

```{code-cell} r
library(symengine)
library(tidyverse)
options(symengine.latex = TRUE, symengine.latex.center = TRUE)
```

## Working with Expressions

We will start by inspecting the use of Expressions.

```{code-cell} r
use_vars(x, y, .quiet = TRUE)
sqrt(x + y)
```

```{code-cell} r
auto ex = pow(x+sqrt(Expression(2)), 6);
ex
```

```{code-cell} r
expand(ex)
```

```{reviewer-meta}
:written-on: "2020-08-27"
:proofread-on: "2021-01-20"
:dust-days-limit: 60
```
