
# Mutagenic Primer Design

## Introduction
This tool is designed to generate primers for quick-change missense mutations easily on google Colab. Below are the instructions for preparing the necessary input files.

## Preparing Input Files

### DNA Sequence File (FASTA Format)
- **Example Filename**: `Shaker_FL.fa`
- **Content**: Start with a header line beginning with `>`, followed by your sequence description. Write the DNA sequence in standard nucleotide codes (A, C, G, T) on the following lines. Sequence must be in frame.
- **Note**: If the first codon does not correspond with the first aminoacid, this can be indicated by modifying the `starting_residue` value
 
### Mutations File (CSV Format)
- **Example Filename**: `mutations.csv`.
- **Content**: List mutations as comma-separated values. Each line should be in the format `[position],[amino acid]`, where `[position]` is the residue number and `[amino acid]` is the desired amino acid using the single-letter code. Other options migth include "*" for ochre stop codon, "-" for amber and "X" for random mutation.


### Codon Table File (CSV Format)
- **Example Filename**:  `codontableXlaevis.csv`.
- **Content**: Include a mapping of amino acids to their respective codons. The first column lists the amino acids (single-letter code), followed by columns listing the high frequency codons.

## Running the Notebook
Execute the cells in the notebook in order, ensuring that each cell completes successfully before proceeding to the next.

## Output
- **Filename**:`primers.csv`
- **Content**: List of primers as comma-separated values. First column list the name of the primer (`position_aa_Fw`), second column is the primer sequence, the third column is the calculated Tm.
