# Analysis of COVID-19 virus sequences

## Data Exploration: 

Imported necessary libraries and read a CSV file containing metadata about COVID-19 sequences continuing with data cleaning and preprocessing on the metadata.
Filtered the metadata to identify specific sequence types, such as RefSeq (reference sequences), Delta variant, and Omicron variant. 

## Downloading and Parsing Sequences

Defined a function download_sequence to retrieve nucleotide sequences from the NCBI database using accession numbers. The downloaded sequences were then parsed using the BioPython library.

## Sequence Alignment

Used the Align module from BioPython to perform pairwise sequence alignment between the reference sequence and other variants and calculated percentage of similarity between the reference sequence and the first non-mutated sequence,
Afterwards created a matrix to store alignment scores between all pairs of sequences to finall store them in a pandas DataFrame.

## Mutations 

Focused on the Omicron variant and performs a detailed alignment with the reference sequence. Mutations (insertions, deletions, and substitutions) between the two sequences were identified and highlighted using color-coded HTML formatting and visualised with  the IPython.display module.

## Translation
Finally, translated the Reference genome and the Omicron genome to their Amino-acid sequences with my https://bioinfotools.streamlit.app/ web-app, and stored them in txt file by eiting the Stop codons out, and separating the Amino-acides between them
