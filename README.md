# NISTmAb_Rg49
Structures from all-atom MD which have Rg 49.0 +/- 1.2 Angstroms.

From fully solvated all-atom MD simulations of NISTmAb, starting from all-atom model (https://doi.org/10.6028/jres.126.012).
Amber tleap was used to build parameter and coordinates. The protein ff14SB force field and glycam 06j-1 force field were used.
Structure was solvated using SPC/E water, 10 Cl- ions (Joung-Cheatham parameters) were added to neutralize the molecule's charge.
A 10 Angstrom buffer was used, and the resulting simulations averaged 47 Angstroms between periodic images.

Simulations were equilibrated using protocol described here for explicitly solvated systems (https://doi.org/10.1063/5.0013849), and included rounds of minimization followed by MD with decreasing positional restraints, including NPT and NVT equilibration.

Production dynamics were run for 1 microsecond for four replicates using Amber's GPU code. 

The trajectories were analyzed using Cpptraj to calculate Rg, and then selecting frames corresponding to min 47.8 Ang and max 50.2 Ang.

Those frames were combined, and clustered using kmeans on all CA atoms of all residues (:1-1320@CA). 
