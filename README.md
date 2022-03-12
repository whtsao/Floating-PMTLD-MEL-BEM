# PMTLD-in-waves

Developed by Wen-Huai Tsao at LSU-CE Feb. 2022

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
  1. Dracy and Forchheimer flow regimes are considered via two damping coefficients used in the code.
  2. Eulerian - Lagrangian method is completed by BEM for free-surface computation.
  3. Numerical method can be referred to article 'Sloshing force in a rectangular tank with porous media (2021)'

B) Mechanical model:
  1. Only Darcy's resistance is considered.
  2. Linear wae theory is applied.
  3. If this model is used, the flow computation can be transferred to several motion equations of a MDOF system that is solved by Newmark method.
  4. Complete model can be referred to article 'An equivalent mechanical model with nonlinear damping for sloshing rectangular tank with porous media (2021)'

C) None:
  This will remove the PMTLD from the floating body. Then the FSI problem only involves floating body and ambient waves.

INPUT:

1.ipt - Wave configuration for dimensions, element number, time interval, tolerent error, etc.

2.ipt - BS setup for wavemaker types, wave gauges, body initial state, body free dof, etc.

3.ipt - PMTLD parameters for dimensions, element number, linear and nonlinear damping coefficients, etc.

4.ipt - State-space metrice for MDOF system on the floating body. Current unavailable.

OUTPUT:

Z.DAT - displacement, velocity, and acceleration of COG of body in three directions.

RB.DAT - corner node of the body.

F.DAT - wave loading, sloshing reaction, and total resultant act on the body.

E.DAT - kenetic energy, potentail energy, total energy, and external work of the wave-body-PMTLD system.

WG.DAT - wave elevations of the PMTLD (_tld) and water wave (_wave). For PMTLD, wave gauges on both side walls. For water wave, wave gauges are arbitrary placed by 2.ipt

S.DAT - boundary shape of the PMTLD (_tld) and water wave (_wave).

Next version to be continued:
  1. Floating body with mooring lines
  2. 3D FSI problem
  3. Offshore wind turbine design and vibration control
