molecule: 2,4,5-trichlorophenoxyacetic_acid

calc_type:
    a) full optimization with Gaussian tight convergence
    b) a few optimization that specified ts optimization
    c) frequency analsysis using finite-differences of gradients

theory: HF/6-31G(d)//HF/6-31G(d)

notes: used in Agent Orange

Energies_raw.csv is in Hartree units
Energies_rel.csv is in kcal/mol

sequence of operations:
1. created conformation 1 using pymol and saved as pdb -> 245_T_conf1.pdb
2. converted pymol's pdb to an xyz -> 245_T_conf1.xyz
3. created the optimization input file using the xyz coordinates -> 245_T_conf1_opt.inp
4. submitted the job to get optimized structure -> 245_T_conf1_opt.log
5. created the output xyz file using the final output of the psi4 log file -> 245_T_conf1_opt.log.xyz
6. create the frequency input files using the optimized xyz coordinates -> 245_T_conf1_freq.inp
7. using the optimized structure, created the other conformations by repeating steps 1-5.
