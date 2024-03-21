## API description
The API for 3040Crypto allows users to access market trends and their account information. It also allows users to find out which currency is trending. They can check which date the currency peaked/plummetted and the value of the currency at those times.

## Endpoints
### Getting Trends
Description: Gets the market trends for most popular currency in the provided date range.  
Endpoint: `/trends`  
Method: `GET`  
Parameters:  
- start-date: datetime   
- end-date: datetime

Success response:
```
{
  message: "success",
  currency-type: MOST_POPULAR_CURRENCY_NAME,
  trends: {
    peak-date: PEAK_DATE,
    peak-value: HIGHEST_CURRENCY_VALUE,
    lowest-date: LOWEST_DATE,
    lowest-value: LOWEST_CURRENCY_VALUE
  }
}
```

### Check Currency Amount
Description: Checks how much of a currency type you have.  
Endpoint: `/currency`  
Method: `GET`  
Parameters:  
- username: string
- currency-type: string

Success response:
```
{
  message: "success",
  type: CURRENCY_TYPE,
  amount: CURRENCY_COUNT
}
```

## Resources
### Trend Object
```
{
  currency-type: string,
  peak-date: datetime,
  peak-value: integer,
  lowest-date: datetime,
  lowest-value: integer
}
```
### UserDetails Object
```
{
  username: string,
  email: string,
  phone-number: string,
  country: string,
  two-factor-auth: boolean,
  date-registered: datetime,
  currency: {
    string: integer
  }
}
```
## Sample request and response

Endpoint: `/trends`  
Sample request: ```https://3040Crypto.com/currency/trends?start-date="01-10-2024"&end-date="03-14-2024"```  
Sample response:
```
{
  message: "success",
  currency-type: "bitcoin",
  trends: {
    peak-date: 02-11-2024,
    peak-value: 1200,
    lowest-date: 01-13-2024,
    lowest-value: 200
  }
}
```

Endpoint: `/currency`  
Sample request: ```https://3040Crypto.com/currency/JohnDoe/bitcoin```  
Sample response:
```
{
  message: "success",
  type: "bitcoin",
  amount: 1000
}
```
