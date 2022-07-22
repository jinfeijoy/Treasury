# Bank Treasury

* Structure
  * Asset Management (interest rate impact)
  * Liquidity 
  * Securilization (rise funding, e.g. GIC/Wholesale Market notes/etc.)
    * big bank mortgage rate low reason: becase big bank funding cost is low, they can rise money with lower interest cost 
  * Cash Management (cash flow forecasting) (cash operation)
    * there is a liquidity pool
    * small individual org cash movement (for each small individual org cash forecasting, need around 4~5% buffer)
    * consolidate all info from all entities to liquidity pool
    * for example, bank cash flow forecasting, there are 2 part: 
      * fixed term (fixed transactions each month, we don't need to predict this)
      * rest random part (it is stable for bank, so using rolling average to estimate)
      * for simple like bank, maybe simple rolling average / time series will work well
    * for other org with more complicated function, the cash flow might be unpredictable with simple time series, we may think about poisson distribution
    * For cash flow, there are 2 part: 
      * In: outgoing transfer from liquidity pool to org banking account
      * Out: outgoing transfer from org banking account to liquidity pool

* Projects
  * potential client level model -- Dement Deposit Forecasting
    * e.g. product ISA (investment saving account), this product volatility is very high, for example if we have 1M deposit, we can only use 50% of money to fund. 
    * in this forecasting, we need to forecast future 3M liquidity and funding
    * data: client level transaction, features like promotion, product type, dealer info, etc. (all client level details)
    * otherthing to monitor/thinking: 
      * how other institution interest impact our portfolio 
      * amount movement
      * large GIC maturity
      * etc. 
