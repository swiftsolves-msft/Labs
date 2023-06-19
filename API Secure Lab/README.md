# API Attack Testing Lab Environment
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FLabs%2Fmaster%2FAPI%20Attack%20Lab%azuredeploy.json)


This ARM deployment includes everything needed to test Defender for API components.

- A Docker image of [VAmPI](https://github.com/erev0s/VAmPI) running in a Azure Container Instance on port: 5000
- Azure API Management Service

## Post Deployment Steps:

1. Ensure Defender for API is turned on
2. Download the [openapi3.json](https://raw.githubusercontent.com/swiftsolves-msft/Labs/main/API%20Secure%20Lab/openapi3.json) file locally
3. Open APIM Service, APIs blade, + Add API, Create from definition OpenAPI... ![addapidef](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/addapidef.png)
4. Load the openapi3.json, switch to full, ensure URL scheme is HTTP, Under Products add Starter & Unlimited and press Create![loadopenspec.png](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/loadopenspec.png)
5. You should now see VAmPI under APIs with 13 defined  operations ![apiops.png](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/apiops.png)
6. Click on the Settings tab, Update Web Service URL to include the http:// of the Azure Container Instance Public IP deployed with :5000 example: *http://containerpip:5000* , Uncheck Subscription required for testing with the API through APIM, and Save![updateset.png](https://github.com/swiftsolves-msft/Labs/raw/main/API%20Secure%20Lab/images/updateset.png)
7. instructions pending

## Links:
Checkout VAmPI Blogs [here](https://erev0s.com/blog/vampi-vulnerable-api-security-testing/) and [here](https://erev0s.com/blog/vampi-against-automated-api-scanning/) for more information on the API itself