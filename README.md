# Prioritizing Repurposable Drugs for SARS-CoV-2 using Deep Learning and Population-based Validation
This is a code repository for project "Prioritizing Repurposable Drugs for SARS-CoV-2 using Deep Learning and Population-based Validation"

## Requirements
### Prepare necessary data
- Obtain Chemical-Gene Interactions, Genes, Phenotypes, and Pathways from [COVID-19 curated list](http://ctdbase.org/detail.go?type=disease&acc=MESH%3aC000657245). Move the file under `./data/CTD/`. 
```
data/CTD/drug-gene-CTD_C000657245_ixns_20200703223915.tsv
data/CTD/pathways-CTD_C000657245_pathways_20200703225429.tsv
data/CTD/phenotype-drug-gene-CTD_C000657245_diseases_20200703224649.tsv
```
- Obtain virus-host protein-protein interaction from Gordon et al. [Nature 2020](https://www.nature.com/articles/s41586-020-2286-9#Sec36)
```
data/biology-database/baits-prey-mist.csv
```

- Download pre-trained [DRKG embedding](https://github.com/gnn4dr/DRKG).  Locate the files under `./data/DRKG/`
```
data/DRKG/embed/DRKG_TransE_l2_entity.npy
data/DRKG/embed/entities.tsv
data/DRKG/embed/relations.tsv
```


### Install packages
```
$ pip install torch-geometric
$ pip3 install torch
```

## Notebooks for drug repurposing pipeline
We provided a self-contained notebook for easy dissemination
### Preprocessing

