
<h3 align="center">Current pipleine</h3>
  
|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Initial Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Step 2 Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |  |
| 🟩 | 4 | SPAdes | Assembly |  |  |
| 🟩 | 5 | custom script | Filtering scaffolds (len and coverage) | [Coverage report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/86969b7b0d02f612bfcbaf97d3bcf47b85117c10/Reports/Coverage_SPAdes_report.md) \| [Plasmid Coverage report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/dbe2e43aecbf186ad0d9272a0bb710274e233043/Reports/Coverage_SPAdes_plasmid_report.md) |  |
| 🟩 | 6 | QUAST + CheckM | Quality check | [MultiQC_QUAST](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST/) \| [CheckM_report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/9c0f8b651fe3bc0402f85996132c94f22af79388/Reports/CheckM_result.md)  [MultiQC_QUAST_plasmid](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST_plasmid/) \| [CheckM_plasmid_report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/4b76ed1e7a865df019c402501f47282d3407ed6b/Reports/CheckM_plasmid_report.md) |  |
| 🟦 | 7 | Geneious + scripts | Assemble plasmids on the reference + assembly data, polishing | [Plasmid Assembly General Report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/1ba135bfba33976b96557f1370a49b2518213ac9/Reports/custom_plasmid_assembly_report.md) \| [Plasmid Assembly Detailed Report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/1ba135bfba33976b96557f1370a49b2518213ac9/Reports/filtration_report.md) | |
| ⬜️ | 8 | Prokka | Annotating of the high-quality assemblies |  | Both core genome & plasmid are fine. Thinking about convenient way to represent data |
