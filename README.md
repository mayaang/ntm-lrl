This github repo contains notebooks investigating current transfer learning options for machine translation for low resource languages. It is a student project on the go.


## Main

In order to be able to reproduce the results the first thing to do it to clone the repository

`git clone https://github.com/mayaang/nmt-lrl.git`
`cd nmt-lrl`

1. Prepare russian-english wikimatrix dataset for opennmt: run prepare-opennmt-russian-dataset.ipynb

2. Prepare bulgarian-english setimes dataset for opennmt: run prepare_opennmt_bulgarian_dataset.ipynb


3. Compute a benchmark for MarianMT: run benchmark_bg_en_translation_marianmt.ipynb

4. Train OpenNMT LSTM Bulgarian English model from scratch: opennmt-train-bg-from-scratch.ipynb


5. Fine-tune on an already pre-trained and available from OpenNMT German-English Transformer language model: run opennmt_fine-tune_en_de_transformer.ipynb
 
6. Train a PTM Russian-English and fine-tune on Bugalrian dataset: run opennmt_ptm_ru_ft_bg.ipynb

## Manual Evaluation for the first 50 Translations.


`ipython manual_evaluation.py ref_bg.txt`


## Automatic evaluation

### nlg-eval


Notebook: evaluation.ipynb

### bleurt

the evaluation can be performed using the notebook bleurt_manual.ipynb

## Manual Evaluation
all the relevant scripts and data are to be found in the questionary folder of the repo

`python3 display_results.py some_ref_translation.json`

