# Supplementary Scripts & Data

**A Benchmark of Computational CRISPR-Cas9 Guide Design Methods**
Jacob Bradford, Dimitri Perrin. 2019.

This directory contains the following files (in alphabetical order):

(see each Python script for more information)

----
#### bed_file_extractor.py

This script takes a `.bed` file and extracts desired portions as according to the configuration (adjusted within the script itself).

----
#### compare-one-with-all-others.py

This scripts compares the guides generated by one tool, with the guides generated by every other tool. 

----
#### exon_list_1m.txt

A tab-separated values file containing annotation data for our `1m` dataset (equivalent to: GRCm38/mm10 chromosome 19 10000000-11000000).

----
#### exon_list_500k.txt

A tab-separated values file containing annotation data for our `500k` dataset (equivalent to: GRCm38/mm10 chromosome 19 10000000-10500000).

----
#### exon_list_5m.txt

A tab-separated values file containing annotation data for our `5m` dataset (equivalent to: GRCm38/mm10 chromosome 19 10000000-15000000).

----
#### exon_list_full.txt

A tab-separated values file containing annotation data for our `full` dataset (equivalent to: GRCm38/mm10 chromosome 19).

----
#### generateFastaGenomeFromXu2014Data.py | generateFastaGenomeFromXu2014Data-TUSCAN.py

The script used to generate the artificial genome, which contained 1169 experimentally validated guides. 

The `-TUSCAN` edition of this script produces sequences which are 30 bp in length, rather than 23 bp.

----
#### instructions.Rmd | instructionsR.html

The setup process for each tool is described in this RMarkdown file (see the HTML version for a rendered edition). 

----
#### mm10dbAccepted.normalised

The targets which mm10db accepted when tested against the `500k` dataset.

----
#### mm10dbRejected.tsv

The targets which mm10db rejected when tested against the `500k` dataset.

----
#### mm10db-rejects-accepted-by-other-tools.py

This scripts calculates the portion of guides reported by one tool, which would have been rejected by mm10db.

----
#### normalise.py

This script converts the raw data produced by the tested guide design tools into our standard format.

----
#### normalised-extract-exon-guides.py

This script reads the normalised data (generated by normalise.py) and extracts guides that target exons. 

----
#### normalise-Xu2015.py

The intentions of this script is to normalise the data produced in the tests using the experimentally validated dataset.

----
#### plot-barStackedAcceptedGuidesRejectedByMm10dbIEEE.py

Generates a plot. The plot describes what percentage of exon-targeting guides reported by a particular tool would have been rejected by mm10db. The data for this is calculated by mm10db-rejects-accepted-by-other-tools.py.

----
#### plot-guideConsensusHeatmaps.py

This script generates the tool consensus heatmap plots in the paper.

----
#### plot-Xu2015.py

This script takes the normalised (with scores, generated by normalise-Xu2015.py) data and plots it to visualise the recall and accuracy of each tool.

----
#### Xu-2015_Is-Efficient.csv

A modified file obtained from (see below), containing the experimentally validated guides. An additional column `Xu-2015_Is-Efficient` was appended to the data, which indicates whether the guide was determined to be efficient (`1`) or inefficient (`0`).

The data is formatted as: `Gene Symbol,chrom,start of target,strand,sequence(target+3'+5'),"log2 fold change, HL60","log2 fold change, KBM7",Xu-2015_Is-Efficient`

> Xu, H., Xiao, T., Chen, C. H., Li, W., Meyer, C., Wu, Q., ... & Brown, M. (2015). Sequence determinants of improved CRISPR sgRNA design. Genome research, gr-191452.