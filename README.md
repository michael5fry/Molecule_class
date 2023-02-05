# Molecule_class

# For the CLASS to Properly Function:

This is the Molecule Class to analyze and give a template to analyze any single molecule computed with Gaussian. 
The files it requires to properly work are:
1. the output file of the computation called .out --> if you are used to say .log, change it on line 174
2. xyz of the structure you are interested in (If you want to easily get the xyz from the output file check the XYZ_converter.ipynb)
3. the formatted chk file (fchk file)

Furthermore this molecule class requires that the File_Name is the same for each type of file e.g (h2o.out, h2o.xyz, h2o.fchk) 


## CLASS METHODS


1. Bond_Length_Alternation_algoritm(BLA_list_of_Bonds) --> it gives the BLA angles you requested
BLA_list_of_Bonds --> [[1,2], [2,3]] n*2 Matrix with n the number of Bonds you want to put into the BLA ---> [Angstrom]

2. Dihedrals_Taker_V3(bond_list_dihedrals) --> it gives the Dihedral angles you requested
bond_list_dihedrals --> [[1,2,3,4], [5,6,3,4]] n*4 Matrix with n the number of Dihedrals you want [Degree]


3. Distances_Taker_V4(bond_list) --> it gives the Bonds length you requested
bond_list --> [[1,2], [2,3]] n*2 Matrix with n the number of Bonds you want [Angstrom]

4. Homo_Lumo_taker_better() --> it gives the HOMO and LUMO, electronegativity and Gap of the Molecule [eV]

5. molecules_energies() --> it gives the 4 possible thermochemistry energy of the output in order [Hartree]

6. polar_dipole_field_finder() --> it gives the polarizability, and dipole moment of the molecule [CHECK]

7. printer() --> it tells you which is the name of the file you putted as input

8. xyz_file_to_dataframe() --> it transform the xyz file into a Dataframe that it is used anywhere else [Angstrom]
