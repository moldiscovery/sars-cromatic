# This directory contains the folowing files #

1. ANNOTATION.csv 
  - This file contains, for each cavity in the full collection, all annotations:
     - cavity_inchi: a uniq identifier for the protein cavity
     - cavity_filename: the corresponding cavity file located in /files/ directory
     - protein_filename: the corresponding protein file located in /files/ directory
     - representative: it is 'yes' if the cavity is in the non-redundant collection
     - representative_name: if cavity is representative, the name reported in the similairty matrix and pairs is indicated
     - protein_name: name of the protein 
     - domain: domain of the protein
     - organism: organism of the protein
     - protein_code: Protein Data Bank ID of protein
     - chain_code: Protein Data Bank ID of chain
     - ligand_code: if cavity contains a ligand, the 3 letter code of the ligand is reported; if ligand comes from Biologically Interesting Molecule Reference Dictionary ('BIRD'), 'birds_' is reported; if ligand is a small peptide, 'small_peptide_*' is reported.
     - ligand_occupancy: if cavity contains a ligand, the fraction of ligand in the cavity is reproted
     - int.protein_code: if cavity is in a protein-protein interaction region, the Protein Data Bank ID of the interactor is reported
     - int.chain_code: if cavity is in a protein-protein interaction region, the Protein Data Bank chain ID of the interactor is reported
     - int.protein_name: if cavity is in a protein-protein interaction region, the name of the interactor is reported
     - int.domain: if cavity is in a protein-protein interaction region, the protein domain of the interactor is reported
     - int.organism : if cavity is in a protein-protein interaction region, the organism of the interactor is reported

2. CROMATIC-full_matrix.tsv & CROMATIC-similar_pairs.csv
 - These two files contain the similarity values among all the cavities in the non-redundant collection. 
   - CROMATIC-full_matrix.tsv: it contains square matrix resulting from 'all against all' comparison
   - CROMATIC-similar_pairs.csv: it reports only similar cavity pairs (score >= 0.8)

3. files
 - This directory contains .pdb files of proteins, cavities and ligands. For example: /6lu71/ contains:
    - 6lu71_1_A.pdb: protein file, model 1       
    - 6lu71_2_A.pdb: protein file, model 2  
    - 6lu71.pdb: protein file, dimer
    - 6lu7.pdb1: orginal biological unit
    - birds_1_C.pdb: bird ligand on model 1 
    - birds_2_C.pdb: bird ligand on model 1 
    - birds_C.pdb: bird ligand (multi model)
    - duplicates_6lu71_1_A.txt: pairs of replicates cavities on the biological unit
    - Pocket_*_6lu71_1_A.pdb: Cavity shapes
    - PocRes_*_6lu71_1_A.pdb: Cavity residues
    - redundant: directory containing one of the duplicates cavity (not considered in the followinhg steps)

4. IMPLEMENTATION.txt
- It contains command lines used for implementing the cavities collection and the cross-relationship map.The BioGPS software, containing flap* executables is available from https://www.moldiscovery.com/and trial licenses are available to both commercial and academic users.

5. README.md
This file
