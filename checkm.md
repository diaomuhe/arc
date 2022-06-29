```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda create -y -n checkm
conda activate checkm
conda install -c bioconda checkm-genome
pip3 install checkm-genome --upgrade --no-deps # upgrade checkm
export CHECKM_DATA_PATH=/work/ebg_lab/referenceDatabases/checkm
