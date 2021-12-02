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
   
   
   
Inputs to all models include X..impervious, Land.Use, and Koppen.Geiger.Zone
All predictions are reported in log10 of mg/L for nutrients and sediments.
All prediction are reported in log10 of μg/L for metals.   
