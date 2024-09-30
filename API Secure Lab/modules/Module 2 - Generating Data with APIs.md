# Module 2 - Generating Data with APIs

### Avg Test Time: 20 mins

## Script based interaction with APIs

## Manual interaction with APIs

### Using APIM API test

### Using Postman

Within Vampi API you can click ... elpises and export a Swagger file for Postman to import![exportdefinapim](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/exportdefinapim.png)

Save the file![exportdefinapim2](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/exportdefinapim2.png)

Within Postman application Collections Import the swagger file![importdefpostman](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/importdefpostman.png)

While unauthenticaed we will retrieve all the books in vampi![retrivebookspostman](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/retrivebookspostman.png) 

Create a new login so you can get a bearer token to authenticate against future APIs![generateuserpostman](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/generateuserpostman.png) 

Login with the user/password created to obtain bearer token, be sure to copy the 'auth_token' value from the response![logintogettoken](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/logintogettoken.png) 

Next go to the API 'Add a New Book' switch the tab to Authorization and drop down to beaer and put in the copied value from above![auth](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/auth.png) 

Switch to the body tab and create a new book title for the secret use [CCGenerator](https://randommer.io/Card) and place in secret and send the request![addabook](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/addabook.png) 

an example of the json payload to create the book could be:
```{
  "book_title": "visa",
  "secret": "4935327716890354,05/2029,456,Joud Heron,8357"
}```

Finally we will retrieve the specific book title API again we will need to update the Authorization to the Bearer Token, and in the URI put in and replace the book title, be sure not to pass in ':'![retrievebook](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/retrievebook.png) 
