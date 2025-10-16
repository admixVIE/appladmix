[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/admixVIE/appladmix/HEAD)

## Applications of Admixture Genomics (UE UniVienna).

This repo contains the materials for practical sessions, and will be updated accordingly.

To use these materials, you can click the badge [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/admixVIE/appladmix/HEAD), which will create an online virtual machine containing the tools and data used in the practical sessions.

Or you can download this repo and install the dependencies with [miniconda](https://docs.conda.io/en/latest/miniconda.html) in your local machine using the following commands. To install `miniconda`, you can follow the instruction [here](https://conda.io/projects/conda/en/latest/user-guide/install/index.html).

```
git clone https://github.com/admixVIE/appladmix
cd appladmix
conda env create -f environment.yml
conda activate appladmix
```


At the moment, there are the following modules:
- Session 0 (before the course): Basics in bash ("0_basics").
- Session 1: Handling of sequencing and genotype data ("1_data")
- Session 2: Exploratory population genetic analysis; with Challenge ("2_popgen") 
- Session 3: Admixtools, f/D-statistics ("3_admixtools")
- Session 4: Introgression detection with sstar; with Challenge ("4_introgression")



Planned modules are:
- Further population genetics with NGStools, plink
- Handling and exploring ancient DNA sequencing data
- Introgression detection with other tools (in development)
- Simulating data

