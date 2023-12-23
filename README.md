# misinfo_detect_LLMs
In our research, we primarily focus on leveraging open-source models, specifically BERT, GPT-2, and LLaMA2.

## Data
Datasets: LIAR - William Yang Wang. 2017. “Liar, Liar Pants on Fire”: A New Benchmark Dataset for Fake News Detection. In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers), pages 422–426, Vancouver, Canada. Association for Computational Linguistics.

Labels: 'barely-true', 'false', 'half-true', 'true', and 'mostly-true'. 

Data preprocssing example for BERT & GPT-2: 
'Says the Annies List political group supports third-trimester abortions on demand. Subject: abortion. Speaker: dwayne-bohac. Speaker title: State representative.'

Data preprocssing example for Llama2:
“### Human: The statement is to be categorized into one of these labels: true, false, half-true, mostly-true, barely-true. \n Headline: 'The Annies List political group supports third-trimester abortions on demand.' Subject: Abortion. Speaker: Dwayne Bohac. Speaker's Title: State Representative.\n\n### Assistant: [Label].”

## Results
## Results

| Models / Results | Baseline (Wang, 2017) | Baseline (pre-fine tuning) | After-fine tuning |
|------------------|-----------------------|----------------------------|-------------------|
| **CNNs**         | Valid: 0.247          | Test: 0.274                |                   |
| **Llama2**       | Valid: 0.0            |                            | Valid: 0.35       |
| **Bert-large**   |                       |                            | Valid: 0.203      |
| **Llama2 7B**    |                       |                            | Valid: 0.37       |
| **GPT-2**        |                       |                            | Test: 0.34        |
|                  |                       |                            | Test: 0.23        |

Table 1: The evaluation accuracy on the LIAR dataset using different LLMs
