<h2 align="center">Contents</h2>

- <a href="#Whole Genome Assembly">Whole Genome Assembly</a>
- <a href="#Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</a>

---

<h3 align="center" id="Whole Genome Assembly">Whole Genome Assembly</h3>

|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Initial Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Step 2 Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |  |
| 🟦 | 4 | SPAdes | Assembly |  | According to the first attempt it is not possible to normally assemble core genome. It is neeeded to be redone with different parameters |
| ⬜️ | 5 | custom script | Filtering scaffolds (len and coverage) |  |  |
| ⬜️ | 6 | QUAST + CheckM | Quality check |  |  |
| ⬜️ | 7 | IUPAC codes analysis | Using blastn to heal ambigious nucleotides |  |  |
| ⬜️ | 8 | Prokka | Annotating of the high-quality assemblies |  |  |
| ⬜️ | 9 | parsnp_tree | Comparing isolates |  | gingr for visualization (File -> open -> tree file \| Export file as .vsf \| Compare non-synonymus changes to actual positions per gene |
| ⬜️ | 10 | cgmlst |  |  | MLST |

COG analysis | KEGG pathway

---

<h3 align="center" id="Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</h3>

|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Initial Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Step 2 Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |  |
| 🟩 | 4 | SPAdes | Assembly |  |  |
| 🟩 | 5 | custom script | Filtering scaffolds (len and coverage) | [Plasmid Coverage report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/dbe2e43aecbf186ad0d9272a0bb710274e233043/Reports/Coverage_SPAdes_plasmid_report.md) |  |
| 🟩 | 6 | QUAST + CheckM | Quality check | [MultiQC QUAST plasmid report](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST_plasmid/) \| [CheckM plasmid report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/4b76ed1e7a865df019c402501f47282d3407ed6b/Reports/CheckM_plasmid_report.md) |  |
| 🟩 | 7 | Geneious + scripts | Assemble plasmids on the reference + assembly data, polishing | [Plasmid Assembly General Report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/1ba135bfba33976b96557f1370a49b2518213ac9/Reports/custom_plasmid_assembly_report.md) \| [Plasmid Assembly Detailed Report](https://github.com/edgeemer/Borrelia_burgdorferi/blob/1ba135bfba33976b96557f1370a49b2518213ac9/Reports/filtration_report.md) | |
| 🟦 | 8 | IUPAC codes analysis | Using blastn to heal ambigious nucleotides |  |  |
| ⬜️ | 9 | Prokka | Annotating of the high-quality assemblies |  |  |
