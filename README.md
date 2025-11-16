<img width="432" height="11" alt="image" src="https://github.com/user-attachments/assets/b0c14b21-1fd5-4462-bbf0-f6117180a39c" /># Workflow for Algorithm

This repository contains the MATLAB implementation of the workflow of this paper "A-helix Architects the Evolution of the Ribosome." used to compute 3D centers of mass (COM) for rRNA A-helices from PDB structures and to perform the structural distance and curve fitting analyses described in our manuscript.

[Dataset]

[Dataset] : https://github.com/user-attachments/assets/4991d526-863a-4020-b917-cb0748f41b70

The code takes ribosomal PDB files as input, computes COM for each A-helix, summarizes COM positions across species, and produces the distance curves used to construct the rAAA / RAP-tree.

## Repository contents

Main scripts
- `script_for_evolution_algorithm.m` – main pipeline script runs all steps end-to-end.
- `calculate_COM.m` – compute COM for a given PDB file and chain ID and save the result as a text file.
- `new_new_calculateAllCOM.m` – batch COM computation for all helices in each PDB.
- `Nucleotide_COM_species_COM_main.m` – aggregate COM information across species and compute pairwise distances.
- `partition_new.m`, – - `partition_new.m` – partition helices into distance bins for downstream analysis.

By default, the analysis uses a radial bin width of 7 Å when binning the COM distances (DCOM) from the LSU center of mass. This is the setting used to generate the main results in the manuscript.

- `fitted_curve_result_new_2.m` – perform curve fitting on the distance profiles and generate the final summary curves.
- `sort_file.m`, `new_COM_generator.m`, `main_with_function_helices_COM_main.m` – helper scripts used inside the main workflow.

Input / output files (expected by the code)

- `pdbs/` – folder containing input ribosomal PDB files, e.g.
  - `1jj2.pdb`
  - `4v6w-pdb-bundle3.pdb`
  - `4v6x-pdb-bundle3.pdb`
  - `4v9d-pdb-bundle3.pdb`
  - `4v51-pdb-bundle4.pdb`
  - `4v88-pdb-bundle2.pdb`
  - `7l20-pdb-bundle1.pdb`

- `input/` – folder containing input helix index tables


> **Note:** Please place the PDB files in the `pdbs/` folder and the Excel files in the repository root (or update the paths in the scripts accordingly).

## Requirements

- MATLAB R2019b or later
- Bioinformatics Toolbox (for the `pdbread` function)
- Optimization or Curve Fitting Toolbox for the fitting functions used in `fitted_curve_result_new_2.m`

## Quick start

1. Download or clone this repository.
2. Open MATLAB and set the current folder to the root of this repository.
3. Run the main workflow:

```matlab
script_for_evolution_algorithm
```
## License

This project is released under the MIT License. See the `LICENSE` file for details.
