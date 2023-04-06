
<h3 align="center">Current pipleine</h3>
  
|State|Step|Software|Brief description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |  |
| 🟩 | 4 | SPAdes | Reads -> scaffolds |  |  |
| 🟩 | 5 | custom script | Polishing scaffolds (len and coverage) | [Coverage report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/86969b7b0d02f612bfcbaf97d3bcf47b85117c10/Reports/Coverage_SPAdes_report.md) \| [Plasmid Coverage report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/dbe2e43aecbf186ad0d9272a0bb710274e233043/Reports/Coverage_SPAdes_plasmid_report.md) |  |
| 🟩 | 6 | QUAST + CheckM | Quality check | [MultiQC_QUAST](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST/) \| [CheckM_report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/9c0f8b651fe3bc0402f85996132c94f22af79388/Reports/CheckM_result.md) \ [MultiQC_QUAST_plasmid](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST_plasmid/) \| [CheckM_plasmid_report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/4b76ed1e7a865df019c402501f47282d3407ed6b/Reports/CheckM_plasmid_report.md) |  |
| ⬜️ | 7 | Prokka | Annotating of the high-quality assemblies |  |  |
