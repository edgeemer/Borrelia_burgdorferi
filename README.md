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
| 🟩 | 3 | [NCBI_assembly_filter_mod.py](https://github.com/edgeemer/genome-assembly/blob/0320ef527e1031f0302d8fa471001ec75017e4f7/Scripts/assembly_length_and_coverage_filtration/NCBI_assembly_filter_mod.py#L5)  | Filtering scaffolds (len and coverage)              | [Coverage Report](Reports/whole_genome/3.0.coverage_SPAdes_wh_report.md) | -> <a href="#Core Genome Assembly">Core Genome Assembly</a> |
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
| 🟩 | 3 | [NCBI_assembly_filter_mod.py](https://github.com/edgeemer/genome-assembly/blob/0320ef527e1031f0302d8fa471001ec75017e4f7/Scripts/assembly_length_and_coverage_filtration/NCBI_assembly_filter_mod.py#L5)        | Filtering scaffolds (len and coverage)                        | [Plasmid Coverage Report](Reports/plasmid/3.0.custom-trim-from-spades-pl-S2.md) |  |
| 🟩 | 4 | Geneious             | Map assemblies with minimap2 to ref plasmids                  |  |  |
| 🟩 | 5 | Geneious             | Map raw reads with bbmap to filtered plasmids                 |  |  |
| 🟩 | 6 | [consensus_generator.py](https://github.com/edgeemer/genome-assembly/blob/0320ef527e1031f0302d8fa471001ec75017e4f7/Scripts/consensus_generator/consensus_generator.py)        | Using consensus from the step 5 improve step 4 assemblies     | [Borrelia Burgdorferi plasmid presence](https://docs.google.com/spreadsheets/d/1qOfwAWgnmrz81K9PqESubi8MufjOqxDshoJY8hGCvTg/edit?usp=sharing) \| [consensus_generator_report](Reports/plasmid/consensus_generator_report.md)|  |
| 🟦 | 7 | Polishing sequebces  | Using blastn to heal ambigious nucleotides (IUPAC)            |  |  |
| ⬜️ | 8 | Prokka               | Annotating of the high-quality assemblies                     |  |  |
