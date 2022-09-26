# Car Price Predictor

## Prepare environment on M1/M2 MacOS
Tutorials:
- https://github.com/jeffheaton/t81_558_deep_learning/blob/master/install/tensorflow-install-conda-mac-metal-jul-2022.ipynb
- https://www.youtube.com/watch?v=5DgWvU0p2bk&ab_channel=JeffHeaton

### Remove old Anaconda installation
```
source ~/miniconda3/bin/activate
conda init zsh

conda install anaconda-clean
anaconda-clean --yes

rm -rf anaconda3
rm -rf ~/anaconda3
rm -rf ~/opt/anaconda3
rm -rf ~/miniconda3
```

### Install XCode
```
xcode-select --install
```

### Install Miniconda3
- Go to https://docs.conda.io/en/latest/miniconda.html and download *Miniconda3 macOS Apple M1 64-bit pkg*
- Install it

### Install Jupyter and Create Environment
1. 
```
conda install -y jupyter

conda deactivate
conda env create -f tensorflow-apple-metal-conda.yml -n tensorflow

conda activate tensorflow
python -m ipykernel install --user --name tensorflow --display-name "Python 3.9 (tensorflow)"

jupyter notebook
```
2. test installation by running notebook test-environment.ipynb with selected kernel *Python 3.9 (tensorflow)*

## How to update packages in tensorflow environment
1. Update file tensorflow-apple-metal-conda.yml
2. 
```
conda env update -f tensorflow-apple-metal-conda.yml
```