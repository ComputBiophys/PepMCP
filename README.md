# PepMCP
a peptide-specific MCP predictor using GraphSAGE

![image](https://github.com/ruihan-dong/PepMCP/blob/main/framework.png)


## Requirements
### ESMC environment
* python == 3.12
* pytorch 
* [esm](https://pypi.org/project/esm/)
* transformers
### PepMCP environment
* pytorch
* transformers
* [dgl](https://www.dgl.ai/pages/start.html)
* sklearn (for training evaluation)

## Usage
### Prediction
Test sequences and names are in `./data/test.csv`
```bash
python ESMC_extract.py  # ESMC environment
python predict.py       # PepMCP environment
```

### Training
#### Data processing
(This step can be skipped for using 5-fold datasets in `./data/res_split` or `./data/seq_split` directly)
```bash
python preprocess.py
python ESMC_extract.py   # change file name to MemAMPs.csv or pdb_sol_neg.txt, under ESMC environment
```
#### Run
```bash
python train.py
```

## Citation
To be updated
