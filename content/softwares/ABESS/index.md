---
title: abess -- A Fast Best-Subset Selection Library in Python and R
summary: abess implements a unified framework of best-subset selection for solving diverse machine learning problems, e.g., linear regression, classification, and principal component analysis. Particularly, abess certifiably gets the optimal solution within polynomial time with high probability under the linear model. Our efficient implementation allows abess to attain the solution of best-subset selection problems as fast as or even 20-times faster than existing competing variable (model) selection toolboxes. Furthermore, it supports common variants like best subset of groups selection and ridge-regularized best-subset selection. The core of the library is programmed in C++. For ease of use, a Python library is designed for convenient integration with sklearn, and it can be installed from the Python Package Index (PyPI). In addition, a user-friendly R library is available at the Comprehensive R Archive Network (CRAN). The full [documentation](https://abess.readthedocs.io/) is online accessible.
show_date: false
tags:
- variable selection
- high-dimensional data
- linear regression
- logistic regression
- poisson regression
- gamma regression
- multi-task learning
- multi-classification
- rank learning
- group variable selection
- principal component analysis
- robust principal component analysis

# Optional external URL for project (replaces project detail page).
# external_link: "https://github.com/abess-team/abess"
---


<a href="https://anaconda.org/conda-forge/abess">
    <img src='https://anaconda.org/conda-forge/abess/badges/platforms.svg' align="left"/></a>
</a>
<a href="https://badge.fury.io/py/abess">
    <img src='https://badge.fury.io/py/abess.svg' align="left"/></a>
</a>
<a href="https://anaconda.org/conda-forge/abess">
    <img src='https://img.shields.io/conda/vn/conda-forge/abess.svg' align="left"/></a>
</a>
<a href="https://cran.r-project.org/package=abess">
    <img src='https://img.shields.io/cran/v/abess?logo=R' align="left"/></a>
</a>
<a href="https://pepy.tech/project/abess">
    <img src='https://pepy.tech/badge/abess' align="left"/></a>
</a>

<img src='https://raw.githubusercontent.com/abess-team/abess/master/docs/image/icon_long.png' align="center"/></a>

## Overview

`abess` (Adaptive BEst Subset Selection) library aims to solve general best subset selection, i.e.,
find a small subset of predictors such that the resulting model is expected to have the highest accuracy.
The selection for best subset shows great value in scientific researches and practical applications.
For example, clinicians want to know whether a patient is healthy or not based on the expression levels of a few of important genes.

This library implements a generic algorithm framework to find the optimal solution in an extremely fast way.
This framework now supports the detection of best subset under:
[linear regression](https://abess.readthedocs.io/en/latest/auto_gallery/1-glm/plot_1_LinearRegression.html),
[classification (binary or multi-class)](https://abess.readthedocs.io/en/latest/auto_gallery/1-glm/plot_2_LogisticRegression.html),
[counting-response modeling](https://abess.readthedocs.io/en/latest/auto_gallery/1-glm/plot_5_PossionGammaRegression.html),
[censored-response modeling](https://abess.readthedocs.io/en/latest/auto_gallery/1-glm/plot_4_CoxRegression.html#sphx-glr-auto-gallery-1-glm-plot-4-coxregression-py),
[multi-response modeling (multi-tasks learning)](https://abess.readthedocs.io/en/latest/auto_gallery/1-glm/plot_3_MultiTaskLearning.html), etc.
It also supports the variants of best subset selection like
[group best subset selection](https://abess.readthedocs.io/en/latest/auto_gallery/3-advanced-features/plot_best_group.html),
[nuisance penalized regression](https://abess.readthedocs.io/en/latest/auto_gallery/3-advanced-features/plot_best_nuisance.html),
Especially, the time complexity of (group) best subset selection for linear regression is certifiably polynomial.

## Quick start

The `abess` software has both Python and R's interfaces. Here a quick start will be given and for more details, please view: [Installation](https://abess.readthedocs.io/en/latest/Installation.html).

### Python package

Install the stable version of Python-package from [Pypi](https://pypi.org/project/abess/):

```shell
$ pip install abess
```

or [conda-forge](https://anaconda.org/conda-forge/abess):

```shell
$ conda install abess
```

Best subset selection for linear regression on a simulated dataset in Python:

```python
from abess.linear import LinearRegression
from abess.datasets import make_glm_data
sim_dat = make_glm_data(n = 300, p = 1000, k = 10, family = "gaussian")
model = LinearRegression()
model.fit(sim_dat.x, sim_dat.y)
```

See more examples analyzed with Python in the [Python tutorials](https://abess.readthedocs.io/en/latest/auto_gallery/index.html).

### R package

Install the stable version of R-package from [CRAN](https://cran.r-project.org/web/packages/abess) with:

```r
install.packages("abess")
```

Best subset selection for linear regression on a simulated dataset in R:

```r
library(abess)
sim_dat <- generate.data(n = 300, p = 1000)
abess(x = sim_dat[["x"]], y = sim_dat[["y"]])
```

See more examples analyzed with R in the [R tutorials](https://abess-team.github.io/abess/articles/).

## Runtime Performance

To show the power of abess in computation, we assess its timings of the CPU execution (seconds) on synthetic datasets, and compare to state-of-the-art variable selection methods. The variable selection and estimation results are deferred to [Python performance](https://abess.readthedocs.io/en/latest/auto_gallery/1-glm/plot_a1_power_of_abess.html) and [R performance](https://abess-team.github.io/abess/articles/v11-power-of-abess.html). All computations are conducted on a Ubuntu platform with Intel(R) Core(TM) i9-9940X CPU @ 3.30GHz and 48 RAM.

### Python package

We compare `abess` Python package with `scikit-learn` on linear regression and logistic regression. Results are presented in the below figure:

![](timings.png)

It can be see that `abess` uses the least runtime to find the solution. 
### R package

We compare `abess` R package with three widely used R packages: `glmnet`, `ncvreg`, and `L0Learn`.
We get the runtime comparison results:

![](r_runtime.png)

Compared with other packages,
`abess` shows competitive computational efficiency,
and achieves the best computational power when variables have a large correlation.

## Open source software

`abess` is a free software and its source code is publicly available on [Github](https://github.com/abess-team/abess). The core framework is programmed in C++, and user-friendly R and Python interfaces are offered. You can redistribute it and/or modify it under the terms of the [GPL-v3 License](https://www.gnu.org/licenses/gpl-3.0.html). We welcome contributions for `abess`, especially stretching `abess` to the other best subset selection problems.

## What's news

New features:

- `abess` Python package can be installed via `conda`.
- `abess` R package is is highlighted as one of the core packages in [CRAN Task View: Machine Learning &amp; Statistical Learning](https://cran.r-project.org/web/views/MachineLearning.html).
- On Windows, the recommended C++ compiler shifts from Mingw to Microsoft Visual Studio.
- Support predicting survival function in `abess.linear.CoxPHSurvivalAnalysis`.
- Rename estimators in Python. Please check [here](https://abess.readthedocs.io/en/latest/Python-package/index.html).

New best subset selection tasks:

- Generalized linear model for ordinal regression (a.k.a rank learning in some machine learning literature).

## Citation

If you use `abess` or reference our tutorials in a presentation or publication, we would appreciate citations of our library.

> Jin Zhu, Xueqin Wang, Liyuan Hu, Junhao Huang, Kangkang Jiang, Yanhang Zhang, Shiyun Lin, Junxian Zhu (2022). “abess: A Fast Best Subset Selection Library in Python and R.” Journal of Machine Learning Research (Accepted).

The corresponding BibteX entry:

```
@article{zhu2022abess,
  author    = {Jin Zhu and Xueqin Wang and Liyuan Hu and Junhao Huang and Kangkang Jiang and Yanhang Zhang and Shiyun Lin and Junxian Zhu},
  title     = {abess: A Fast Best Subset Selection Library in Python and R},
  journal   = {Journal of Machine Learning Research (Accepted)},
  year      = {2022}
}
```

## References

- Junxian Zhu, Canhong Wen, Jin Zhu, Heping Zhang, and Xueqin Wang (2020). A polynomial algorithm for best-subset selection problem. Proceedings of the National Academy of Sciences, 117(52):33117-33123.
- Pölsterl, S (2020). scikit-survival: A Library for Time-to-Event Analysis Built on Top of scikit-learn. J. Mach. Learn. Res., 21(212), 1-6.
- Yanhang Zhang, Junxian Zhu, Jin Zhu, and Xueqin Wang (2021). Certifiably Polynomial Algorithm for Best Group Subset Selection. arXiv preprint arXiv:2104.12576.
- Qiang Sun and Heping Zhang (2020). Targeted Inference Involving High-Dimensional Data Using Nuisance Penalized Regression, Journal of the American Statistical Association, DOI: 10.1080/01621459.2020.1737079.
- Jin Zhu, Xueqin Wang, Liyuan Hu, Junhao Huang, Kangkang Jiang, Yanhang Zhang, Shiyun Lin, Junxian Zhu (2022). abess: A Fast Best Subset Selection Library in Python and R. Journal of Machine Learning Research (Accepted).