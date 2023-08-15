# Install checkm on arc server
## Updated install
```
cnoda create -n checkm
conda activate checkm
conda install -c bioconda checkm-genome

```
## old version install
```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda create -n checkm python=3.9
conda activate checkm
conda install -c bioconda checkm-genome

### Install dependencies
pip install pysam
pip install dendropy
conda create -n pplacer python=3.9
conda activate pplacer
conda install -c bioconda pplacer 
```
# Run checkm on arc server
## Inspection MAGs
```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda activate checkm
export CHECKM_DATA_PATH=/work/ebg_lab/referenceDatabases/checkm # use the reference data on shared ebg directory
conda activate pplacer # load pplacer
module load hmmer/v3.3 # load hmmer
module load prodigal/v2.6.3 # load prodigal
checkm lineage_wf -f checkm.txt -t 8 -x fa PATH_To_Bins checkm_out # run checkm
```
## checkm utility 
```
# move into "checkm_out" direcotry
>cd checkm_out

# print the "checkm coverage" usage message. This command needs the sorted and indexed bam files
>checkm coverage -h
#produces coverage profiles for all the MAGs inside the "binning" directory
>checkm coverage -x fa ../ your_sample_id.checkm_coverage.bins.tsv the_path_to_your_mapping_dir_generated_in_mapping_section/*sorted.bam > your_sample_id.coverage.log.txt

# print the "checkm profile" usage message
>checkm profile -h
# determine the percentage of each bin relative to all genome bins under consideration.
>checkm profile your_sample_id.checkm_coverage.bins.tsv > your_sample_id.checkm_profile.bins.txt

# Calculate sequence coverage for good bins
checkm qa -c your_sample_id.checkm_coverage.bins.tsv lineage.ms . -f your_sample_id_checkm_qa_bins.txt -o 2 --tab_table

# print the "checkm unbinned" usage message
>checkm unbinned -h
# extract unbinned sequences and get unbinned sequence statistics
>checkm unbinned -x fa ../ your_contig_file_longer_than_500bp.fasta your_sample_id.unbinned.fna your_sample_id.unbinned_stats.txt
```
### checkm utility example
```
cd checkm_out
checkm coverage -x fa ../ C4.checkm_coverage.bins.tsv /gpfs/ebg_projects/subsurface/crash_course/mdiao/mapping/C4_mapping_bbmap/*sorted.bam.rename.bam > C4.coverage.log.txt
checkm profile C4.checkm_coverage.bins.tsv > C4.checkm_profile.bins.txt
checkm qa -c C4.checkm_coverage.bins.tsv lineage.ms . -f C4_checkm_qa_bins.txt -o 2 --tab_table
checkm unbinned -x fa ../ /gpfs/ebg_projects/subsurface/crash_course/assembly_all_gown/C4/C4_contigs.500.fasta C4.unbinned.fna C4.unbinned_stats.txt
```

https://github.com/xiaoli-dong/metagenomics_crash_course/blob/master/binning/bin_quality_assessment.md
