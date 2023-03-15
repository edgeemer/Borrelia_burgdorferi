
<h3 align="center">Current pipleine</h3>
  
|State|Step|Software|Brief description| Report |
|:--:|:--:|:--:|:--:|:--:|
| 🟩 | 1 | FastQC | Quality check | [MultiQC_init](https://edgeemer.github.io/B_burgdorferi_MuliQC_init/) |
| 🟩 | 2 | FastP | Polishing raw reads (len and coverage) |  |
| 🟩 | 3 | FastQC | Quality Check | [MultiQC_trimmed](https://edgeemer.github.io/B_burgdorferi_MultiQC_trimmed/) |
| 🟩 | 4 | SPAdes | Reads -> scaffolds |  |
| 🟩 | 5 | custom script | Polishing scaffolds (len and coverage) |  |
| 🟨 | 6 | QUAST + CheckM | Quality check | [MultiQC_QUAST](https://edgeemer.github.io/B_burgdorferi_MultiQC_QUAST/) \| [MultiQC_QUAST_ref_test](https://edgeemer.github.io/B_burgdorferi_QUAST_ref_test/) |
| 🟩 | 7 | bowtie-build | create basenames |  |
| 🟩 | 8 | Bowtie2 | Mapping raw reads |  |
| ⬜️ | 9 | samtools | SAM file to BAM |  |
| ⬜️ | 10 | samtools | Sort and index the BAM file |  |
| ⬜️ | 11 | bedtools | Convert the assembly to BED format |  |
| ⬜️ | 12 | bedtools | Calculate coverage |  |
| ⬜️ | 13 | IGV | Visualize coverage |  |
| ⬜️ | 14 | Racoon | Polishing assembly |  |
| ⬜️ | 15 | IGV | Visualize coverage |  |


# Borrelia_burgdorferi
The project is funded by Genome Atlantic to study the diversity of Lyme disease-causing spirochaete bacteria (genus/species = Borrelia burgdorferi)  in Nova Scotian ticks and in patient biopsies. The project has taken a LOT longer than expected, mainly due to the pandemic. It has taken years for us to even get samples. 

• Our role in the project was to provide support for genomics and bioinformatics. We were to be given DNA from natural samples and from cultured Borrelia spp. for the purposes of de novo genome sequencing and assembly (originally slated to be nanopore, but DNA yield is a big problem). 

• We recently (finally) received some samples that could be sequenced and submitted them to the IMR — Marlena, please indicate how many different samples, and the nature of the sequencing data collected.

-My thought process at this stage: 
(a) Dima is going to be having the IMR sequence the genomes of some of his Paramoeba-associated bacteria, and will thus need to learn how to process / assemble the genomic data.
(b) Xi has extensive experience in bacterial genome assembly, prior to joining my lab, and also from his current work assembling and analyzing >700 E. coli genomes!
(c) We have just had a bunch of Illumina sequence data arrive for Borrelia samples
(d) My hope was that Xi could advise Dima on the initial steps in the data processing and assembly phase — Dima is a quick learner, and thus will soon be able to carry out the steps independently! 

Attached is a presentation Bruce gave some years ago summarizing what is known about Borrelia genomes. One interesting thing is Borrelia spp. have multiple chromosomes and plasmids. So the assembly process will be more complex than would normally be the case. 
