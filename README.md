# NICE-seq Data Analysis Pipeline

This pipeline is designed to analyze NICE-seq sequencing data. Below are the steps involved:

1. **Quality Control (QC) for NICE-seq Data:**
   - FASTQ files are checked for quality using FastQC, and a summary report is generated.

2. **Read Alignment for NICE-seq Data:**
   - Reads are aligned to the reference genome using BWA, and sorted and indexed BAM files are generated.

3. **Filtering of Aligned Reads:**
   - PCR duplicates and low-quality reads are removed from the aligned reads.

4. **Peak Calling for NICE-seq Data:**
   - Nucleosome-protected ends are identified using MACS2.

5. **Annotation of Peaks:**
   - Annotate the identified peaks with genomic features using annotatePeaks.pl.

6. **Differential Accessibility Analysis (Optional):**
   - Perform differential accessibility analysis if comparing between different experimental conditions using tools like DESeq2.

7. **Functional Enrichment Analysis:**
   - Perform functional enrichment analysis of nucleosome-protected ends using external tools like GREAT.

8. **Visualization and Interpretation:**
   - Visualize and interpret the identified nucleosome-protected ends and differential accessibility using tools like deeptools.

## Usage
- Clone this repository.
- Place your NICE-seq FASTQ files and reference genome in the same directory as the pipeline script.
- Modify the script as necessary to specify paths and parameters.
- Run the pipeline using `./pipeline.sh`.

## Requirements
- BWA
- Samtools
- MACS2
- FastQC
- deeptools
- R (if performing differential analysis)

## Notes
- Adjust parameters and additional analysis steps based on specific experimental needs.
- Ensure reference genome files are available and properly indexed.
- External tools such as GREAT and DESeq2 need to be installed separately.
