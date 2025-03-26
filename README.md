# zwitterFF
=================================================

[Pramudit Tripathi](https://www.linkedin.com/in/pramuditt/) and [Scott T. Milner](https://sites.psu.edu/stm9research/)

Department of Chemical Engineering

The Pennsylvania State University


*zwitterFF* is an OPLS based force field for molecular dynamics simulations of zwitterions and their polymers.
It coarse grains most alkane hydrogen atom and employes virtual cites and lincs algorithms to represent stiff parts of the molecules.
This accelerates simulations to access time scales to equilibrate slow charged polymers, i.e. poly-zwitterions,
without sacrificing much chemical resolution.

The files represent some molecules studied in this article:
[doi:10.1021/acscentsci.1c01260](https://pubs.acs.org/doi/full/10.1021/acscentsci.1c01260)

Our publication is under review.

zwitterFF is self containted: it does not need any additional force field parameters from GROMACS.

The folder `top_ZIL` contains files for small-molecule zwitterions, while `top_pZIL` contains files for poly-zwitterions.
The file `system.top` can be edited to change the number of zwitterions or salt molecules in the simulation.
The parameters are optimized to be simulatied with a background dielectric constant of 2.
`epsilon-r=2` must be included in `.mdp` file for the simulaton.

zwitterFF builds upon the [OPLS-VSIL](https://github.com/orlandoacevedo/IL.git), all atom force field for ionic liquids,
to arrive at parameters for zwitterions.
Instead of using charge scaling, we use a background dielectric constant of 2 in our simultions.
[OPLS-VSIL](https://github.com/orlandoacevedo/IL.git) is the work of
Dr. [Orlando Acevedo](https://web.as.miami.edu/chemistrylabs/acevedogroup/), University of Miami.
