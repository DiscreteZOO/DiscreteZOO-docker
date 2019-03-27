# DiscreteZOO Sage docker image (experimental)

[![Launch in Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/DiscreteZOO/DiscreteZOO-docker/master)

[*DiscreteZOO*](http://discretezoo.xyz) is a project combining a central repository of discrete objects, its website front-end and extensions for software packages like [Sage](http://sagemath.org). The repository contains certain precomputed properties to speed up the processes of filtering, searching and computation. For now, it can store graphs, with the groundwork already laid out for more combinatorial objects (such as maps, maniplexes, geometries, etc.).

This Docker image contains Sage and the DiscreteZOO [package](https://github.com/DiscreteZOO/DiscreteZOO-sage) together with the latest [database](https://data.discretezoo.xyz/discretezoo.db), which currently contains graphs from three distinct censuses. It is based off a version of the [`sagemath/sagemath`](https://hub.docker.com/r/sagemath/sagemath/) image suitable for running on [Binder](https://mybinder.org).

This version of the image currently does not compile, as the `sagemath/sagemath` image does not contain the required build tools.
