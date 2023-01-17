# Financial-calculator
predicting future stock price w.r.t net profit and cash flows

This code takes some input in the format of array of the past net profits and 
cash flows (yearly basis) and w.r.t each year's performance and calculates the average 
increament of NP of CF (CAGR or Average, whichever is lower), calculates the future NP's 
and CF's for next (typically 40) years.While calculating the next year's performances, 
the code halfs the increament rate after every 5 future years and finally takes same for 
all the way from 20th to 40th year. So for the input of the profits of last 10years, it
will generate 10 forecasts for any future year's profit and take the average of them and
discount them to current value. According to that, it will use the DCF methode to evaluate
the intrinsic share price of the company. 


the inputs are in the form:

################################################################################################################################################

current_price=278                   #current market price
marketcap= 15685                     #market cap of the company
debt_to_equity= 0.04                   #debt_to equity
roce= 36.2                             #ROCE
roe= 23                            #ROE
pe= 9.53                             #pe ratio of the company
medpe=12.1                             #avg pe of 10Y
pb=1.8                              #PB
medpb=2.2                          #avg pb of 10y
peg=0.39                            #PEG
inflation=7                         #assumed inflation rate
margin_of_safety=20                    #margin of safety


netprofit=[578,545,538,417,488,465,718,958,1190,2279,2192,2231]        #Net profit array
cashflow=[598,795,692,644,626,603,1644,1669,2044,2771,2897,2746]       #Operating cash flow array


company="GUJARAT STATE PETRONET"

factor=4        #We are assuming the future growth rates (Both NP and CF) will reduce by 1/factor times w.r.t past average/CAGR as the future is uncertain. 
time=40         #Total time we assume the company will be there
starting_year=2011    #Year from where the NP or CF data is available

current_year=2023

###############################################################################################################################################

The output is a jpg file (change the location to save the file in your computer in the plotting panel, otherwise it will show error) that contains different 
informations like intrinsic value (based on both net profit and cash flow), CAGR of NP and CF till now etc...



