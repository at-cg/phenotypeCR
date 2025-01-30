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
    |---Evaluation
    |---test
    |---create_embeddings.ipynb
    |---gpt_models.ipynb
    |---README.md
    |---requirements.txt
```


We have provided a jupyter notebook `gpt_models.ipynb` which demonstrates how to use the models for phenotype concept recognition and normalisation. Besides, we have provided a `test` directory which contains the sample data and the output of the models. The `Evaluation` directory contains the datasets, `Eval.ipynb` file for reproducing the results.

## Updating and Creating HPO Term Embeddings

HPO updates frequently with new terms. To handle this, we provide a method to generate embeddings for new HPO terms.

```text
Steps to create embeddings:
1. Download the latest `hp.obo` file from:
   [http://purl.obolibrary.org/obo/hp.obo](http://purl.obolibrary.org/obo/hp.obo)

2. Open the `create_embeddings.ipynb` notebook.

3. Update the file path in the notebook to point to the downloaded `hp.obo` file.

4. Run the notebook to generate embeddings.

5. The resulting CSV file will contain embeddings for the new HPO terms.

```


## Model Options

You can select either a finetuned or base model depending on your evaluation needs.

```text
Finetuned Models

For improved accuracy, use the following finetuned models:

1. GPT4o-mini-2024-07-18:
   - Identifier: ft:gpt-4o-mini-2024-07-18:iisc-bangalore::AYf5TC9S

2. GPT4o-2024-08-06:
   - Identifier: ft:gpt-4o-2024-08-06:iisc-bangalore::AZ03ME6y

Base Models

For zero-shot evaluation, use one of these base models:

1. GPT4o-mini-2024-07-18:
   - Identifier: gpt-4o-mini-2024-07-18

2. GPT4o-2024-08-06:
   - Identifier: gpt-4o-2024-08-06
```

## How to Use the Models

To use these models, you need an **OpenAI API key** to access the GPT4o models. If you do not have an API key, you can use the alternative **`BioMED_NER`** model.

```text
Steps to use the models:

1. Refer to the `gpt_models.ipynb` notebook for guidance.

2. If using a custom dataset, refer to the `test` directory for a sample file format.

3. Ensure the following:
   - Update paths in the notebook to match your data and model setup.
   - Follow the sample file format in the `test` directory to ensure consistent results.
```

