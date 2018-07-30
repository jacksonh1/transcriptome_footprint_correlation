# This repo is not for sharing with others. I am just learning how to use Git/Github with ongoing work

---

# ribosome profile correlation between replicates

alignments are from `/Volumes/external2/rpf-external/alignments/yeast/orf_coding-FILTERED1`
they are bbmap trimmed to length 29

---

- get genome coverage for all transcripts for the 2 replicates
- get pearson correlation between replicates for each transcripts ribosome profile
- coverage depth: `bedtools genomecov -d -ibam [sorted bam file] > [file.tsv]`
	- or `bedtools genomecov -d -ibam [sorted bam file] | gzip > [file.tsv.gz]`
- do this for replicates aligned with `-a`, `-m 1`, and `-k 1`

---

### find files
- `find . -name "*.bam" > bam_files.txt`
- manually delete realignment bams

`./SRR948553_BBduk2_NEBtrim-rRNA-bbmap_trim_29-alignment--norc-a-v2-p4/SRR948553_BBduk2_NEBtrim-rRNA-bbmap_trim_29--norc-a-v2-p4.sorted.bam`
`./SRR948553_BBduk2_NEBtrim-rRNA-bbmap_trim_29-alignment--norc-k1-v2-p4/SRR948553_BBduk2_NEBtrim-rRNA-bbmap_trim_29--norc-k1-v2-p4.sorted.bam`
`./SRR948553_BBduk2_NEBtrim-rRNA-bbmap_trim_29-alignment--norc-v2-p4-m1/SRR948553_BBduk2_NEBtrim-rRNA-bbmap_trim_29--norc-v2-p4-m1.sorted.bam`
`./SRR948555_BBduk2_NEBtrim-rRNA-bbmap_trim_29-alignment--norc-a-v2-p4/SRR948555_BBduk2_NEBtrim-rRNA-bbmap_trim_29--norc-a-v2-p4.sorted.bam`
`./SRR948555_BBduk2_NEBtrim-rRNA-bbmap_trim_29-alignment--norc-k1-v2-p4/SRR948555_BBduk2_NEBtrim-rRNA-bbmap_trim_29--norc-k1-v2-p4.sorted.bam`
`./SRR948555_BBduk2_NEBtrim-rRNA-bbmap_trim_29-alignment--norc-v2-p4-m1/SRR948555_BBduk2_NEBtrim-rRNA-bbmap_trim_29--norc-v2-p4-m1.sorted.bam`
