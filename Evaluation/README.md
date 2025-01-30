 The entire evaluation process can be reproduced through the provided Jupyter notebook. We had used **Micrometrics** to evaluate model performance but in the code we had provided were using instance-based metrics.


```text
Reproducing Results

Steps:

1. Open Eval.ipynb.
2. Provide paths for the required data and model within the notebook:

   - Data Path: The dataset is located in the datasets folder.
   - Model Identifier: Choose a model identifier from the options below.

3. Run all cells in the notebook to perform the evaluation.

The dataset is in JSON format, where each entry consists of clinical text as input and the corresponding HPO terms and IDs as output.
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

