# Benchmark Study: Large Language Models in Brazil's Law Exam

This is an introductory repo to my bachelor's thesis with most of the code used to generate the results (it does not include all the code used for the PDF parsing, but all required files to run the benchmark). It 

## Table of Contents
- [Benchmark Study: Large Language Models in Brazil's Law Exam](#benchmark-study-large-language-models-in-brazils-law-exam)
  - [Table of Contents](#table-of-contents)
  - [Setup Python Virtual Environment](#setup-python-virtual-environment)
    - [RAG Hyperparameters](#rag-hyperparameters)
    - [Results](#results)
    - [Note on Reproducibility](#note-on-reproducibility)


## Setup Python Virtual Environment

To ensure a consistent development environment, it is recommended to use a Python virtual environment. Follow these steps:

1. Install `virtualenv` if you haven't already:
    ```bash
    pip install virtualenv
    ```

2. Create a virtual environment:
    ```bash
    virtualenv venv
    ```

3. Activate the virtual environment:
    - On Windows:
        ```bash
        .\venv\Scripts\activate
        ```
    - On Unix or MacOS:
        ```bash
        source venv/bin/activate
        ```

4. Install project dependencies from `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

Now your Python virtual environment is set up.


This Benchmark used GPT 4, GPT 3.5, Llama 2 13B, and Llama 2 70B. Experiments were conducted from 2023 Nov 9 to 2023 Nov 12 using OpenAI and Replicate APIs.

### RAG Hyperparameters

| Hyperparameter                       | Value |
| ------------------------------------ | ----- |
| LLM Model Temperature                | 0.2   |
| LLM Max Tokens                       | 50    |
| Text Chunk Size (Number of Chars)    | 512   |
| Text Chunk Overlap (Number of Chars) | 64    |
### Results

#### How much did OpenAI models score on the 1st Phase of the 37th OAB SP Exam (Bar Exam)?![how_much_did_openai_models_score_on_the_1st_phase_of_the_37th_oab_sp_exam_(bar_exam)?](https://github.com/mateusnobre/oab_1st_phase_brazil_law_exam_RAG/assets/45945888/78e19c0f-07c9-4ecf-a068-bf6d05244167)


#### How much did Llama2 models score on the 1st Phase of the 37th OAB SP Exam (Bar Exam)?![how_much_did_llama2_models_score_on_the_1st_phase_of_the_37th_oab_sp_exam_(bar_exam)?](https://github.com/mateusnobre/oab_1st_phase_brazil_law_exam_RAG/assets/45945888/558ee59f-c068-42c7-a0ad-6d103e0f987a)


#### How much does the embedding model matter when doing RAG? Using GPT 3.5 and retrieving 5 text chunks
![how_much_the_embeddings_model_matter_when_doing_rag?_using_gpt_3 5_and_retrieving_5_text_chunks](https://github.com/mateusnobre/oab_1st_phase_brazil_law_exam_RAG/assets/45945888/85b67485-7f37-4018-9822-89ee2d24cdb1)


### Note on Reproducibility

The results presented here are point estimates and may not be 100% reproducible due to the stochastic nature of Large Language Models (LLMs). This is especially true for commercial LLMs, where the internal workings are not fully transparent. Keep in mind that variations in results might occur even with the same hyperparameters and settings.
