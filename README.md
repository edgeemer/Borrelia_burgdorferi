
<h3 align="center">Current pipleine</h3>
  
|State|Step|Software|Brief description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |  |
| 🟩 | 4 | SPAdes | Reads -> scaffolds |  |  |
| 🟩 | 5 | custom script | Polishing scaffolds (len and coverage) | [Coverage report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/86969b7b0d02f612bfcbaf97d3bcf47b85117c10/Reports/Coverage_SPAdes_report.md) |  |
| 🟩 | 6 | QUAST + CheckM | Quality check | [MultiQC_QUAST](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST/) \| [MultiQC_QUAST_plasmid](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST_plasmid/) \| [CheckM_report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/9c0f8b651fe3bc0402f85996132c94f22af79388/Reports/CheckM_result.md) |  |
| 🟨 | 7 | bowtie-build | create basenames |  | Decided to redo with some tweaks |
| 🟨 | 8 | Bowtie2 | Mapping raw reads |  | Decided to redo with some tweaks |
| 🟨 | 9 | samtools | SAM file to BAM |  | Decided to redo with some tweaks |
| 🟨 | 10 | samtools | Sort and index the BAM file |  | Decided to redo with some tweaks |
| ⬜️ | 11 | Prokka | Annotating of the high-quality assemblies |  |  |
