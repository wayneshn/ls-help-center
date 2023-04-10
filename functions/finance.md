# Finance

The finance functions of Logic Sheet rely on the Alpha Vantage database, which is a free financial information provider. In order to use Logic Sheet to retrieve finance data such as real-time share prices or currency exchange rates, you have to gain an Alpha Vantage API key. The API key is provided completely free and it only takes you less than one minute to register. You can use the API key repeatedly.

Get the API Key here: [https://www.alphavantage.co/support/#api-key](https://www.alphavantage.co/support/#api-key)

### Alpha Vantage API Key

Type in and save your Alpha Vantage API key here so that you don’t have to type it every time you use a Finance function.

Get the API Key here: https://www.alphavantage.co/support/#api-key

### Get share prices

This function allows you to retrieve the share price data of a given company.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

**API key:** This function relies on the Alpha Vantage API for information. You will need to get a free Alpha Vantage API key first to use this function.

Get the API Key here: https://www.alphavantage.co/support/#api-key

**Data type:** Select the time interval of the share price to retrieve.

* “Intraday means “within the day.” In the financial world, the term is shorthand used to describe securities that trade on the markets during regular business hours.” – Investopedia

**Interval for intraday data:** Time interval between two consecutive data points in the time series.

**Stock symbol:** The name of the equity of your choice. Example: IBM, APPL, GOOGL. (One symbol each time)

### Fundamental information

This function allows you to retrieve fundamental-data information of a given company such as cash flow, earnings, and balance sheet.

**API key:** This function relies on the Alpha Vantage API for information. You will need to get a free Alpha Vantage API key first to use this function.

Get the API Key here: https://www.alphavantage.co/support/#api-key

**Data type:**

* Company overview. This type returns the company information, financial ratios, and other key metrics for the equity specified. Data is generally refreshed on the same day a company reports its latest earnings.
* Income statement. This type returns the annual and quarterly income statements for the equity specified. Data is generally refreshed on the same day a company reports its latest earnings.
* Balance sheet. This type returns the annual and quarterly balance sheets for the equity specified. Data is generally refreshed on the same day a company reports its latest earnings.
* Cash flow. This type returns the annual and quarterly cash flows for the equity specified. Data is generally refreshed on the same day a company reports its latest earnings.
* Earnings. This type returns the annual and quarterly earnings (EPS) for the equity specified. Quarterly data also includes analyst estimates and surprise metrics.

**Stock symbol:** The name of the equity of your choice. For example: IBM, APPL, GOOGL. (One symbol each time)

### Forex rates

This function allows you to retrieve the foreign exchange rates between two given currencies.

**API key:** This function relies on the Alpha Vantage API for information. You will need to get a free Alpha Vantage API key first to use this function.

Get the API Key here: https://www.alphavantage.co/support/#api-key

**Data type:** Select the time interval of exchange rates to retrieve.

* “Intraday means “within the day.” In the financial world, the term is shorthand used to describe securities that trade on the markets during regular business hours.” – Investopedia

**Interval for intraday data:** Time interval between two consecutive data points in the time series.

**From currency:** A three-letter symbol from the [supported currency list](https://docs.logicsheet.co/attachment/supported-currencies#supported-physical-currencies). For example: EUR.

**To currency:** A three-letter symbol from the [supported currency list](https://docs.logicsheet.co/attachment/supported-currencies#supported-physical-currencies). For example: USD.

### Cryptocurrency rates

This function allows you to retrieve exchange rates of a given cryptocurrency in a given market.

**API key:** This function relies on the Alpha Vantage API for information. You will need to get a free Alpha Vantage API key first to use this function.

Get the API Key here: https://www.alphavantage.co/support/#api-key

**Data type:** Select the time interval of exchange rates to retrieve.

**Crypto symbol:** The symbol of digital/cryptocurrency. It can be any of the currencies in the [supported cryptocurrency list](https://docs.logicsheet.co/attachment/supported-currencies#supported-cryptocurrencies). For example: BTC.

**Market:** The exchange market of your choice. It can be any of the currency in the [physical currency list](https://docs.logicsheet.co/attachment/supported-currencies#supported-cryptocurrencies). For example: SGD means the Singaporean market.\
