# Do language models make human-like predictions about the coreferents of Italian anaphoric zero pronouns?

This repository includes all the files required to replicate the paper "Do language models make human-like predictions about the coreferents of Italian anaphoric zero pronouns?", accepted at COLING 2022.

Paper abstract:
> Some languages allow arguments to be omitted in certain contexts. Yet human language comprehenders reliably infer the intended referents of these *zero* pronouns, in part because they construct expectations which referents are more likely. We ask whether Neural Language Models also extract the same expectations. We test whether 12 contemporary language models display expectations that reflect human behavior when exposed to sentences with zero pronouns from five behavioral experiments conducted in Italian by Carminati (2005). We find that at least three models capture human behavior from each experiment, with three&mdash;XGLM 2.9B, 4.5B, and 7.5B&mdash;successfully modeling human behavior from all the experiments. This result suggests that human expectations about coreference can be derived from exposure to language, and also indicates features of language models that allow them to better reflect human behavior.

## Respository Contents

### Data 
The aim of the study was to model specific effects found by Carminati (2005) on the processing of Italian sentences involving zero anaphora. The stimuli are included in Appendix A of the original paper. These are included in the `stimuli` directory. `carminati_2005.stims` is the file used as input to the language models (using the Python code provided), while `carminati_2005.csv` also includes additional information relevant for statistical analysis.

### Python Code
The file `transformers_code.py`, can be used to run experiments of the kind reported in the paper. It is intended to be run from the command line. Information about the relevant arguments can be found by typing `python transformers_code.py -h` in the command line. `transformers_code.py` was written for `Python 3.8` and requires the `pytorch` and `transformers` packages.

The `run_experiments.sh` bash script runs the experiments we present in the paper. 

The `models.txt` file consists of the names (as listed on the [Hugging Face Model Hub](https://huggingface.co/models)) of all the transformer language models used in our analyses, with each model name listed on a separate line. This is used by `transformers_code.py`.

### R Code

The results of the study were analyzed using R. `StatisticalAnalysis.Rmd` runs all the analyses resported in the paper. The 'knitted' HTML version of this R Markdown file is also included as `StatisticalAnalysis.html`.


## How to cite
This will be updated. The final version of the paper can be found [here](https://arxiv.org/abs/2208.14554).

## References

* Carminati, M. N. (2005). [Processing reflexes of the Feature Hierarchy (Person> Number> Gender) and implications for linguistic theory](https://doi.org/10.1016/j.lingua.2003.10.006). *Lingua, 115*(3), 259-285.
