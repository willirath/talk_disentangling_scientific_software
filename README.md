# Disentangling Scientific Software

Launch interactive version: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/willirath/talk_disentangling_scientific_software/v2022.01.08.1?urlpath=lab/tree/00_welcome.ipynb)

This is a lecture on dissecting a piece of scientific software.

## Outline

### Messy but realistic toy model

[Click here to view the notebook.](https://nbviewer.jupyter.org/github/willirath/talk_disentangling_scientific_software/blob/v2022.01.08.1/01_a_toy_black_box.ipynb)

I'll first show a very simple physical model (many particles randomly moving around in a 2-dimensional box) that allows for calculating (or diagnosing) physical quantities.  We'll use the [center of mass](https://en.wikipedia.org/wiki/Center_of_mass) and the [moment of inertia](https://en.wikipedia.org/wiki/Moment_of_inertia) across all the particles.

The implementation of this example will be messy but fairly realistic.

### Dissecting the structure

[Click here to view the notebook.](https://nbviewer.jupyter.org/github/willirath/talk_disentangling_scientific_software/blob/v2022.01.08.1/02_separation.ipynb)

I'll then go on to separate different parts of the model (space where the particles live, a group of particles, a source of randomness) to more clearly understand the relationship between the different parts.

The implementation of that part will be what scientific software developers do if the modularize their software for better understanding the structure, for separating the development into work packages, etc.

### Distributing the different parts of the model

[Click here to view the notebook.](https://nbviewer.jupyter.org/github/willirath/talk_disentangling_scientific_software/blob/v2022.01.08.1/03_using_actors.ipynb)

Finally, I'll use [Dask](https://dask.org/) to distribute the model.  Each component will live on a different worker (can be threads, processes, nodes in a cluster, different data centres, ...).  All parts will talk to each other using [actors](https://en.wikipedia.org/wiki/Actor_model).

### Room for own work

[Click here to view the notebook.](https://nbviewer.jupyter.org/github/willirath/talk_disentangling_scientific_software/blob/v2022.01.08.1/04_go_on_from_here.ipynb)

The distributed step will be used as a starting point to think about

- how to add components to the model
- how to optimize the layout of the different components under different conditions
- how to ensure reproducibility of the computation
- ...
