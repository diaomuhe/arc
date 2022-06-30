```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda create -n checkm python=3.9
conda activate checkm
conda install -c bioconda checkm-genome
export CHECKM_DATA_PATH=/work/ebg_lab/referenceDatabases/checkm # use the reference data on shared ebg directory
checkm lineage_wf -f checkm.txt -t 8 -x fa . checkm_out # run checkm
