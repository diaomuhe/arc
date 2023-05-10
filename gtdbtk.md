# install gtdbtk v2.1.0
delete the old version of gtdbtk on arc server 

```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
which python # check the python you are using
conda create -y -n gtdbtk
conda activate gtdbtk
conda install -c bioconda gtdbtk
download-db.sh # download the lastest database
export GTDBTK_DATA_PATH=/work/ebg_lab/referenceDatabases/GTDB_R207/release207_v2 # set the path to the reference data
export GTDBTK_DATA_PATH=/home/muhe.diao/.conda/envs/gtdbtk/share/gtdbtk-2.1.0/db # set the path to the reference data
```

# install gtdbtk v2.3.0
```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda create -y -n gtdbtk-2.3.0
conda activate gtdbtk-2.3.0
conda install -c bioconda gtdbtk
```
Still get the version 2.1.0 on arc server

```
conda create -n gtdbtk-2.3.0 -c conda-forge -c bioconda gtdbtk=2.3.0
```
Successfully installed on local PC


