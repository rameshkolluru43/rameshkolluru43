# Hi, I'm Ramesh Kolluru 👋

**Computational Fluid Dynamics · Numerical Methods · HPC (CUDA / Metal)**

Senior CFD consultant at [**BosonQ Psi (BQP)**](https://www.linkedin.com/company/bosonq-psi), based in **Sagar, Madhya Pradesh**. I develop advanced flow solvers, hybrid optimization frameworks, and GPU-accelerated PDE codes—with research spanning immersed-boundary methods, pollutant dispersion, hypersonics, and quantum-enhanced simulation approaches.

[![GitHub followers](https://img.shields.io/github/followers/rameshkolluru43?style=social)](https://github.com/rameshkolluru43?tab=followers)
[![GitHub stars](https://img.shields.io/github/stars/rameshkolluru43?style=social)](https://github.com/rameshkolluru43)

---

## About me

Computational fluid dynamics scientist with **20+ years** of experience across consulting, R&D, and teaching in **India, France, and Singapore**, including doctoral research at **IISc Bengaluru** and postdoctoral work on hybrid CFD–optimization frameworks.

- 🔭 **Current focus:** viscous flows, immersed-boundary methods, GPU Poisson/CFD solvers, and quantum-enhanced numerics (CVQLS, QAPINN)
- 🧮 **Methods:** GMRES, finite-volume / finite-difference schemes, CMC & ISRN for turbulent reacting flows, MPI-parallel CFD
- 🏢 **BQP** — quantum-powered physics simulation & optimization ([BosonQ Psi](https://www.linkedin.com/company/bosonq-psi))
- 🎓 **Background:** Cambridge CARES (Research Fellow) · IISc (Postdoc) · B.M.S. College of Engineering (Faculty) · IIT Madras (Research Scholar)

---

## Focus areas

| Area | Topics |
|------|--------|
| **CFD & HPC** | Immersed boundary methods, CUDA / Metal kernels, Poisson & Laplace solvers, OpenFOAM |
| **Marine & environmental** | Ship line heating, exhaust dispersion (ISRN/CMC), Gaussian plume baselines, naval architecture & propulsion |
| **Optimization** | Hybrid gradient / metaheuristic solvers coupled with in-house CFD (scramjet inlet design, etc.) |
| **Teaching** | *Python for Marine Engineering* — 2-semester LaTeX course (2026): numerics, pandas, marine KPIs, propulsion & condition monitoring |
| **Numerical methods** | GMRES, spectral & orthogonal basis functions, tensor-train linear algebra |

---

## Marine & ship modeling

### 🔥 Ship line heating (3D thermo-mechanics)

Coupled **transient heat transfer + thermoelasticity** workflow for **ship-plate line heating** and permanent bending:

- **Forward problem:** prescribed torch temperature (e.g. 900 K) → predicted curvature profile
- **Inverse problem:** target curvature + plate geometry → optimal heating pattern
- **Numerics:** Gmsh tetrahedral mesh (refined along heating lines), moving Gaussian surface heat flux, convection/radiation, 3D linear thermoelasticity (`thermo_bindings`), optional **inherent-strain** surrogate for residual bend
- **Outputs:** VTK (ParaView), plots, LaTeX/PDF reports; optional PINN paths (DeepXDE / Modulus)

### 🚢 Ship pollution — ISRN & CMC

**In-Situ Reaction Network (ISRN)** with **Conditional Moment Closure (CMC)** for ship-exhaust and atmospheric reacting flows, integrated with [**CONVERGE**](https://convergecfd.com/) CFD:

- Fortran production library + **C++ port** (Eigen, MPI, HDF5 restart) and unified Doxygen docs
- Resolves **micromixing** and fast chemistry (e.g. **NO, NO₂, SO₄**) behind large marine sources—beyond mean-field assumptions
- Application context: pollutant dispersion in the wake of a **~270 m oil tanker** (Cambridge CARES); CONVERGE UDF workflow for plume analysis with RANS/LES and detailed chemistry

### 🌫️ Gaussian plume modeling

Atmospheric **Gaussian plume** dispersion software used as a **regulatory / screening baseline** and for **manuscript comparison** against high-fidelity models:

- Reflected-ground point source: Pasquill–Gifford & **Briggs** σ models (class D stability)
- Computes mass concentration **C** [kg/m³] and passive scalar **ξ = C/ρ_source** for direct comparison with CFD/CMC/ISRN fields
- Python CLI + Tkinter GUI: contours, crosswind/vertical profiles, skewed-wind receptors, literature benchmark cases
- Validates when classical plume theory is sufficient vs. when **CMC/ISRN micromixing** and 3D CFD are required

```mermaid
flowchart LR
  A[Ship exhaust / stack] --> B[Gaussian plume baseline]
  A --> C[CONVERGE CFD + ISRN/CMC]
  B --> D[Screening & ξ comparison]
  C --> D
  E[Line heating torch] --> F[3D thermo-FEM]
  F --> G[Plate curvature forward / inverse]
```

---

## Tech stack

<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Fortran-734F96?style=for-the-badge&logo=fortran&logoColor=white" alt="Fortran"/>
  <img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="CUDA"/>
  <img src="https://img.shields.io/badge/Metal-000000?style=for-the-badge&logo=apple&logoColor=white" alt="Metal"/>
  <img src="https://img.shields.io/badge/OpenFOAM-1E6E9C?style=for-the-badge&logo=openfoam&logoColor=white" alt="OpenFOAM"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
  <img src="https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white" alt="LaTeX"/>
  <img src="https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white" alt="CMake"/>
  <img src="https://img.shields.io/badge/MPI-0091BD?style=for-the-badge&logo=openmpi&logoColor=white" alt="MPI"/>
</p>

---

## Featured repositories

| Project | Description | Stack |
|--------|-------------|-------|
| [**IBM_Viscous**](https://github.com/rameshkolluru43/IBM_Viscous) | Immersed-boundary method for viscous flows | C++ |
| [**CFD_Solver_withCUDA**](https://github.com/rameshkolluru43/CFD_Solver_withCUDA) | CFD solver with CUDA kernels | CUDA |
| [**Poisson_Metal_CUDA**](https://github.com/rameshkolluru43/Poisson_Metal_CUDA) | Laplace / Poisson solvers on Metal and CUDA | C++ |
| [**GMRES_Python**](https://github.com/rameshkolluru43/GMRES_Python) | GMRES iterative solver experiments | Python |
| [**BQP_Drive**](https://github.com/rameshkolluru43/BQP_Drive) | BQP project resources & shared work | — |

---

## GitHub stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=rameshkolluru43&show_icons=true&theme=github_dark&hide_border=true" alt="GitHub stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rameshkolluru43&layout=compact&theme=github_dark&hide_border=true" alt="Top languages"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=rameshkolluru43&theme=github-dark-blue&hide_border=true" alt="GitHub streak"/>
</p>

---

## What I'm exploring

- 🌱 GPU porting and kernel tuning (CUDA ↔ Metal)
- 🔬 Quantum-enhanced CFD workflows at BQP
- 👯 Collaborations on **ship line heating**, **ISRN/CMC ship pollution**, **Gaussian plume baselines**, and **marine propulsion**
- 💬 Happy to discuss **line-heating FEM**, **CMC/ISRN**, **CONVERGE UDFs**, **Poisson solvers**, **GMRES**, and **HPC profiling**

---

## Connect

<p>
  <a href="mailto:rameshkolluru43@gmail.com">
    <img src="https://img.shields.io/badge/Email-rameshkolluru43@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <a href="https://www.linkedin.com/in/drrameshkolluru">
    <img src="https://img.shields.io/badge/LinkedIn-drrameshkolluru-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://github.com/rameshkolluru43">
    <img src="https://img.shields.io/badge/GitHub-rameshkolluru43-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
  <a href="https://scholar.google.co.in/citations?user=Zzl8hbwAAAAJ&hl=en">
    <img src="https://img.shields.io/badge/Google_Scholar-Publications-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white" alt="Google Scholar"/>
  </a>
  <a href="https://orcid.org/0000-0001-5447-8550">
    <img src="https://img.shields.io/badge/ORCID-0000--0001--5447--8550-A6CE39?style=for-the-badge&logo=orcid&logoColor=white" alt="ORCID"/>
  </a>
</p>

📫 **rameshkolluru43@gmail.com** · [LinkedIn](https://www.linkedin.com/in/drrameshkolluru) · [Google Scholar](https://scholar.google.co.in/citations?user=Zzl8hbwAAAAJ&hl=en) · [ORCID 0000-0001-5447-8550](https://orcid.org/0000-0001-5447-8550)

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=rameshkolluru43&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views"/>
</p>
