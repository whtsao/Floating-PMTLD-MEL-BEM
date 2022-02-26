# PMTLD-in-waves

Description:

Two-dimensional fluid-structure interaction problem of a water tank filled with porous media installed on a rectangle floating platform in waves.

Water wave problem:

A) The numerical method can be referred to repository 'potential flow wave problem'.

B) Three kinds of boundary conditions can be applied to left- and right-side of the channel.
  1. Wavemaker: piston type or flap type
  2. Stationary wall
  3. Radiation

Rigid-body dynamics:

A) The floating body dynamics is completed by Newmark method with constant acceleration assumption.

B) The velocity and acceleration of the body surface will be involded in the flow computation as boundary conditions. They are coupled by iterative algorithm for force convergence.

Porous-media tuned liquid damper (PMTLD):

A) Potential flow model:
  1. Dracy and Forchheimer flow regimes are considered.
  2. Eulerian - Lagrangian method is completed by BEM for free-surface omputation.
  3. Numerical method can be referred to article 'Sloshing force in a rectangular tank with porous media (2021)'

B) Mechanical model:
  1. Only Darcy's resistance is considered.
  2. Linear wae theory is applied.
  3. If this model is used, the flow computation can be transferred to several motion equations of a MDOF system that is solved by Newmark method.
  4. Complete model can be referred to article 'An equivalent mechanical model with nonlinear damping for sloshing rectangular tank with porous media (2021)'
