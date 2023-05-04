# MaGeCK

The list of files to prepare before running mageck
- feature count tables (could start from fastq as well)
- design matrix
- negative control guide list
- SSC scoring file (will be covered later)

With all those files in certain repository run mageck with below command
```
# "You should have mageck conda environment installed" (Otherwise, 
conda activate mageck
```

With UMI: Get feature count tables using Robins 'feature-barcode-qc' snakemake files (This script shrink UMI)
Without UMI: You can also run the mageck mle pipeline to get feature count table

# Making SSC matrix based on the sequence
https://sourceforge.net/p/mageck/wiki/advanced_tutorial/#tutorial-5-include-the-sgrna-efficiency-into-mle-calculation
```
conda activate mageck
```
Follow all protocols as it's described. Download SSC from the link. Before executing './SSC -l 20 -m SSC0.1/matrix/human_CRISPRi_20bp.matrix -i tim.library.in -o tim.library.out' code, you need to move 'SSC' execution file into the parental directory where your library file is in. It's in 'SSC0.1/bin' Copy and paste the execution file into somewhere where your '.in' file is located
```
