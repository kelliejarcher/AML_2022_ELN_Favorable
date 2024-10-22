# 2022_ELN_Favorable_Code.Rmd
R code for replicating results in Archer et al., "Improving risk stratification for 2022 European LeukemiaNet favorable-risk patients with acute myeloid leukemia"

# hdcuremodels 
The hdcuremodels R package was used for fitting high-dimensional mixture cure models. A vignette to illustrate usage is included. 

This package is also available from the Comprehensive R Archive Network at https://cran.r-project.org/web/packages/hdcuremodels/index.html and can be installed in R by issuing

 > install.packages("hdcuremodels")

# 2022_ELN_Favorable_Data.RData 

This is the R workspace required by 2022_ELN_Favorable_Code.Rmd and contains the following objects: 

eset.fav.filter: an ExpressionSet the filtered normalized training set gene expression and phenotypic data \
alliance.frame:  data.frame that includes the time-to-event outcome (cryr), censoring indicator (relapse.death), and expression for all genes retained after filtering \
weibull.gmifs:  the mixturecure model fit to the training set (lines 51-56 - retained because it takes > 11 hours to run) \
amlcg.final:  an ExpressionSet that includes the normalized test set gene expression and phenotypic data after filtering to retain probe sets that mapped to transcripts included in the training set mixture cure model\
amlcg.frame: data.frame that includes the time-to-event outcome (cryr), censoring indicator (relapse.death), and gene expression data filtered to retain probe sets that mapped to transcripts included in the training set mixture cure model\
select.inc: vector of probe sets that map to transcripts having non-zero coefficient estimates in the training set incidence portion of the model \
select.lat: vector of probe sets that map to transcripts having non-zero coefficient estimates in the training set incidence portion of the model \
weibull.gmifs.test: the mixturecure model fit to the test set 

# KJArcher_hdcuremodels_06-13-2024.pdf

These are slides from my presentation at the R/Medicine conference. The illustrative datasets amltrain and amltest include cytogenetically normal AML patients (not ELN Favorable).
