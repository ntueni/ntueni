# Nicole Tueni

R&D engineer in computational biomechanics at FAU Erlangen-Nürnberg, working on **patient-specific brain simulations**.
I contribute to the BRAINIACS group's shared simulation code: a C++ finite-element library built on deal.II, and a Python pipeline that turns MRI data into finite-element models.

---

## Contributions to BRAINIACS group code

###  Reaction–diffusion tumor growth in brain tissue — C++ / deal.II
[efi-growth-diffusion-reaction · branch main](https://github.com/BRAINIACS-Group/efi-growth-diffusion-reaction)
Couples tumor cell concentration to nonlinear brain mechanics through an accumulated growth field and a multiplicative split F = F_e · F_g, which deforms and stresses the surrounding tissue (region-wise modified one-term Ogden material). On main, the concentration comes from a reaction–diffusion model (explicit finite-volume diffusion with logistic proliferation). 
[efi-growth-diffusion-reaction · branch image-driven-growth](https://github.com/BRAINIACS-Group/efi-growth-diffusion-reaction/tree/image-driven-growth) On image-driven-growth, it is read from a NIfTI time series registered to the mesh, one image per time step, which allows to simulate patient-specific tumor evolution. Both versions are verified against analytical and synthetic test cases, and export concentration, growth, displacement and stress fields (hydrostatic, von Mises) for ParaView.

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

