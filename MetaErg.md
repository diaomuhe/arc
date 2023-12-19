### Installation 

```
apptainer build metaerg.sif docker://kinestetika/metaerg:latest
apptainer run ~/metaerg.sif metaerg --database_dir ~/metaerg_database_2.4.0 --download_database
apptainer run ~/metaerg.sif metaerg --network host -v ~/metaerg_database_2.4.0:/databases --database_dir ~/metaerg_database_2.4.0 --create_database S
```
