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

Finally we will retrieve the specific book title API again we will need to update the Authorization to the Bearer Token, and in the URI put in and replace the book title, be sure not to pass in ':'![retrievebook](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/retrievebook.png) 

## Defender for API Enable and Enroll:

1. Ensure Defender for API is turned on - Defender for Cloud, Environment Settings, select Azure Subscription, Defender Plans, turn on APIs, and Save.![defapiplan](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/defapiplan.png)
2. Click on Recommendations, search for *Azure API Management APIs should be onboarded to Defender for APIs* , confirm unhealthy API Collections, and click on recommendation ***may take +30 minutes**![onboardapi1](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/onboardapi1.png)
3. Check both APIs vampi, and echo-api, click Fix , click Fix 2 resources![onboardapi3](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/onboardapi2.png)  ![onboardapi2](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/onboardapi3.png) ![onboardapi4](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/onboardapi4.png)
