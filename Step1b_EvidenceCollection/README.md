## Alignment evidence collection
This repository contains scripts required to collect PE, SR, RD, BAF evidences, and those that integrate information per sample to form reference matrix that will be referred to during downstream random forest filtering step.

### PE/SR
 - command:
```svtk collect-pesr example.bam example_ID example.pe example.sr
```

### RD
 - command:
```svtk bincov example.bam 1 example.cov
```

### B allele frequency (BAF)
 - apply GATK on to each batch:
```
```
 - collect baf information:
```
```





