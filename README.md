# Nicole Tueni

R&D engineer in computational biomechanics at FAU Erlangen-Nürnberg, working on **patient-specific brain simulations**.
I contribute to the BRAINIACS group's shared simulation code: a C++ finite-element library built on deal.II, and a Python pipeline that turns MRI data into finite-element models.

---

## Contributions to BRAINIACS group code

### FA-based heterogeneous brain tissue — C++ / deal.II
[`EFI_atrophy_and_tumor` · branch `atrophy_FA_integration`](https://github.com/BRAINIACS-Group/EFI_atrophy_and_tumor/tree/atrophy_FA_integration)
Extends the brain atrophy simulation from region-wise to **voxel-wise shear modulus**, computed element by element from diffusion MRI fractional anisotropy (FA) maps. Adds FA data as a model input and exports the resulting material parameters (alpha, mu) for analysis.

### Tumor growth simulation — C++ / deal.II
[`EFI_atrophy_and_tumor` · branch `tumor_growth_NT`](https://github.com/BRAINIACS-Group/EFI_atrophy_and_tumor/tree/tumor_growth_NT)
Extends the tumor growth model: multiplicative growth applied to tumor regions within a modified one-term Ogden material model, revised material and boundary conditions, hydrostatic stress output, reduced output size, and bug fixes.

### MRI-to-mesh pipeline with FA integration — Python
[`Brain-Creation-Code` · branch `FA_integration`](https://github.com/BRAINIACS-Group/Brain-Creation-Code/tree/FA_integration)
Extends the model-creation pipeline (FreeSurfer segmentation → finite-element mesh + simulation parameter files) to process FA images during meshing. The resulting meshes feed directly into the C++ atrophy simulations above.
I also continue development of the main [Brain-Creation-Code](https://github.com/BRAINIACS-Group/Brain-Creation-Code) pipeline.

### Brain mesher with skull layer
[`brain-mesher-skull-layer`](https://github.com/BRAINIACS-Group/brain-mesher-skull-layer)

---

## Own repositories

- [`linear_periodic_homogenization`](https://github.com/ntueni/linear_periodic_homogenization) — linear periodic homogenization applied to cardiac tissue (from my PhD, Python).

---

