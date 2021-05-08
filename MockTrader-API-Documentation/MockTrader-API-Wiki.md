# MockTrader API WIKI

[Back to home](../README.md)



### Companies

- [`GET` /companies](./Collections/MockTrader_Wiki_Companies.md#Get-companies) : Get all companies in MockTrader catalog
- [`GET` /companies/:companyId](./Collections/MockTrader_Wiki_Companies.md#Get-company-by-Id) : Get one company
- [`POST` /companies](./Collections/MockTrader_Wiki_Companies.md#Add-company-to-catalog) : Add a new company to catalog by ticker aggregate (admin only)
- [`PATCH` /companies/:companyId](./Collections/MockTrader_Wiki_Companies.md#Modify-company) : Modify info for an existing company in catalog (admin only)
- [`DELETE` /companies/:companyId](./Collections/MockTrader_Wiki_Companies.md#Delete-company-from-catalog) : Remove a company from catalog (admin only)



### Orders

- [`GET` /users/:userId/orders](./Collections/MockTrader_Wiki_Orders.md#Get-all-orders-for-user) : Get full order history for user
- [`GET` /users/:userId/portfolios/:portfolioId/orders](./Collections/MockTrader_Wiki_Orders.md#Get-all-orders-for-portfolio) : Get all orders in a given portfolio for user
- [`POST` /users/:userId/portfolios/:portfolioId/orders](./Collections/MockTrader_Wiki_Orders.md#Create-new-order) : Create new order for user
- [`POST` /users/:userId/orders/:orderId/cancel](./Collections/MockTrader_Wiki_Orders.md#Cancel-order) : Cancel a pending order



### Portfolios

- [`GET` /users/:userId/portfolios](./Collections/MockTrader_Wiki_Portfolios.md#Get-all-portfolios-for-user) : Get all portfolios for user
- [`GET` /users/:userId/portfolios/:portfolioId](./Collections/MockTrader_Wiki_Portfolios.md#Get-portfolio-by-Id) : Get one portfolio
- [`POST` /users/:userId/portfolios](./Collections/MockTrader_Wiki_Portfolios.md#Create-new-portfolio) : Create new portfolio
- [`PATCH` /users/:userId/portfolios/:portfolioId](./Collections/MockTrader_Wiki_Portfolios.md#Modify-portfolio) : Modify existing portfolio
- [`DELETE` /users/:userId/portfolios/:portfolioId](./Collections/MockTrader_Wiki_Portfolios.md#Delete-portfolio) : Delete existing portfolio



### Positions

- [`GET` /users/:userId/positions](./Collections/MockTrader_Wiki_Positions.md#Get-all-positions-for-user) : Get all positions for user
- [`GET` /users/:userId/positions/:portfolioId](./Collections/MockTrader_Wiki_Positions.md#Get-positions-in-portfolio) : Get all positions in given portfolio



### Stocks

- [`GET` /stocks](./Collections/MockTrader_Wiki_Stocks.md#Get-all-stocks) : Get all available stocks in MockTrader catalog
- [`GET` /stocks/:tickerAggregate](./Collections/MockTrader_Wiki_Stocks.md#Get-stock-by-ticker-aggregate) : Refresh and get stock data with ticker aggregate 
- [`GET` /stocks/analytics/:tickerAggregate?period=period](./Collections/MockTrader_Wiki_Stocks.md#Get-stock-analytics) : Refresh and get stock analytics for ticker aggregate and given period
- [`POST` /stocks](./Collections/MockTrader_Wiki_Stocks.md#Add-new-stock-to-catalog) : Add new stock to catalog (admin only)
- [`DELETE` /stocks/:tickerAggregate](./Collections/MockTrader_Wiki_Stocks.md#Remove-stock-from-catalog) : Delete stock from catalog (admin only)



### Transactions

- [`GET` /users/:userId/transactions](./Collections/MockTrader_Wiki_Transactions.md#Get-all-transactions-for-user) : Get full transaction history for user
- [`GET` /users/:userId/portfolios/:portfolioId/transactions](./Collections/MockTrader_Wiki_Transactions.md#Get-transactions-in-portfolio) : Get transaction history for portfolio
- [`POST` /users/:userId/portfolios/:portfolioId/transactions](./Collections/MockTrader_Wiki_Transactions.md#Create-new-transaction) : Create new transaction in portfolio



### Users

- [`GET` /users](./Collections/MockTrader_Wiki_Users.md#Get-all-users) : Get basic info for all users (admin only)
- [`GET` /users/:userId](./Collections/MockTrader_Wiki_Users.md#Get-user-by-Id) : Get info for user
- [`POST` /users](./Collections/MockTrader_Wiki_Users.md#Create-use) : Create new user
- [`PATCH` /users/:userId](./Collections/MockTrader_Wiki_Users.md#Modify-user) : Modify existing user
- [`DELETE` /users/:userId](./Collections/MockTrader_Wiki_Users.md#Delete-user) : Delete existing user



### Watchlists

- [`GET` /users/:userId/watchlist](./Collections/MockTrader_Wiki_Watchlists.md#Get-user-watchlist) : Get all stocks in user watchlist
- [`POST` /users/:userId/watchlist](./Collections/MockTrader_Wiki_Watchlists.md#Create-new-transaction) : Add stock to user watchlist
- [`DELETE` /users/:userId/watchlist/:stockTickerAggregate](./Collections/MockTrader_Wiki_Watchlists.md#Remove-stock-from-watchlist) : Remove stock from user watchlist



### Authentication

- [`POST` /auth/login](./Collections/MockTrader_Wiki_Authentication.md#Login) : Get temporary Auth Token for user credentials
- [`DELETE` /auth/logout](./Collections/MockTrader_Wiki_Authentication.md#Logout) : Invalidate Auth Token



### Emails

- [`GET` /accounts/confirm/:userId](./Collections/MockTrader_Wiki_Emails.md#Confirm-account) : Confirm user email
- [`POST` /accounts/reset/:userEmail](./Collections/MockTrader_Wiki_Emails.md#Request-password-reset-email) : Request password reset email
- [`GET` /accounts/reset/:userEmail/:resetId](./Collections/MockTrader_Wiki_Emails.md#Reset-password) : Access password reset resource



### Admin

[(In development)](./Collections/MockTrader_Wiki_Admin.md#Admin)

