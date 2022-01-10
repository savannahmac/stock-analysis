# Green Stocks Analysis 

## Project Purpose: 

The client, Steve, would like to assist his parents in choosing the most appropriate sustainable stock for future investment. 
The program will analyze stock returns from multiple years to allow Steve to quickly and easily compare the Daily Volume and Return for 
each stock in a given year. Initially, the program was adequate to run an analysis on a small number of stocks. However, this project was
refactored so that Steve could run hundreds of stocks in order to find the absolute best fit for his parents' investment. 

## Results: 

### 2017 Stocks Analysis
*The 2017 Stock Analysis ran in 0.07 seconds. This was significantly faster than the original run time of 0.77 seconds.
*Refactoring the original code so that the tickers were part of an index affected the run time significantly. See the code to initiate the index below: 
	'1a) Create a ticker Index
    		tickerIndex = 0

    	'1b) Create three output arrays
    		Dim tickerVolumes(12) As Long
    		Dim tickerStartingPrices(12) As Single
    		Dim tickerEndingPrices(12) As Single
*This refactoring should allow Steve to run exponentially more stocks simply by adding them to our identified ticker index. 

Steve and his parents should note the following stock outcomes: 

![vba_challenge_2017](https://user-images.githubusercontent.com/93888037/148706883-48b95ea3-8d7d-4265-bc09-63f2a1b4581d.png)

*Nearly all of the sustainable stocks selected show a favorable return.
*Most notably, the stocks DQ and SEDG showed nearly a 200% return. 
*In 2017, the stock with the most unfavorable return was TERP. 

### 2018 Stocks Analysis 
*The 2018 Stock Analysis ran in 0.07 seconds. This is significantly faster than the original run time of 0.79 seconds. 
*Refactoring the original code should allow Steve to run 100 stocks in approximately 0.59 seconds. 
*Steve can input the new tickers into the array of all tickers at this point in the code: 

'Initialize array of all tickers
    Dim tickers(12) As String
    
    tickers(0) = "AY"
    tickers(1) = "CSIQ"
    tickers(2) = "DQ"
    tickers(3) = "ENPH"
    tickers(4) = "FSLR"
    tickers(5) = "HASI"
    tickers(6) = "JKS"
    tickers(7) = "RUN"
    tickers(8) = "SEDG"
    tickers(9) = "SPWR"
    tickers(10) = "TERP"
    tickers(11) = "VSLR"

*Then, Steve will simply need to update the numbers through this next section of the code to reflect the number of tickers he has added: 

'1a) Create a ticker Index
    tickerIndex = 0

    '1b) Create three output arrays
    Dim tickerVolumes(12) As Long
    Dim tickerStartingPrices(12) As Single
    Dim tickerEndingPrices(12) As Single
    
    ''2a) Create a for loop to initialize the tickerVolumes to zero.
    For i = 0 To 11
        tickerVolumes(i) = 0 

Steve and his parents should note the following information about the sustainable stocks in 2018: 

![vba_challenge_2018](https://user-images.githubusercontent.com/93888037/148706875-29beef84-60cf-4322-be77-f6fed589a1be.png)

*The majority of the sustainable stocks saw unfavorable returns in the year 2018.
*This suggests volatility in this type of stock, and that level of risk should be understood before investing. 
*The most consistently viable stock in 2017 AND 2018 was ENPH, which had a return of 129.5% in 2017 and a return of 81.9% in 2018. 
*The stock RUN was the only other stock to have a positive return in both 2017 and 2018, but the 2017 was much lower than that of ENPH at only 5.5%.

##Summary Statement 

###Advantages and Disadvantages of Refactoring Code
The major advantage to refactoring this code was to allow the program to expand with the client's needs. For example, after seeing the 2018 returns, Steve and his family may not be as comfortable investing in one of the original 12 stocks we analyzed. Since the code is refactored, Steve will be able to adjust and run a wider variety of stocks to see what other types of stocks may be more suitable for his parents' investment. The refactoring is essential for allowing Steve to expand his search much wider and include a larger data set. 

The refactored code runs much faster. This should allow Steve to run more data through the refactored code and not have to wait for that code to process. As mentioned in the 2018 analysis, running about 100 tickers should take approximately 0.59 seconds. However, running 100 tickers on the original code would take approximately 6.6 seconds. This number would only continue to grow. If we were to run the highest number of publicly listed stocks in U.S. history (7,562), the original program would take at least 8 minutes. If the refactored code continued to work at this same rate, that record-breaking
number of stocks could run in approximately 44 seconds. Speed is the major advantage of the refactored code.

However, refactoring the code was complicated. If I were to hand this project off to Steve without continued assistance, it might be difficult for Steve to adjust the code to fit his changing needs. Installing the button makes running the refactored code simple, but programming it or changing it would be complicated for someone without experience. The original code is much easier to adjust and could help Steve make changes to the code without additional help. 





