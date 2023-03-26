
<h3 align="center">Current pipleine</h3>
  
|State|Step|Software|Brief description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |  |
| 🟩 | 4 | SPAdes | Reads -> scaffolds |  |  |
| 🟩 | 5 | custom script | Polishing scaffolds (len and coverage) |  |  |
| 🟩 | 6 | QUAST + CheckM | Quality check | [MultiQC_QUAST](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST/) \| [CheckM_report](https://github.com/edgeemer/CheckM_report/blob/feff9fd5d0e1a6ccfc96b56cbe2bed829091200b/README) |  |
| 🟩 | 7 | bowtie-build | create basenames |  |  |
| 🟩 | 8 | Bowtie2 | Mapping raw reads |  |  |
| 🟩 | 9 | samtools | SAM file to BAM |  |  |
| 🟩 | 10 | samtools | Sort and index the BAM file |  |  |
| ⬜️ | 11 | Prokka | Annotating of the high-quality assemblies |  |
