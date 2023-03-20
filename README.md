# globalurbanstormwaterMLR
MLR of urban stormwater concentrations
Our Rdata file contains the dataframe used to generate the stormwater prediction models. This includes the following models: 
lm.TSS- total suspended solids
lm.TN- total nitrogen
lm.TP- total phosphorus
lm.NH3- ammonia
lm.NO2.3- nitrate+nitrite
lm.TKN- total Kjeldahl nitrogen
lm.OP- orthophosphates
lm.Cd- cadmium
lm.Cr- chromium, does not meet model assumptions
lm.Cu- copper
lm.Ni- nickel
lm.Pb- lead
lm.Zn- zinc
   
   
   
Inputs to all models include 'X..impervious', 'Land.Use', and 'Koppen.Geiger.Zone'
All predictions are reported in log10 of mg/L for nutrients and sediments.
All prediction are reported in log10 of μg/L for metals.   

#example#
Type in the code:
predict(lm.TP,newdata=data.frame(X..impervious=61,Land.Use='residential',Koppen.Geiger.Zone='Cwa',stringsAsFactors=T), interval = "confidence")
Change lm.TP, residential, Cwa as needed for different scenarios
Model output:
        fit       lwr       upr
  -0.437959 -1.057273 0.1813546
Thus, the predicted concentration for this scenario is 10^(-0.437959) mg/L with a confidence interval of (10^(-1.057273) , 10^(0.1813546)).


Input options:
X..impervious = [0,100]
Land.Use = 'road', 'residential', 'industrial', 'commercial', 'single family residential', 'multi family residential', or 'city center' 
Koppen.Geiger.Zone = 'Af', 'BSh', 'BSk', 'BWh', 'Cfa', 'Cfb', 'Csa', 'Csb', 'Cwa', 'Cwb', 'Dfa', 'Dfb', or 'Dwa' (refer to graphs in publication [or Table 3] for which KGZs do not have data in them, model will not run for those few zones)

