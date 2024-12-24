
#![BaSeRPro](https://github.com/user-attachments/assets/59673387-cacb-4cca-a27c-03681739a9d5)
 BaSeRPro - Batch Sequence Retrieval and Processing for GenBank

### Application Screenshot

![BaSeRPro_X3WdeoIfq1](https://github.com/user-attachments/assets/3f045395-5980-40d5-94bf-f1a2d64c3c5c)

### Features

* Portable Application (Windows / Mac / Linux)
* Retrieves GenBank sequences from following arguments (comma seperated OR in multiple fields): 
  * Multiple species / organism (at least one argument must be supplied)
  * Strain / Isolate 
  * Gene / product (at least one argument must be supplied)
  * Sequence length / range
  * Country
  * Title of record (according to GenBank .GBFF format)
  * Three RefSeq modes: All sequences / RefSeq only / RefSeq priority (preferentially extracts RefSeq sequences first. If number of target records is not achieved, continue retrieval with non-Refseq sequences)
  * Two extraction modes: Single Gene (Extracts single gene) / Gene range (Extracts segment of sequence to another [Requires input of two gene/product arguments])
* Progress bar for fetching GenBank sequences
* Automatically generates .xlsx file containing annotations/summary of extracted GenBank records
* Automatically aligns sequences using FAMSA alignment
* Automatically trims gaps in sequence using gap threshold (0-1)
  * Example: If gappyness threshold is 0.7, at least 70 % of sequences must contain a gap in a position for EACH species for it to be trimmed
* Automatically generates consensus sequence based on trimmed alignment using consensus threhsold (0-1)
  * Example: If consensus threhsold is 0.2, at least 20% of equences must contain the same base in a position for it to be incorporated into the consensus sequence
  * Full support for ambiguous bases (both input and output)
  * Automatic detection of DNA, RNA and amino acids
  * Base frequencies of degenerate bases are shown in .xlsx summary file
* Automatically generates conservation plot based on consensus sequence (only positions with degenerate bases from consensus sequence are shown)
* Automatically retries search using provided email only if API key is invalid





