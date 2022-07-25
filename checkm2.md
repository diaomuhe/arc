# Install checkm2

```
export PATH=/home/muhe.diao/miniconda3/bin:$PATH
git clone --recursive https://github.com/chklovski/checkm2.git && cd checkm2
conda create -n checkm2 python=3.9 # conda env create -n checkm2 -f checkm2.yml did not work
conda activate checkm2
python setup.py install
```

# Running checkm2
```
checkm2 predict --threads 30 --input <folder_with_bins> --output-directory <output_folder> 
