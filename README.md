# phenotypeCR
HPO-based phenotype concept recognition using language models

## Installation
```bash
git clone https://github.com/at-cg/phenotypeCR.git
cd phenotypeCR
pip install requirements.txt
```

Download files from [here](https://drive.google.com/drive/folders/1ED1gqeqnyvX_Sk5_KA_W5XxMVDrWk2tS)
## move files to the following directories
```bash
mv Downloads/embeddings/* .
```

else run the following commands
```bash
gdown 1ED1gqeqnyvX_Sk5_KA_W5XxMVDrWk2tS
```

## After this step the directory structure should look like this
```bash
---phenotypeCR
   |---2022
        |---HPO_embeddings_38k.csv
        |---hpo2022.txt
    |---2024
        |---HPO_embeddings_40k.csv
        |---child_parent_dict_merged.json
        |---hpo_dict.txt 
        |---phenotype_to_genes.txt
    |---gpt_models.ipynb
    |---README.md
    |---requirements.txt
```


