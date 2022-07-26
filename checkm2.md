# Install checkm2

```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
git clone --recursive https://github.com/chklovski/checkm2.git && cd checkm2
conda env create -n checkm2 -f checkm2.yml
conda activate checkm2
bin/checkm2 -h # run checkm2 without installation
```
Tried `python setup.py install`, but did not work

# Running checkm2
```
checkm2 predict --threads 30 --input <folder_with_bins> --output-directory <output_folder> 
