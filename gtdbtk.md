## install gtdbtk v2.1.0

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
conda create -n gtdbtk-2.3.0 -c conda-forge -c bioconda gtdbtk=2.3.0
conda env config vars set GTDBTK_DATA_PATH="/work/ebg_lab/referenceDatabases/GTDB_R214" # set up reference database
gtdbtk classify_wf --genome_dir /work/ebg_lab/eb/crash_course/GOWN/metagenomics_Aug2022/binning/22GWC22042-GOWN983/dastool/G7_DASTool_bins -x fa --out_dir gtdbtk_out --mash_db /work/ebg_lab/referenceDatabases/GTDB_R214/mash --cpus 10
```



