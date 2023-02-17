# Efficient fair PCA for fair representation learning

This repository contains code for our AISTATS 2023 paper [Efficient fair PCA for fair representation learning](http://aistats.org/aistats2023/accepted.html).

## Preparations

* install all required packages as specified in `requirements.txt`.

* set the project root directory as your working directory.

* download the code provided by Lee et al. (2022) by running
   `git clone https://github.com/nick-jhlee/fair-manifold-pca.git`. Their code requires Matlab
   and R, and since our code is built on theirs, so does ours.

* download the code provided by Ravfogel et al. (2020) by running
   `git clone https://github.com/shauli-ravfogel/nullspace_projection.git`. Change Line 5 in
   `nullspace_projection/src/debias.py` from 'from src import classifier' to
   'from nullspace_projection.src import classifier'.

* download the code provided by Ravfogel et al. (2022) by running
   `git clone https://github.com/shauli-ravfogel/rlace-icml.git`. Rename the folder rlace-icml to
   rlace_icml.

* download some of the code provided by Samadi et al. (2018) by running 

   `wget https://raw.githubusercontent.com/samirasamadi/Fair-PCA/master/optApprox.m -P experiment_as_in_Lee_real_data` 
   `wget https://raw.githubusercontent.com/samirasamadi/Fair-PCA/master/mw.m -P experiment_as_in_Lee_real_data`

* download the Adult Income and the Bank Marketing dataset from the UCI repository to the folder comparison_with_Agarwal by running 
   1. `wget https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data`
   2. `wget https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.test`
   3. `wget https://archive.ics.uci.edu/ml/machine-learning-databases/00222/bank-additional.zip`
   4. `unzip bank-additional.zip` 
   from within that folder. Delete the first row of the adult.test file.
 

 
## Running the code

* in order to produce the plots of Figure 1, from the project root directory run `illustration_Figure1/illustration_Figure1.py`.

* in order to produce the plots in Figures 3 & 4, from the project root directory first run `experiment_as_in_Lee_synthetic_data/experiment_as_in_Lee_synthetic_data.py`,
   then `experiment_as_in_Lee_synthetic_data/analysis.m`, and finally
   `experiment_as_in_Lee_synthetic_data/boxplot.R`.

* in order to produce the results of Tables 1 to 3, from the project root directory first run `experiment_as_in_Lee_real_data/experiment_as_in_Lee_real_data.py`,
   then `experiment_as_in_Lee_real_data/analysis.m`, then
   `experiment_as_in_Lee_real_data/MLP_analysis.py`, and finally
   `experiment_as_in_Lee_real_data/write_results.py`.

* in order to produce the plots of Figures 4 & 8, from the project root directory
 run `comparison_with_Agarwal/comparison_with_Agarwal.py`. Change the parameters in 
   Lines 15 - 20 depending on which plots you want to create.
 


 ## Citation

If you publish material that uses this code, please cite our paper:

```js
@inproceedings{kleindessner2022fairordreg,
title={Pairwise Fairness for Ordinal Regression},
author={Kleindessner, Matthäus and Donini, Michele  and Russell, Chris and Zafar, Muhammad Bilal},
year={2023},
booktitle={International Conference on Artificial Intelligence and Statistics (AISTATS)}
}
```

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This project is licensed under the Apache-2.0 License.