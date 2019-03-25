## Alignment evidence collection
This repository contains psuedo code required to collect PE, SR, RD, BAF evidences, and those that integrate information per sample to form reference matrix that will be referred to during downstream random forest filtering step.

### PE/SR
 - collect PE/SR evidence:
```
svtk collect-pesr example.bam example_ID example.pe example.sr
```
 - concatinate across samples to form PE/SR matrics:
```
cat *.pe |sort -k1,1 -k2,2n|cut -f 1-7|bgzip -c > ${Name}.pe.sorted.txt.gz
tabix -b 2 -e 2 ${Name}.pe.sorted.txt.gz
cat *.sr |sort -k1,1 -k2,2n|cut -f 1-5|bgzip -c > ${Name}.sr.sorted.txt.gz
tabix -b 2 -e 2 ${Name}.sr.sorted.txt.gz
```

### RD
 - collect bincov evidence:
```
svtk bincov example.bam 1 example.bincov.bed
```
 - concatinate across samples to form bincov matrics:
```
paste ${write_tsv(bincov_per_sample)} ${write_tsv(bincov_paths)} > samples.key;
makeMatrix.sh -z -N -o ${example_batch}.bincov.bed.gz samples.key
```

### B allele frequency (BAF)
note: GATK and baf collection were applied to each batch instead of per sample.

 - apply GATK on to each batch:
```
```
 - collect baf information:
```
vcf2baf.sh example_batch.baf.vcf.gz example_batch.baf.txt
```

 - concatinate across batches to form baf matrics:
```
cat *.baf |sort -k1,1 -k2,2n|bgzip -c > ${Name}.baf.sorted.txt.gz
tabix -b 2 -e 2 ${Name}.baf.sorted.txt.gz
```




