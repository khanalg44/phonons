# phonons

Basically the idea is to calculate phonons within DFT+DMFT formalism.

#Few thoughts

The Phonopy code formulation can be found here
https://atztogo.github.io/phonopy/formulation.html

For phonon band structure calculate the Dynamical Matrix (DM) for a given
q point. The size of a DM is 3N where N is the # of atoms in the Unit cell.
For example For FeSe with 4 atoms per unit cell, the DM will have 4 blocks
of 3x3 matrices.
Diagonalize the matrix and obtain omega squared for each bands. take squared 
rood and then you'll get the phonon frequency at a given q point.

In the website given above, it can be seen that we need Force Constants to
calculate the DM. We plan to get Force Sets from other methods (DFT, DMFT) 
and calculate FORCE_CONSTANTS (Phi's).
