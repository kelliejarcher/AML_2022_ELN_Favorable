# 2022_ELN_Favorable_Code.Rmd
R code for replicating results in Archer et al., "Improving risk stratification for 2022 European LeukemiaNet favorable-risk patients with acute myeloid leukemia"

# hdcuremodels is our R package for fitting high-dimensional mixture cure models

# 2022_ELN_Favorable_Data.RData is the R workspace required by 2022_ELN_Favorable_Code.Rmd and contains the following objects: 

eset.fav: an ExpressionSet that includes the full normalized training set gene expression and phenotypic data \
eset.fav.filter: an ExpressionSet the filtered normalized training set gene expression and phenotypic data \
alliance.frame:  data.frame that includes the time-to-event outcome (cryr), censoring indicator (relapse.death), and expression for all genes retained after filtering \
weibull.gmifs:  the mixturecure model fit to the training set (lines 51-56 - retained because it takes > 11 hours to run) \
amlcg.final:  an ExpressionSet that includes the full normalized test set gene expression and phenotypic data\
amlcg.frame: data.frame that includes the time-to-event outcome (cryr), censoring indicator (relapse.death), and gene expression data \
select.inc: vector of probe sets that map to transcripts having non-zero coefficient estimates in the training set incidence portion of the model \
select.lat: vector of probe sets that map to transcripts having non-zero coefficient estimates in the training set incidence portion of the model \
weibull.gmifs.test: the mixturecure model fit to the test set \

