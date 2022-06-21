# install gtdbtk v2.1.0
delete the old version of gtdbtk on arc server 

```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
which python # check the python you are using
conda create -y -n gtdbtk
conda activate gtdbtk
conda install -c bioconda gtdbtk
download-db.sh # download the lastest database
export GTDBTK_DATA_PATH=/home/muhe.diao/.conda/envs/gtdbtk/share/gtdbtk-2.1.0/db # set the path to the reference data
```
