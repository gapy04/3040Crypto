## API description

## Endpoints
### Getting Trends
Description: Gets the market trends for the provided date range.  
Endpoint: `/trends`  
Method: `GET`  
Parameters:  
- start-date: datetime   
- end-date: datetime

Success response:
```
{
  message: "success",
  trends: {
    peak-date: 02-11-2024,
    peak-value: 1200,
    lowest-date: 01-13-2024,
    lowest-value: 200
  }
}
```

### Check Currency
Description: Check how much currency you have.
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


### Sample request and response

Endpoint: `/trends`  
Sample request: ```https://3040Crypto.com/currency/trends?start-date="01-10-2024"&end-date="03-14-2024"```  
Sample response:
```
{
  message: "success",
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
