# WDSM: Weighted Double Score Matching

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

**WDSM** (Weighted Double Score Matching) is a statistical method for causal inference from complex survey observational data. This method integrates survey weights into matching analysis by combining propensity and prognostic scores, providing robust estimation of treatment effects while properly accounting for complex survey design.

## Key Features

- **Double Robustness**: Achieves consistency when either the population-level propensity or prognostic score model is correctly specified with survey-weighted estimation
- - **Survey Weight Integration**: Properly incorporates survey weights throughout the double score estimation and matching process
  - - **Multiple Estimands**: Supports estimation of both Population Average Treatment Effects (PATE) and Treatment Effects on the Treated (PATT)
    - - **Flexible Sampling**: Handles both retrospective sampling (selection depends on treatment) and prospective sampling (treatment-independent selection)
      - - **Reduced Bias**: Substantially reduces bias compared to unweighted methods under informative retrospective sampling
       
        - ## Background
       
        - Double score matching is an emerging method for causal inference that achieves dimension reduction and model robustness by combining propensity and prognostic scores. However, existing implementations assume simple random sampling, which limits their applicability to complex survey observational data where valid population inference requires the proper incorporation of survey weights.
       
        - WDSM extends double score matching to complex survey data by:
        - 1. Incorporating survey weights in score estimation
          2. 2. Adapting the matching procedure for weighted data
             3. 3. Providing valid inference under complex survey designs
               
                4. ## Method
               
                5. Under the weighted matching framework, WDSM provides a unified solution for incorporating survey weights throughout the double score estimation and matching process. The method:
               
                6. - Derives estimators for PATE and PATT under different sampling schemes
                   - - Establishes consistency and asymptotic normality
                     - - Maintains double robustness property in the survey-weighted setting
                       - - Provides superior robustness to model misspecification compared to single-score survey-weighted alternatives
                        
                         - ## Applications
                        
                         - WDSM is particularly useful for:
                         - - Analyzing observational data from national health surveys (e.g., NHANES)
                           - - Causal inference studies with complex survey designs
                             - - Population-level treatment effect estimation from stratified, clustered samples
                               - - Studies where valid population inference is required from non-representative samples
                                
                                 - ## Implementation
                                
                                 - ### Installation
                                
                                 - ```r
                                   # Installation instructions will be provided upon release
                                   # install.packages("devtools")
                                   # devtools::install_github("ykzeng-yale/WDSM")
                                   ```

                                   ### Basic Usage

                                   ```r
                                   # Example code will be provided
                                   # library(WDSM)
                                   #
                                   # # Estimate weighted double score matching
                                   # result <- wdsm(
                                   #   outcome = "Y",
                                   #   treatment = "A",
                                   #   covariates = c("X1", "X2", "X3"),
                                   #   weights = "survey_weight",
                                   #   data = survey_data,
                                   #   estimand = "PATE"
                                   # )
                                   ```

                                   ## Citation

                                   If you use this method in your research, please cite:

                                   ```bibtex
                                   @article{zeng2026wdsm,
                                     title={Integrating Survey Weights into Matching Analysis for Complex Survey Observational Data},
                                     author={Zeng, Yukang and Tong, Guangyu and Li, Fan},
                                     journal={},
                                     year={2026},
                                     note={In preparation}
                                   }
                                   ```

                                   ## Authors

                                   - **Yukang Zeng** - Department of Biostatistics, Yale School of Public Health; Cardiovascular Medicine Analytics Center, Yale School of Medicine
                                   - - **Guangyu Tong** - Department of Biostatistics, Yale School of Public Health; Section of Cardiovascular Medicine, Yale School of Medicine
                                     - - **Fan Li** - Department of Biostatistics, Yale School of Public Health; Section of Cardiovascular Medicine, Yale School of Medicine
                                      
                                       - ## Keywords
                                      
                                       - Causal inference, Complex surveys, Double score matching, Population average treatment effect, Retrospective sampling, Survey weights
                                      
                                       - ## License
                                      
                                       - This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
                                      
                                       - ## Acknowledgments
                                      
                                       - This work was supported by the Department of Biostatistics at Yale School of Public Health and the Center for Methods in Implementation and Prevention Science.
                                      
                                       - ## Contact
                                      
                                       - For questions or feedback, please contact:
                                       - - Yukang Zeng: yukang.zeng@yale.edu
                                         - - Guangyu Tong: guangyu.tong@yale.edu
                                           - - Fan Li: fan.li@yale.edu
                                            
                                             - ## Status
                                            
                                             - 🚧 This repository is under active development. Code and documentation will be added as the manuscript progresses through peer review.
