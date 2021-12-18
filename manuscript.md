---
title: Estimating microbial (meta)pangenomes with amino acid k-mers OR Protein k-mers enable assembly-free microbial metapangenomics
keywords:
- metapangenome
- pangenome
- assembly graph
- reduced alphabet k-mer
- open reading frame
lang: en-US
date-meta: '2021-12-18'
author-meta:
- Taylor E. Reiter
- N. Tessa Pierce-Ward
- C. Titus Brown
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Estimating microbial (meta)pangenomes with amino acid k-mers OR Protein k-mers enable assembly-free microbial metapangenomics" />
  <meta name="citation_title" content="Estimating microbial (meta)pangenomes with amino acid k-mers OR Protein k-mers enable assembly-free microbial metapangenomics" />
  <meta property="og:title" content="Estimating microbial (meta)pangenomes with amino acid k-mers OR Protein k-mers enable assembly-free microbial metapangenomics" />
  <meta property="twitter:title" content="Estimating microbial (meta)pangenomes with amino acid k-mers OR Protein k-mers enable assembly-free microbial metapangenomics" />
  <meta name="dc.date" content="2021-12-18" />
  <meta name="citation_publication_date" content="2021-12-18" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Taylor E. Reiter" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0002-7388-421X" />
  <meta name="twitter:creator" content="@ReiterTaylor" />
  <meta name="citation_author" content="N. Tessa Pierce-Ward" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0002-2942-5331" />
  <meta name="twitter:creator" content="@saltyscientist" />
  <meta name="citation_author" content="C. Titus Brown" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0001-6001-2677" />
  <link rel="canonical" href="https://taylorreiter.github.io/2021-paper-metapangenomes/" />
  <meta property="og:url" content="https://taylorreiter.github.io/2021-paper-metapangenomes/" />
  <meta property="twitter:url" content="https://taylorreiter.github.io/2021-paper-metapangenomes/" />
  <meta name="citation_fulltext_html_url" content="https://taylorreiter.github.io/2021-paper-metapangenomes/" />
  <meta name="citation_pdf_url" content="https://taylorreiter.github.io/2021-paper-metapangenomes/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://taylorreiter.github.io/2021-paper-metapangenomes/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://taylorreiter.github.io/2021-paper-metapangenomes/v/ce93fccb6429817e1bd97b632391c66103e89df3/" />
  <meta name="manubot_html_url_versioned" content="https://taylorreiter.github.io/2021-paper-metapangenomes/v/ce93fccb6429817e1bd97b632391c66103e89df3/" />
  <meta name="manubot_pdf_url_versioned" content="https://taylorreiter.github.io/2021-paper-metapangenomes/v/ce93fccb6429817e1bd97b632391c66103e89df3/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://taylorreiter.github.io/2021-paper-metapangenomes/v/ce93fccb6429817e1bd97b632391c66103e89df3/))
was automatically generated
from [taylorreiter/2021-paper-metapangenomes@ce93fcc](https://github.com/taylorreiter/2021-paper-metapangenomes/tree/ce93fccb6429817e1bd97b632391c66103e89df3)
on December 18, 2021.
</em></small>

## Authors



+ **Taylor E. Reiter**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-7388-421X](https://orcid.org/0000-0002-7388-421X)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [taylorreiter](https://github.com/taylorreiter)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [ReiterTaylor](https://twitter.com/ReiterTaylor)<br>
  <small>
     Department of Population Health and Reproduction, University of California, Davis
     · Funded by Grant XXXXXXXX
  </small>

+ **N. Tessa Pierce-Ward**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-2942-5331](https://orcid.org/0000-0002-2942-5331)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [bluegenes](https://github.com/bluegenes)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [saltyscientist](https://twitter.com/saltyscientist)<br>
  <small>
     Department of Population Health and Reproduction, University of California, Davis
     · Funded by NSF 1711984
  </small>

+ **C. Titus Brown**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-6001-2677](https://orcid.org/0000-0001-6001-2677)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [ctb](https://github.com/ctb)<br>
  <small>
     Department of Population Health and Reproduction, University of California, Davis
  </small>



## Abstract {.page_break_before}




# Introduction

Short read metagenomic sequencing has expanded our knowledge of microbial communities and diversity [@doi:10.1038/nmicrobiol.2016.48; @doi:10.1038/s41587-020-0718-6; @doi:10.1038/s41579-019-0311-5].
Many of these insights are attributable to *de novo* assembly and binning, which estimate species-level composite genomes (metagenome-assembled genomes, *MAGs*) from genomes in a sample, capturing unculturable genomes which have expanded the tree of life and and our understanding of microbial metabolism in diverse environments [@doi:10.1038/nature02340; @doi:10.1038/nmicrobiol.2016.48; @doi:10.1038/s41587-020-0718-6]. 
Along with these advances, the concept of metapangenomics has arisen as a framework for understanding how sets of genes that occur in closely related MAGs correlate with parameters in the environments in which they are sampled from [@doi:10.7717/peerj.4320; @doi:10.1038/s41396-019-0516-7; @doi:10.1007/978-3-030-38281-0_9].
Like pangenome analysis of isolate genomes, metapangenomes reflect the metabolic and ecological plasticity of populations of microbes and give insights into the genes that support specific environmental adaptations [@doi:10.1038/s41396-019-0516-7].

<!-- Really trying not to shit on de novo analysis, which really has given us many great things -->
Metapangenomics is reliant on *de novo* metagenome analysis, but both assembly and binning introduce biases into analysis [@doi:10.1186/s13059-020-02066-4; @doi:10.1038/nmeth.4458; @doi:10.1101/2021.07.12.451567; @doi:10.1038/s41396-018-0081-5; @doi:10.1099/mgen.0.000436; @doi:10.1101/2021.05.04.442591].
Low coverage or large amounts of variation (SNPs, indels, rearrangements, horizontal gene transfer, sequencing error, etc.) cause assemblers to break contiguous sequences, producing short fragments or unassembled reads that are too short to be binned into MAGs (CITE).
These biases disproportionately impact genomic islands and plasmids [@doi:10.1099/mgen.0.000436], hot spots for evolution that support microbial adaptation to changing environments [@doi:10.1101/2021.03.15.435471].

To more fully represent the functional potential in metapangenomes, we present an analysis approach that relies on amino acid and reduced alphabet k-mers to accurately estimate microbial pangenomes. 
K-mers are words of length *k* in DNA or protein sequences. 
K-mer-based analysis has recently risen in popularity via sketching algorithms that sub sample sequences to facilitate rapid comparisons while maintaining similarity between samples [@doi:10.1186/s13059-019-1809-x]. 
In particular, long nucleotide k-mers preserve similarities between closely related genomes but are brittle to evolutionary distance [@doi:10.1128/mSystems.00020-16] (CITE: Tessa). 
By using amino acid k-mers and other reduced alphabets, sequence similarities are preserved across larger evolutionary distances.
Combining this approach with accurate open reading frame prediction from short read sequences, this method can be applied without assembly.

# Results

We demonstrate ... / summarize results or something here

![
**Organisms used in this paper**
](images/tree_fig.png "tree fig"){#fig:tree_fig}

## Reduced alphabet k-mers accurately estimate microbial pangenomes

To determine whether pangenomes could be constructed using amino acid or other reduced alphabet k-mers, we constructed pangenomes from amino acid (k = 7, 8, 9, 10, 11), dayhoff (k = 13, 15, 17), and the hydrophobic-polar (k = 27, 31) encodings and compared these against pangenomes constructed from genes using roary. 
We constructed pangenomes for 23 species from 23 phyla in the GTDB taxonomy, ranging from 20 to 972 genomes per pangenome (average = 203).
For each pangenome, we compared the total number of genes and k-mers and the total number of unique genes and k-mers for each genome. 
We also tested whether genomes that had similar gene presence-absence profiles had similar k-mer presence-absence profiles using the Mantel test.
Performance varied minimally across encodings (**Figure @fig:violin_fig**) thus we performed the majority of our analyses using amino acid encodings with a k-mer size of 10.

+ @Tessa: Do we need to justify selecting a k-mer size of 10 here?
+ @Tessa: Do I need to show a comparison to a scaled of 1 here? I have it for 12 of the species, and the numbers are similar enough to scaled 100 that I stopped wasting the compute on scaled 1
+ @Tessa: should I compare this against nucleotide k-mers at all? Bc I think that's the underlying assumption here, nucleotides don't work for this stuff.

![
**K-size and alphabet do not impact pangenome estimation with k-mers.** Violin plots represent the distribution of R2 values for linear models (Total, Unique) or statistic values for mantel tests (Mantel). *Total* corresponds to correlation between total number of distinct genes and distinct k-mers in a genome. *Unique* corresponds to correlation between the number of unique genes and unique k-mers in genome. *Mantel* corresponds to a mantel test between the gene and k-mer presence-absence matrices.
](images/violin_fig.png){#fig:violin_fig}

Performance across metrics varied dramatically for different pangenomes, with k-mers and genes highly correlated for some pangenomes and not correlated for others (**Figure @fig:violin_fig**) . 
We investigated pangenomes more closely to determine the source of the poor correlations and found that they were caused by the presence of many frameshifted proteins, one of many potential criteria for exclusion of GenBank genomes from RefSeq.
For example, *Leptospira interrogans* had an R^2^ of 0.12 between the total number of genes and k-mers in genomes in the pangenome, however 21 genomes contained frameshifted proteins. 
Removing these genomes increased the R^2^ to 0.87 (**Figure @fig:frameshift_fig A,B**).
This trend was consistent across pangenomes, where pangenomes that had at least one genome that was excluded from RefSeq for having many frameshifted proteins had a significantly lower R^2^ values between total number of genes and total number of k-mers per genome than pangenomes that did not (Welch Two Sample t-test, estimate = -0.36, p = 0.003) (**Figure @fig:frameshift_fig C**).
Other RefSeq exclusion criteria did not impact the correlation between the total genes and k-mers per genome for a given pangenome.

![
**Genomes that are excluded from RefSeq for having many frameshifted proteins reduce similarity between gene- and k-mer-based pangenomes.**
**A, B)** Scatter plots of the total number of distinct genes and k-mers per genome for the species *Leptospira interrogans*, where each point represents a single genome in the pangenome. 
Removing genomes flagged with RefSeq exclusion criteria "many frameshifted proteins" improves the correlation between these variables. 
**C)** Box plot of R^2^ values between the total number of distinct genes and k-mers per genome. 
Pangenomes that contain genomes with the RefSeq exclusion criteria of "many frameshifted proteins" have significantly lower R^2^ values
](images/frameshift_fig.png){#fig:frameshift_fig}

We next investigated whether other pangenome metrics were well correlated between k-mer-based and gene-based methods using pangenomes that did not contain genomes excluded from RefSeq for having many frameshifted proteins.
For these 13 pangenomes, the percent of k-mers or genes predicted to be part of the core, shell, or cloud genome was strongly correlated (**Figure @fig:pg_fig**).
We also compared whether pangenomes would be designated as open or closed by calculating the alpha value for the Heaps law model. 
Alpha values were strongly correlated between gene- and k-mer based pangenomes (**Figure @fig:pg_fig**). 

![
**Pangenome metrics strongly correlate between gene- and k-mer-based pangenomes.** Pangenome categories core, shell, and cloud refer to genes or k-mers shared between the majority (>95%), some, or singleton genomes in the pangenome. \Alpha is a value from Heaps law used to estimate whether a pangenome is open or closed.
](images/pg_fig.png){#fig:pg_fig height=2.5in}

## Jaccard containment between reduced alphabet k-mers and k-mers in databases accurately predicts open reading frames in short sequencing reads

Given that protein k-mers can accurately estimate bacterial and archaeal pangenomes, we next sought to determine whether open reading frames could be accurately predicted directly from short sequencing reads, as this would enable pangenome analysis without assembly.
We evaluated whether orpheum, a tool recently developed to predict open reading frames in Eukaryotic short reads [@doi:10.1101/2021.07.09.450799], could also perform this task in bacterial and archaeal sequences.
Orpheum predicts open reading frames by comparing reduced alphabet k-mers in six frame translations of short sequencing reads against those in a database (jaccard containment) and assigns an open reading frame as coding if containment exceeds a user-defined threshold [@doi:10.1101/2021.07.09.450799].
To evaluate orpheum, we constructed a database containing all k-mers in coding domain sequences from genomes in GTDB rs202.
Using representative genomes from the 23 species above, as well as 20 additional genomes not in the GTDB rs202 database, we simulated short sequencing reads either from coding domain sequences or non-coding sequences and used these reads to test orpheum.

Using default parameters, orpheum accurately separated coding from non-coding reads when reads were simulated from genomes in GTDB (**Figure @fig:orpheum_fig A**).
For reads simulated from genomes not in GTDB, orpheum recovered the majority of coding reads when genomes of the same species were in the database (**Figure @fig:orpheum_fig A,B**).
Accuracy decreased with increasing taxonomic distance between the query genome and the closest relative in the database (**Figure @fig:orpheum_fig B**).

For genomes that had at least species-level representatives in GTDB, the largest source of error was non-coding reads being predicted as coding (**Figure @fig:orpheum_fig A**).
We hypothesized that these reads originated from pseudogenes as these sequences would likely not be annotated as coding in the genomes from which the reads were simulated from, but may retain some k-mers contained in the database.
To assess this hypothesis, we used annotation files produced by the NCBI Prokaryotic Genome Annotation Pipeline (PGAP), which annotates pseudogenes, for the 23 genomes for which these files were available [@doi:10.1093/nar/gkw569; @doi:10.1093/nar/gkaa1105].
On average, 12.4% (SD = 13.8%) of non-coding reads that were predicted to be coding fell within pseudogenes annotated by the PGAP pipeline.
We then BLASTed a subset of the remaining non-coding read that were predicted to be coding against the NCBI nr database.
All reads we investigated had at least one mach at 100% identity to protein sequences in the database, suggesting our test genomes contained additional pseudogenes not annotated by PGAP, or that the software we used to predict open reading frames missed some coding sequences (see Methods).
<!--Indeed, the worst performer was *Mycoplasmopsis bovis*, with 23% of non-coding reads predicted to be coding. 
*M. bovis* causes bovine tuberculosis and its genome contains signatures of genomic decay and pseudogenization [@doi:10.3389/fmicb.2017.02389], processes that may be linked to bacterial host specialization [@doi:10.1101/cshperspect.a010041; @doi:10.1093/gbe/evv135].-->
Because this method of open reading frame prediction cannot distinguish pseudogenes, it may not be appropriate for species with many pseudogenes.

+ Why coding as noncoding? sequencing error?

Protein k-mers from predicted open reading frames in the simulated short sequencing reads recapitulated similarity between genomes estimated from coding domain sequences in those genomes.
We estimated the jaccard similarity between genomes using protein k-mers (*k* = 10) from annotated coding domain sequences, and compared this against jaccard similarity between genomes using protein k-mers from predicted open read frames in the simulated short sequencing reads.
Genomes that were most similar in one matrix were also most similar in another matrix (Mantel statistic = 0.9975, p < 0.001). 
The average similarity among all pairwise comparisons for the coding domain sequences was 2.6%, and this decreased to 2.5% when using the open reading frames predicted from reads.
This demonstrates that information recovered from open reading frame prediction from short read is similar to that derived directly from the genome sequence.

The majority of predictive capability originated from species-level databases.
We performed ORF prediction using just species-level databases for genomes that had at least a species-level representative in GTDB, and compared this against ORF prediction using the full GTDB database. 
On average, there was no change between the percent of reads derived from coding domain sequences when a species-level database was used versus when all of GTDB was used to predict open reading frames (**Figure @fig:orpheum_db**).

Decreasing the jaccard containment threshold increased the sensitivity and specificity of ORF prediction when there are no closely related genomes in the database (**Figure @fig:orpheum_fig C, Table @tbl:threshold**).
The jaccard containment threshold controls the final prediction of coding vs. non-coding, as well as the the number of open reading frames which a read is translated into.
We suggest the results in **Table @tbl:threshold** be used as a guide for setting the jaccard threshold based on the taxonomy of the organism relative to the organisms in the database.


|jaccard threshold | closest rank | mean sensitivity| mean specificity | mean Youden's index |
|:-------------:|:------------:|:--------------:|:--------------:|:------------:|
|          0.47 | genome       |          0.988 |           0.971|       0.959|
|          0.39 | species      |          0.941 |           0.961|       0.902|
|          0.17 | genus        |          0.790 |           0.862|       0.653|
|          0.07 | family       |          0.593 |           0.878|       0.471|
Table: Jaccard containment thresholds that maximize the Youden's index depending on the taxonomic rank of the closest relative in GTDB.
{#tbl:threshold}


![
**Orpheum correctly assigned short sequencing reads as coding or non-coding and selects the correct open reading frame.**
**A)** Percent of simulated coding or non-coding sequences predicted as coding, non-coding, or discarded based on quality metrics (see methods). 
Genomes are split by those in GTDB and those not in GTDB.
Genomes not in GTDB are labelled by taxonomic assignment from GTDB-tk.
Predictions were made using default parameters (jaccard containment = 0.5).
**B)** Boxplots of the percent of coding reads that were recovered by Orpheum, separated by the level of taxonomic assignment achieved by GTDB-Tk. 
Orpheum recovers more coding sequences when there are closely related genomes in the database. 
**C)** Receiver operating curves for the jaccard containment thresholds. 
Curves are separated by the level of taxonomic assignment achieved by GTDB-Tk, and values are averaged across all genomes that fell within those categories.
The best jaccard threshold decreases when there are fewer closely related genomes in the database.
**D)** Databases constructed of only closely-related genomes recover the majority of coding sequences, but including increasingly distantly related genomes improves total coding recall. 
](images/orpheum_fig.png){#fig:orpheum_fig}

**LEFTOVERS**

+ k-mer size, alphabet selection
  + we don't have any evidence for this yet with these data sets.
+ Should/do I have to compare these results against FragGeneScan?

## K-mer-based metapangenomics combined with assembly graphs ... 

Given that amino acid k-mers accurately estimated pangenomes, and that the correct open reading frame could be predicted from short sequencing reads, we next combined these approaches to perform metapangenome analysis from short read shotgun metagenomes.
We used 12 metagenomes from a single individual that were sampled over the course of a year by the Integrated Human Microbiome Project (iHMP) [@doi:10.1038/s41586-019-1238-8]. 
The individual was diagnosed with Crohn's disease, a sub type of inflammatory bowel disease characterized by inflammation along the gastrointestinal tract. 
The individual received three courses of antibiotics over the year and each course was separated by weeks without antibiotics (**Figure @fig:metag_species**).

![
](images/common_species_breakdown.png){#fig:metag_species height=2.5in}

We estimated the metapangenome for each species that was detected in all 12 metagenomes and that accounted for at least 10% of reads across metagenomes, for a total of nine metapangenomes (**Figure @fig:metag_species**).
To obtain all sequencing reads that originated from genomes of these species, we performed assembly graph genome queries [@doi:10.1186/s13059-020-02066-4].
Assembly graphs contain all sequences in a metagenome, and assembly graph queries return sequences in the metagenome that are either in the query or nearby to the query in the graph.
Assembly graph genome queries return sequencing reads that originate from genomes in the metagenome that have as little as 0.1 jaccard similarity (approximately 93% average nucleotide identity (ANI) (CITE: TESSA)) to the query genome [@doi:10.1186/s13059-020-02066-4].
After retrieving reads in this way, we predicted open reading frames using orpheum. 
We used species-level databases as these were successful in the context of isolate genomes not in the database (see above) and because they would be more likely to filter out reads beyond the species boundary (95% ANI [@doi:10.1038/s41467-018-07641-9]) but returned by assembly graph queries.
Using the predicted amino acid sequences, we built metapangenomes for each of the nine species (FIGURE).

Unlike isolate genomes, metagenomes may contain a fraction of an organisms genome if the metagenome was not sequenced deeply or if an organism was rare. 
To calculate the core, shell, and cloud fractions and to estimate the alpha of the metapangenome, we thresholded the number of k-mer, removing samples with fewer k-mers than two standard deviations below the mean (CHECK).
XXXX

Using our metapangenome approach, we identified interesting patterns in accessory gene presence associated with antibiotic exposure (FIGURE).
For example, the *Phocaeicola vulgatus* metapangenome is stable for the first 11 weeks of sampling even during ciprofloxacin administration,
but a portion of the accessory genome corresponding to XX% of the total metapangenome disappears at week 13, coinciding metronidazole administration.
While a portion of the *Parabacteroides merdae* metapangenome is present in early samples, the full genome is only detected after metronidazole administration when the fractional abundance of *P. merdae* increases starting at week 13.
However, additional accessory elements are detected beginning at week 19, which coincides with a bloom of *P. merdae*. 

In two bacterial species antibiotic administration appears to spur on strain switching for some species.
In *Bacteroides uniformis*, one set of accessory elements present from weeks 0 - 11 is replaced by a new set in weeks 25-36.
Similarly, in *Parabacteroides distasonis* accessory elements present in weeks 4, 9, and 11 are replaced by new accessory elements in weeks 25-36. 
Both switches occur during metronidazole administration after the bloom of *P. merdae* and *P. vulgatus*.


+ Do I need to compare these results against typical metapangenomics? like do de novo assembly, binning, prokka? etc?

## Extra results that don't really fit in the paper, but I could force them to fit or we could put them in a different paper

Lastly, we investigated whether the relationship between the number of k-mers in coding domain sequences in a genome and the number of genes in a genome was constant across diverse phyla represented here. (**Figure @fig:all_pw_fig**)

![
**The ratio of total distinct genes per genome to total distinct k-mers per genome is conserved across distantly related species.** 
Each point represents a single genome, and genomes are colored by species.
](images/all_pw_fig.png){#fig:all_pw_fig}


# Discussion

We present a method to perform assembly-free metapangenomics.
We show that pangenome metrics like estimate of core, cloud, and shell pangenome fractions can be accurately estimated with long amino acid k-mers and k-mers from other reduced alphabets.
We then demonstrate accurate prediction of open reading frames in highly accurate short sequencing reads by comparing amino acid k-mers in all translation frames against a database of k-mers from all known bacterial and archaeal genomes in GTDB (rs202).
Combining these tools enables pangenome estimation directly from quality controlled short sequencing reads.
In the context of metagenomes, these approaches enable metapangenome estimation without the need to *de novo* assemble and bin sequences, eliminating common sources of lost sequencing variation (cite spacegraphcats).

The combination of these approaches is potentially most useful in the context of analyzing metagenome assembly graphs.
Assembly graphs like compact de Bruijn graphs (cDBG) capture all sequences in a metagenome, including sequences with high strain variation or low coverage, which may not be captured by other analysis methods. 
A targeted query of an assembly graph, for example with a metagenome-assembled genome bin, can recover all sequencing reads in a metagenome that originate from all genomes of the same species (cite spacegraphcats). 
While recovering these reads and assigning their taxonomic identity through graph queries is useful, many of the recovered reads cannot be assembled due to prolific sequencing variation attributable to strain diversity in the original microbial community.
Yet, the sequences represented by these un-assembleable reads often encode functional potential, some of which may be key to a microorganisms functioning within its ecosystem (cite sumner paper?; metachercant).
The approaches presented in this paper enable these sequences to be represented in metapangenome estimation.

Long read sequencing of microbial communities stands to improve many of these challenges, particularly as lineage-resolved methods become mainstream (cite bickhart et al.).
Even as long read technologies improve, short read sequences continue to better capture strain diversity from a community (Cite Maureen?). 
Even with long read references from the same community, many of these short reads do not map and do not assemble (cite Maureen). 
The approaches presented here will allow these sequences to be included in pangenome estimation.

Practically, open reading frame prediction with orpheum can be executed on microbial illumina short read data sets.
<!-- Generalize? Include citation to olga paper here? -->
The RAM used to run orpheum is dictated by the database size, as the database is loaded into to memory while its running.
The GTDB rs202 nodegraph was 94 GB, and the RAM required to run orpheum never exceed 97GB, which makes database distribution and orpheum execution available on high performance compute clusters and other remote computers.
To reduce ram, this data structure could be improved XXX. 
<!-- Titus/Tessa? -->

We demonstrated that orpheum is better able to predict open reading frames in genomes that have species-level representatives in the GTDB database. 
To asses whether this criteria is satisfied by a query genome without performing genome assembly, we recommend sourmash gather. Sourmash gather will estimate the fraction of sequencing reads in a genome or metagenome that match to a genome in GTDB by comparing long nucleotide k-mers in the query against those in the database (cite gather paper).
Alternatively, the tool SingleM could be used to perform this task. 
SingleM estimates the taxonomic composition of sequencing reads by identifying fragments of single copy marker genes in short reads and comparing them against a database of taxonomically labelled sequences.

While it is necessary for the database to have a species-level representative for orpheum to achieve high ORF recall for a given query, it is not sufficient.
This likely reflects similarity in core genomes for closely related organisms, but prolific horizontal gene transfer between both closely and distantly related organisms.
Including genomes from increasingly distant taxonomic ranks in the database added XX additional true positives. 

<!-- Interestingly, while shared k-mer content between distantly related genomes improves ORF prediction, using reduced alphabets did not improve ORF recall. -->
<!-- We only did this for panmers, not orpheum...so for. Could show e.g. within phlya or some small db.  -->

Comparison between euks? Need to read orpheum paper.

PANMER discussion

+ sourmash signature generation is rapid.
+ Exact matching scales (linearly?). May enable running on very large collections of genomes.
+ Exact matching of k-mers enables additions of new species without having to rerun everything.
+ Exact matching also allows direct comparisons to distantly related organisms. Unified framework for genome comparisons even when organisms are distantly related.
+ scaled is handy parameter to potentially enable even larger comparisons
+ sacrifice function -- annotating k-mers with function is good future work. 

### Other points

+ While the number of genes per genome is increased for genomes with this exclusion criteria, there is no commiserate increase in the number of k-mers observed. 
This suggests that the number of k-mers in a genome could be used to predict the expected range of predicted genes in a genome, and could be potentially used a quality control metric for annotated genomes.
+ While developed for the metapangenomics space, this study demonstrates that k-mer-based pangenomes will also work in isolate genomes. Given that building k-mer sketches and exact matching of k-mers between genomes is fast, this provides an alternative approach for building pangenomes. 
+ De novo metagenome analysis probably dramatically improves ORF prediction because of the inclusion of these genomes in GTDB.


# Methods 

<!-- Can I pretty plz keep these separate or do they need to be combined? -->
All code is available at github.com/taylorreiter/2021-panmers (results section 1), github.com/taylorreiter/2021-orpheum-sim (results section 2), and https://github.com/taylorreiter/2021-metapangenome-example (results section 3).

### Selection of benchmarking species for pangenome analysis
We selected a species representative for each of the 23 phyla in GTDB rs202. 
To select representative species, we first filtered species with fewer than 20 representatives and greater than 1000 representatives.
While this approach scales beyond 1000 genomes, we elected to benchmark smaller sets to iterate over the potential parameter space more quickly.
Of species remaining after filtering, we selected the species within each phyla that had the largest number of genomes.
We downloaded these genomes from GenBank.
Species names are in table XXX.

### Calculating the gene-based pangenome with roary 
To calculate the gene-based pangenome, we first annotated each genome using prokka with the `--metagenome` flag.
We then used the resulting GFF annotations files to calculate the pangenome with roary using default settings.

### Calculating the k-mer based pangenome with sourmash 
To calculate k-mer based pangenomes, we used sourmash `sketch` to generate signatures from the prokka-predicted amino acid sequences (`.faa` files). 
We used the protein alphabet (k = 7, 8, 9, 10, 11), dayhoff alphabet (k = 13, 15, 17), and the hydrophobic-polar alphabet (k = 27, 31). 
All signatures were calculated with a scaled value of 100.
The scaled parameter controls the fraction of the total k-mers represented by the sketch; a scaled value of 100 indicates that 1/100th of the distinct k-mers in a genome were included in each sketch.
We converted signatures from json format into a genome x hash presence-absence matrix.

### Correlating gene-based and k-mer based pangenomes 
Using the presence-absence matrices for the gene-based and k-mer-based pangenomes, we correlated total genes/k-mers observed per genome and total unique genes/k-mers observed per genome for each species.
We used the `rowSums()` function in R to determine the number of genes/unique genes per matrix, then used the `lm()` function with default parameters to correlate the values.
We also used the Mantel test to determine whether genomes that were most similar in the gene presence-absence matrix were also most similar in the k-mer presence-absence matrix. 
We used the `mantel()` function in the R vegan package to perform this test. 
We used distance matrices calculated with the `dist()` function using the parameter `method = "binary"` as input to the mantel test.

### Generating standard pangenome metrics with pagoo 
The pagoo R package provides functions to analyze bacterial pangenomes.
We used this package to generate standard pangenome metrics and visualizations.
These metrics are based on the presence-absence matrices generated above and include calculation of the core, shell, and cloud genome sizes and estimation of the alpha value in Heaps law for estimation of pangenome openness.

### Augmenting benchmarking species set to include genomes not in GTDB for open reading frame prediction
We next generated a benchmarking data set for open reading frame prediction. 
We selected a genome from each of the 23 species evaluated above, choosing the GTDB rs202 representative genome for each species.
Given that open reading frame prediction relies on a database, and we used k-mers in GTDB rs202 to generate this database, we also wanted to select genomes that were not in GTDB to evaluate this method.
We determined the bacterial and archaeal genomes that were added to RefSeq after the construction of GTDB rs202 (April 2021-November 2021).
From this set, we selected a representative genome from each of the distinct NCBI phyla represented among these genomes, 20 in total.
Genome accessions are recorded in Table XXX.
We then ran GTDB-tk on these genomes to predict the GTDB taxonomy of each.

### Simulating coding domain sequence and non coding domain sequence reads with polyester
We next created a labelled data set of simulated reads that were generated from either coding domain sequences (CDS) or non-coding regions within each genome.
We annotated the genomes with bakta to produce CDS ranges, and used polyester to simulate reads from CDS or non-coding regions. 
We used the default short read error profile within polyester.

### Determing short read open reading frames with orpheum 
We used the orpheum tool to predict open reading frames from simulated short reads.
Orpheum was developed to predict open reading frames in short RNA-seq reads from Eukaryotic organisms without a reference genome or transcriptome sequence.
Orpheum perform six-frame translation on nucleotide sequencing reads, calculates k-mers in an amino acid, dayhoff, or hydrophobic-polar encoding at the designated k-mer length, and then estimates the jaccard similarity between k-mers in each translation frame and a database. 
It then selects all open reading frames based on a jaccard similarity threshold, and returns those reads as translated amino acid sequences.
Open reading frames are excluded if they contain stop codons, low complexity sequences, or if the read is too short to perform translation.
Reads are designated as non-coding if they don't reach the jaccard similarity threshold and are not excluded for other reasons.
<!-- Is it jaccard similarity? It's whichever one makes sense and I always get them confused -->

We constructed a database from GTDB rs202 using sourmash XXX and using a k-mer size of 10.
+ @Tessa any relevant details would be very helpful :) 


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>



![The slight increase observable for some species is a results in different thresholds, where we used 0.39 for the species database and 0.5 for the GTDB rs202 database.
](images/orpheum_supp1.png){#fig:orpheum_db height=3in}