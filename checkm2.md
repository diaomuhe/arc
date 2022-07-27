# Install checkm2

```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
git clone --recursive https://github.com/chklovski/checkm2.git && cd checkm2
conda env create -n checkm2 -f checkm2.yml
conda activate checkm2
/home/muhe.diao/programs/checkm2/bin/checkm2 -h # run checkm2 without installation
```
Tried `python setup.py install`, but did not work

# Running checkm2
```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
conda activate checkm2
module load prodigal/v2.6.3
module load diamond/v2.0.6
/home/muhe.diao/programs/checkm2/bin/checkm2 predict --threads 30 --input ./*.fa --output-directory checkm2_out 


https://github.com/chklovski/CheckM2
