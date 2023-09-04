## 8/23 paper read

ngs (including genomics, metagenomics, transcriptomics) tells us about biological processes and how they are getting regulated. it tells us what living organisms are in the system which we can label using various libraries and do functional annotation on. you can do this on dna or rna

nucleic acid modifications - when a big section of rna or dna has been modified so one nucleotide replaces another, possibly changing what gets transcribed and the new function of the cell.

people have combined sequencing w a bunch of stuff to enrich for and identify covalent modifications of RNA and DNA.

a covalent modification is when u alter a synthesized protein to add or remove a chemical group.

people are trying to see which of these changes actually change the structure and function of the protein.

they do this through:

**immunoprecipitation - using antibodies to enrich protein antigens from a mixture. an anitgen is a protein or sugar found on the outside of cells or viruses that serves as an identification for the cell.**

**chemical treatment**

**enzymatic treatment**

**the use of reverse transcriptase enzymes**

anitbody - a blood protein counteracting a specific antigen

monoclonal antibody - human made antibody used against specific antigens. clones by itself.

“However, the majority of nucleic acid modifications lack commercial monoclonal antibodies”

aka, modification changed base, which changed protein getting made. this prob has an antigen on it but we dont know how to search for and target it because we havent made any antibodies for these types of cells yet.

“mapping techniques that rely on chemical or enzymatic treatments to manipulate modification signatures add additional technical complexities to library preparation”

[https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7113611/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7113611/)

- apparently dna modifications are done for gene expression (not random) and that s done by reader proteins and relevant effectors
- reader protein to read genetic mofication?

big problem: its hard to tell where the modification has taken place

we only know how to tag/identify very specific classes of nucleotide modifications and even that only gives us an ‘indirect readout’. aka, the protein can search for dna fragments based on their specific base pair identities so long as they aren’t already attached to the protein.

instead of using short read fragments and trying to tag and look for a nucleotide modification in them, long read fragments are way better. when using the short read stuff, you can only analyze the kinetics of the **reverse transcriptase reaction**:

start with single stranded rna, attach reverse transcriptase enzyme + have dTNA base pairs hanging out in the buffer. allow the enzyme to bind where the primer is and find the complementary dna strand to your mrna.

nanopore sequencing can directly detect any nucleic acid modification that produces a signal distortion as the nucleic acid passes through a nanopore sensor embedded within a charged membrane.

nucleic acid = chain of nucleotides

During nanopore sequencing, consecutive nucleotide sequence kmers block the pores sequentially, producing ionic currents. **Chemical modifications on nucleotides additionally alter the ionic currents** measured during nanopore sequencing

overview of nanopore sensing:

nanopore (transmembrane protein) allows the nucleic acid to pass through and reads it at the same time. at the narrowest aperture of the pore, the flow of ions is suppressed depending on the size and shape of the base present.

![[Untitled (2).png]]
The differences in raw signal between modified and unmodified bases may be quite subtle compared to the signal differences between canonical nucleotides, and are best analyzed _via_ machine learning algorithms and/or downstream analysis tools.

Nanopore sequencing produces a raw output of current intensity over time.

MinKNOW software turns the signal into a base call by matching the signal to the signal of 5 known nucleotide bases. THIS IS STORED AS A FASTQ FILE.

after base calling, can align to a reference sequence!!!!!!!!! we know the bases of what we have, then we can align this with the reference sequence for what we know we should have to look at where the modifications have occurred.

rna sequencing has 5% less accuracy than dna because they use an older base calling software. current “official” ONT base caller, Guppy, in “super accuracy” mode

PCR-amplified cDNA of an mRNA strand will give you an order of magnitude better results than a straight RNA sequenced strand

quality score is informed by the ion current signatures produced before and after the current sequencing read. guppy is ONT’s RNN neural network for base calling.