# Details about how to further validate the prognostic model 


Please see the Appendix file related to the Li, Y. et al. (2025). Personalised prediction of institutionalisation in Parkinson’s: Prognostic factor identification and model development and validation using IPD meta-analysis.


Table S7 and Table S9 can both be found in the Appendix 10.


In this study, the equation of Royston-Parmar model is g(S(t,x))=s(ln(t),γ)+β^T x, where s(ln(t),γ)=γ_0+γ_1  ln⁡(t) is based on the position of knots and the time point of interest for making predictions. Therefore, researchers can adjust the position of knots based on their study’s population, but this requires knowledge of the distribution of survival times in their population. We suggest researchers to use R function “basis” in “flexsurv” package15 to calculate the basis spline function to adjust the model for their population. With information of the positions of knots in table S7 and table S9, researchers could also use R function “basis” in “flexsurv” package to calculate the basis spline function in the 7-year model and the 10-year model developed in this study. For example, the R code to calculate the basis spline function for CamPalGN study in 10-year model will be “basis(knots,log(10))”, where “knots” contains the value of the first boundary knot, the internal knot and the last boundary knot from table S9. We suggest researchers using the information we provide in this section to rebuild the Royston-Parmar model developed in this study and perform further external validation in their study population.  
