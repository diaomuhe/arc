### Installation 

```
apptainer build metaerg_2.5.sif docker://kinestetika/metaerg:latest
apptainer run ~/metaerg.sif metaerg --database_dir ~/metaerg_database_2.4.0 --download_database
apptainer run ~/metaerg.sif metaerg --database_dir ~/metaerg_database_2.4.0 --create_database S
```
