This repository includes tools and scripts adopte to run SV discovery algorithms on CMC samples.

## SV discovery algorithms applied:
 - 4 pair end(PE) / split read(SR) algorithms: **DELLY**, **LUMPY**, **Manta**, **WHAMG** 
 - 3 read depth(RD) algorithm:  **CNVnator**, **cn.MOPS**, **GenomeSTRiP**
 - 1 mobile element insertion(MEI) discovery method: **MELT**

### DELLY
 - software: [https://github.com/dellytools/delly](https://github.com/dellytools/delly)
 - reference: [Rausch, Tobias, et al. 2012](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3436805/)
 - command:

### LUMPY
 - software: [https://github.com/arq5x/lumpy-sv](https://github.com/arq5x/lumpy-sv)
 - reference: [Layer, Ryan M., et al. 2014](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2014-15-6-r84)
 - command:

### Manta
 - software: [https://github.com/Illumina/manta](https://github.com/Illumina/manta)
 - reference: [Chen, Xiaoyu, et al. 2015](https://academic.oup.com/bioinformatics/article/32/8/1220/1743909)
 - command:

### WHAMG
 - software: [https://github.com/zeeev/wham](https://github.com/zeeev/wham)
 - reference: [Kronenberg, Zev N., et al. 2015](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004572)
 - command:

### CNVnator
 - software: [https://github.com/abyzovlab/CNVnator](https://github.com/abyzovlab/CNVnator)
 - reference: [Abyzov, Alexej, et al. 2011](https://genome.cshlp.org/content/21/6/974.short)
 - command:

### cn.MOPS
 - software: [https://github.com/Bioconductor/copy-number-analysis/wiki/cn.mops](https://github.com/Bioconductor/copy-number-analysis/wiki/cn.mops)
 - reference: [Klambauer, Günter, et al. 2012](https://academic.oup.com/nar/article/40/9/e69/1136601)
 - command:

### GenomeSTRiP
 - software: [http://software.broadinstitute.org/software/genomestrip/](http://software.broadinstitute.org/software/genomestrip/)
 - reference: [Handsaker, Robert E., et al. 2011](https://www.nature.com/articles/ng.768)
 - command:

### MELT
 - software: [http://melt.igs.umaryland.edu/manual.php](http://melt.igs.umaryland.edu/manual.php)
 - reference: [Gardner, Eugene J., et al. 2017](https://genome.cshlp.org/content/27/11/1916.short)
 - command:


## SV clustering across each batch
### SVTK
 - software: [https://github.com/talkowski-lab/svtk](https://github.com/talkowski-lab/svtk)
 - reference: [Werling, Donna M., et al. 2018](https://www.nature.com/articles/s41588-018-0107-y)

### PE/SR collection
 - command: 

### RD collection
 - command: 

## Alignment evidence collection

### PE/SR
 - command:
```
svtk collect-pesr example.bam example_ID example.pe example.sr
```

### RD
 - command:
```
svtk bincov example.bam 1 example.cov
```

### B allele frequency (BAF)
 - command:





