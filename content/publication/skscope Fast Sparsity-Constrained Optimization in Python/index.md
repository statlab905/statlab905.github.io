---
title: "skscope: Fast Sparsity-Constrained Optimization in Python"
authors:
- zezhi-wang
- Junxian Zhu
- xueqin-wang
- jin-zhu
- huiyang-peng
- peng-chen
- anran-wang
- xiaoke-zhang
date: "2024-09-19T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-09-19T00:00:00Z"

publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Journal of Machine Learning Research"
publication_short: "JMLR"

abstract: Applying iterative solvers on sparsity-constrained optimization (SCO) requires tedious mathematical deduction and careful programming/debugging that hinders these solvers' broad impact. In the paper, the library skscope is introduced to overcome such an obstacle. With skscope, users can solve the SCO by just programming the objective function. The convenience of skscope is demonstrated through two examples in the paper, where sparse linear regression and trend filtering are addressed with just four lines of code. More importantly, skscope's efficient implementation allows state-of-the-art solvers to quickly attain the sparse solution regardless of the high dimensionality of parameter space. Numerical experiments reveal the available solvers in skscope can achieve up to 80x speedup on the competing relaxation solutions obtained via the benchmarked convex solver. skscope is published on the Python Package Index (PyPI) and Conda, and its source code is available at: https://github. com/abess-team/skscope.

featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://www.jmlr.org/papers/v25/23-1574.html
---