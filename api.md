## API description

## Endpoints
### Login
Description: Authenticates users into the system.  
Endpoint: /login  
Method: `POST`  
Parameters:  
- username: string
- password: string  
Success response:
```
{
  message: "success",
  username: USERNAME
}
```

### Check Currency
Description: Checks how much currency you have.  
Endpoint: /currency  
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

## Sample request
