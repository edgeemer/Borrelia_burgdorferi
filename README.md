<h2 align="center">Contents</h2>

- <a href="#Whole Genome Assembly">Whole Genome Assembly</a>
- <a href="#Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</a>

---

<h3 align="center" id="Whole Genome Assembly">Whole Genome Assembly</h3>

|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Initial Quality check | [MultiQC_init](Reports/B_burgdorferi_MuliQC_init.html) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Step 2 Quality Check | [MultiQC_trimmed](Reports/B_burgdorferi_MultiQC_trimmed.html) |  |
| 🟩 | 4 | SPAdes | Assembly |  | According to the first attempt it is not possible to normally assemble core genome. It is neeeded to be redone with different parameters |
| 🟩 | 5 | custom script | Filtering scaffolds (len and coverage) | [Coverage report](Reports/Coverage_SPAdes_wh_report.md) |  |
| 🟦 | 6 | QUAST + CheckM | Quality check |  |  |
| ⬜️ | 7 | Prokka | Annotating of the high-quality assemblies |  |  |
| ⬜️ | 8 | parsnp_tree | Comparing isolates |  | gingr for visualization (File -> open -> tree file \| Export file as .vsf \| Compare non-synonymus changes to actual positions per gene |
| ⬜️ | 9 | cgmlst |  |  | MLST |

COG analysis | KEGG pathway

---

<h3 align="center" id="Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</h3>

|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Initial Quality check | [MultiQC_init](Reports/B_burgdorferi_MuliQC_init.html) |  |
| 🟩 | 2 | FastP | Filtering and trimming raw reads (len and coverage) |  |  |
| 🟩 | 3 | FastQC | Step 2 Quality Check | [MultiQC_trimmed](Reports/B_burgdorferi_MultiQC_trimmed.html) |  |
| 🟩 | 4 | SPAdes | Assembly |  |  |
| 🟩 | 5 | custom script | Filtering scaffolds (len and coverage) | [Plasmid Coverage report](Reports/Coverage_SPAdes_plasmid_report.md) |  |
| 🟩 | 6 | QUAST + CheckM | Quality check | [MultiQC QUAST plasmid report](Reports/B_burgdorferi_MultiQC_QUAST_plasmid.html) \| [CheckM plasmid report](Reports/CheckM_plasmid_report.md) |  |
| 🟩 | 7 | Geneious + scripts | Assemble plasmids on the reference + assembly data, polishing | [Plasmid Assembly General Report](Reports/custom_plasmid_assembly_report.md) \| [Plasmid Assembly Detailed Report](Reports/filtration_report.md) | |
| 🟦 | 8 | IUPAC codes analysis | Using blastn to heal ambigious nucleotides |  |  |
| ⬜️ | 9 | Prokka | Annotating of the high-quality assemblies |  |  |
