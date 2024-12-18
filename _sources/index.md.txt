---
hide-toc: true
---

# Repo4Cat Documentation Hub

This is work in progress...

::::{grid} 3
:::{grid-item-card}
:link: https://github.com/nfdi4cat/repo4cat/
**Link A**, Anna
^^^

```{image} _static/fig_A.svg
:align: center
:alt: screenshot of documentation
```

+++
<small>Most current</small>
:::

:::{grid-item-card}
:link: https://github.com/nfdi4cat/repo4cat/
**Link B**, Berta
^^^

```{image} _static/fig_B.svg
:align: center
:alt: screenshot of file
```
+++
<small>Download to contribute</small>
:::

:::{grid-item-card}
:link: https://w3id.org/nfdi4cat/repo4cat/
**Link C**, Charla
^^^

```{image} _static/fig_C.svg
:align: center
:alt: screenshot of file 3
```

+++
<small>Download to contribute</small>
:::
::::

More text ....

```{toctree}
:hidden:
Overview <self>
GitHub page <https://github.com/nfdi4cat/repo4cat>
About <usage/about>
```

```{toctree}
:caption: For Users
:hidden:
:maxdepth: 2

usage/how-to-use
usage/how-to-contribute
usage/guidelines
```

```{toctree}
:caption: For Maintainers
:glob:
:hidden:

maintenance/*
```
