# R
Singularity image for R 4.2.3, alongside the libraries needed to install `devtools` and `usethis`.

## Notes
To install packages, run the Singularity shell as:
```
singularity shell singularity-r.sif
```
Inside singularity's shell, run the following commands:

```
mkdir -p $HOME/apps/R_Singularity/4.2.3
export R_LIBS_USER=$HOME/apps/R_Singularity/4.2.3:$R_LIBS_USER
R
```

Inside R, install the required packages:

```
install.packages("devtools")
install.packages("usethis")
```
