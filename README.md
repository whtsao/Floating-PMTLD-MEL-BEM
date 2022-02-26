# PMTLD-in-waves
Tuned liquid damper filled with porous media installed on a Floating body

Two-dimensional fluid-structure interaction problem of a water tank filled with porous media installed on a rectangle floating platform in waves.

Water wave problem:
The numerical method can be referred to repository 'potential flow wave problem'.

Rigid-body dynamics:
The floating body dynamics is completed by Newmark method with constant acceleration assumption.

Porous-media tuned liquid damper (PMTLD):
Two solvers can be used.
A) Potential flow model:
  1. Dracy and Forchheimer flow regimes are considered.
  2. Eulerian - Lagrangian method is completed by BEM for free-surface omputation.
B) Mechanical model:
  1. Only Darcy's resistance is considered.
  2. Linear wae theory is applied.

The coupling behavior is solved by iterative algorithm for force convergence.
