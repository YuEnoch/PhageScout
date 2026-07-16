# PhageScout

Substrate phage display analysis for **cathepsin G** and **elastase**: cleavage preferences from SPD screens are combined with AlphaFold structural features to score and predict MEROPS cleavage sites.

## Analysis

Main notebook: [`PhageScout_code.Rmd`](PhageScout_code.Rmd)

1. Unselected (FLAG) library composition  
2. DESeq2 enrichment vs FLAG  
3. PWMs and peptide profiles (DESeq2 / significant peptides; aligned and unaligned)  
4. MEROPS site mapping onto AlphaFold models  
5. Cut-site scoring, structural annotation, and PWM validation  
6. Per-protease XGBoost classifiers (sequence + structure)

Figures are written to `figures/`.

Upstream sequencing / peptide translation: [ProteaseProfiling](https://github.com/YuEnoch/ProteaseProfiling)

## Requirements

R with DESeq2, DECIPHER, ggseqlogo, xgboost, pROC, and related tidyverse / structure packages (see the Setup chunk in the notebook).
