# TXO_TX_Strategy


Member
--------------
I-Fan Chiang

Data
-------------- 
* Futures: The Nearby month Taiwan Futures from 03/13/2020 ~ 04/24/2020
* OptionOpen: The daily transaction Call and Put data in Open Interval (84500 ~ 85000) from 03/13/2020 ~ 04/24/2020
* OptionClose: The daily transaction Call and Put data in Close Interval (134000 ~ 134500) from 03/13/2020 ~ 04/24/2020
* Rate: ZCB rate from 03/13/2020 ~ 04/24/2020

Data Resorce
-------------- 
* Data resorce:    
    * Futures:  http://www.taifex.com.tw/cht/3/dlFutPrevious30DaysSalesData  
    * Options:  http://www.taifex.com.tw/cht/3/dlOptPrevious30DaysSalesData
    * Rate: TEJ


Strategy Development 
-------------- 
* Strategy1: Buy and Hold  

* Strategy2: Based on intradayCPIVchange
   * Buy @ OpenPrice_T+1 and offset at the @ closePrice_T+1 if 
       * the intradayCPIVchange is positive;  
   * Sell @ OpenPrice_T+1 and offset at the @ closePrice_T+1 if 
       * the intradayCPIVchange is negative



Performance
-------------- 
* Strategy1: 
 ![alt text](https://github.com/A2Zntu/FuturesStrategy/blob/master/Graph/BuyandHold.png "BuyandHold")

 
* Strategy2: 
 ![alt text](https://github.com/A2Zntu/FuturesStrategy/blob/master/Graph/Strategy2.png "Strategy2")



Conclusion
-------------- 
| Strategy  | HPR    | APR    | Sharp Ratio | MDD |
| ---       | ---    |   ---  |   ---  | ---    |
| Strategy1 | 0.0531 | 0.0179 | 0.0434 | -0.314 |
| Strategy2 | 0.2135 | 0.0686 | 0.5171 | -0.164 |

 



Improvement
-------------- 
* Could consider about the transaction fee and taxes
* Could use ANN or other machine learning skills to improve
