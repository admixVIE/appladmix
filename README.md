[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/admixVIE/appladmix/HEAD)
[![Linux build Status](https://github.com/admixVIE/iNEAL/actions/workflows/ubuntu-build.yml/badge.svg?branch=main)](https://github.com/admixVIE/appladmix/actions)
[![macOS build Status](https://github.com/admixVIE/iNEAL/actions/workflows/macos-build.yml/badge.svg?branch=main)](https://github.com/admixVIE/appladmix/actions)

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
- Basics in bash and handing of sequencing data ("basics").
- VCF files and bcftools; with Challenge ("vcf")
- Admixtools, f/D-statistics & intro to R ("admixtools")
- Introgression detection with sstar; with Challenge ("introgression")

Planned modules are:
- Detection of  Selection
- Introgression detection with hmmix
- Explorative data analysis with PCA, clustering and NGStools
- Handling amd exploring ancient DNA sequencing data
- Simulating data


