https://rcs.ucalgary.ca/index.php?title=Python&action=edit&section=5 #install own python

```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
which python # check the python you are using
conda create -n arb # create environment
conda install -n arb -c bioconda arb-bio
conda activate arb
arb
```
