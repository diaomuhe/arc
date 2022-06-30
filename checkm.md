# Install checkm on arc server
```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda create -n checkm python=3.9
conda activate checkm
conda install -c bioconda checkm-genome
```
# Run checkm on arc server
## Inspection MAGs
```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda activate checkm
export CHECKM_DATA_PATH=/work/ebg_lab/referenceDatabases/checkm # use the reference data on shared ebg directory
checkm lineage_wf -f checkm.txt -t 8 -x fa . checkm_out # run checkm
```
## checkm utility 
```
cd checkm_out
checkm coverage -x fa ../ C4.checkm_coverage.bins.tsv /gpfs/ebg_projects/subsurface/crash_course/mdiao/mapping/C4_mapping_bbmap/*sorted.bam.rename.bam > C4.coverage.log.txt
checkm profile C4.checkm_coverage.bins.tsv > C4.checkm_profile.bins.txt
checkm unbinned -x fa ../ /gpfs/ebg_projects/subsurface/crash_course/assembly_all_gown/C4/C4_contigs.500.fasta C4.unbinned.fna C4.unbinned_stats.txt
```
