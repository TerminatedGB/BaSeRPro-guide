<img src="https://github.com/user-attachments/assets/59673387-cacb-4cca-a27c-03681739a9d5" width="100" align="left" />

# BaSeRPro - Batch Sequence Retrieval and Processing for GenBank

### Application Preview

<img src="https://github.com/user-attachments/assets/c1129427-0a29-4582-baf9-f3553f39e797" width="720" />
![BaSeRPro-v0 0 9_sGluw37xaI]()

### Features

* Portable Application (Windows / Mac / Linux)
* Retrieves GenBank sequences from following arguments (comma seperated OR in multiple fields): 
  * Multiple species / organism (at least one argument must be supplied)
  * Strain / Isolate / Title / Wildcard (Any)
  * Gene / Product / Locus tag (at least one argument must be supplied)
  * Sequence length / range
  * Country
  * Title of record (according to GenBank .GBFF format)
  * Three RefSeq modes: All sequences / RefSeq only / RefSeq priority (preferentially extracts RefSeq sequences first. If number of target records is not achieved, continue retrieval with non-Refseq sequences)
  * Four extraction modes:
    * Single gene
    * Gene range (Extracts segment of sequence from one gene to another [Requires input of two gene/product/locus tag arguments])
    * Gene order (Extracts segment of sequence when a specific order of genes is met [Requires input of two or moregene/product/locus tag arguments])
    * Entire sequence
* Progress bar for fetching GenBank sequences
* Automatic retries sequence retrieval to obtain desired number of target sequences if duplicate accession number is found (e.g. NZ_ vs. non-NZ_)
* Automatically generates .xlsx file containing annotations/summary of extracted GenBank records
* Automatically aligns sequences using FAMSA alignment
* Automatically trims gaps in sequence using gap threshold (0-1)
  * Example: If gappyness threshold is 0.7, at least 70 % of sequences must contain a gap in a position for EACH species for it to be trimmed
  * Default: 0.95
* Automatically generates consensus sequence based on trimmed alignment using consensus threhsold (0-1)
  * Example: If consensus threhsold is 0.2, at least 20% of equences must contain the same base in a position for it to be incorporated into the consensus sequence
  * Default: 0.1
  * Full support for ambiguous bases (both input and output)
  * Automatic detection of DNA, RNA and amino acids
  * Base frequencies of degenerate bases are shown in .xlsx summary file
* Automatically generates conservation plot based on consensus sequence (only positions with degenerate bases from consensus sequence are shown)
* Automatically retries search using provided email only if API key is invalid
* Advanced features
  * Expand extracted sequence range by number of base pairs upstream/downstream (used for checking gene boundaries)





