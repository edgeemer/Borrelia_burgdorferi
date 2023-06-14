<h2 align="center">Contents</h2>

- <a href="#Core Genome Assembly">Core Genome Assembly</a>
- <a href="#Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</a>

---

<h3 align="center" id="Core Genome Assembly">Core Genome Assembly</h3>

|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | ─ | FastQC         | Initial Quality check                               | [MultiQC_Init](Reports/B_burgdorferi_MultiQC_init.html) |  |
| 🟩 | 1 | FastP          | Filtering and trimming raw reads (len and coverage) |  | -> <a href="#Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</a>|
| 🟩 | └ | FastQC         | Trimmed Reads Quality Check                         | [MultiQC_Trimmed](Reports/B_burgdorferi_MultiQC_trimmed.html) |  |
| 🟩 | 2 | SPAdes         | Assembly                                            |  |  |
| 🟩 | 3 | custom script  | Filtering scaffolds (len and coverage)              | [Coverage Report](Reports/whole_genome/3.0.coverage_SPAdes_wh_report.md) | -> <a href="#Core Genome Assembly">Core Genome Assembly</a> |
| 🟩 | 4 | Geneious    | Extracting main chromosomes (core genomes)             |                      | Main chromosome is present ✅ |
| 🟩 | 5 | Prokka      | Annotating of the high-quality assemblies              | Project drive folder |  |
| 🟦 | 6 | parsnp_tree | Comparing isolates                                     |                      | gingr for visualization (File -> open -> tree file \| Export file as .vsf \| Compare non-synonymus changes to actual positions per gene |
| ⬜️ | 7 | cgmlst      |                                                        |                      | MLST |

COG analysis | KEGG pathway

---

<h3 align="center" id="Plasmid on the Reference Genome Assembly">Plasmid on the Reference Genome Assembly</h3>

Branch from S1 <a href="#Core Genome Assembly">Core Genome Assembly</a>

|State|Step|Software|Step description| Report | Notes |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 2 | SPAdes               | Assembly                                                      |  |  |
| 🟩 | 3 | custom script        | Filtering scaffolds (len and coverage)                        | [Plasmid Coverage Report](Reports/plasmid/3.0.custom-trim-from-spades-pl-S2.md) |  |
| 🟩 | 4 | Geneious             | Map sequences with minimap2 to reference plasmids             |  |  |
| 🟩 | 5 | custom script        | Filter consensus sequences (75+ coverage to reference)        | [Plasmid Filtration Report](Reports/plasmid/5.0.minimap_to_reference_plasmids_geneious_filtered-pl-S5.md) | Step is not relevant => will be removed with update |
| 🟩 | 6 | Geneious             | Map raw reads with bowtie2 to filtered plasmids               |  |  |
| 🟩 | 7 | custom script        | Using consensus from the step 6 improve step 4 assemblies     | [Borrelia Burgdorferi plasmid presence](https://docs.google.com/spreadsheets/d/1qOfwAWgnmrz81K9PqESubi8MufjOqxDshoJY8hGCvTg/edit?usp=sharing) |  |
| 🟦 | 8 | Polishing sequebces  | Using blastn to heal ambigious nucleotides (IUPAC)            |  |  |
| ⬜️ | 9 | Prokka               | Annotating of the high-quality assemblies                     |  |  |
