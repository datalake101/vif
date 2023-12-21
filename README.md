library(jtools)  
 
df=import("https://raw.githubusercontent.com/datalake101/vif/main/df.csv")
 
m=glm(ncd_diabetes~year+agee+race, data=dd, family = 'binomial')

summ(m,confint = T, digits = 3, vifs = T)
MODEL INFO:
Observations: 68944
Dependent Variable: ncd_diabetes
Type: Generalized linear model
  Family: binomial 
  Link function: logit 

MODEL FIT:
χ²(15) = 481.308, p = 0.000
Pseudo-R² (Cragg-Uhler) = 0.012
Pseudo-R² (McFadden) = 0.008
AIC = 60427.189, BIC = 60573.446 

Standard errors: MLE
----------------------------------------------------------------------
                      Est.     2.5%    97.5%    z val.       p     VIF
----------------- -------- -------- -------- --------- ------- -------
(Intercept)         -1.838   -1.905   -1.771   -53.689   0.000        
year2013             0.047   -0.035    0.128     1.126   0.260   1.006
year2014             0.118    0.038    0.198     2.876   0.004   1.006
year2015             0.028   -0.060    0.116     0.622   0.534   1.006
year2016             0.096    0.009    0.184     2.167   0.030   1.006
year2017            -0.007   -0.095    0.081    -0.151   0.880   1.006
year2018             0.063   -0.024    0.150     1.426   0.154   1.006
year2019             0.158    0.073    0.244     3.650   0.000   1.006
year2020            -0.046   -0.155    0.064    -0.817   0.414   1.006
year2021             0.171    0.070    0.272     3.313   0.001   1.006
agee14               0.080    0.026    0.135     2.890   0.004   1.007
agee15               0.147    0.087    0.207     4.795   0.000   1.007
agee16               0.149    0.095    0.204     5.383   0.000   1.007
race2                0.337    0.274    0.400    10.508   0.000   1.011
race3                0.877    0.775    0.979    16.811   0.000   1.011
race4               -0.208   -0.271   -0.145    -6.450   0.000   1.011
----------------------------------------------------------------------
-------------------------
