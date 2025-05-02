## Weather API Request Using Postman

### Request Details
 **Endpoint:** `https://api.weatherbit.io/v2.0/current`
 **Query Parameters:**
`city`: London
 `key`:84090c50cd54400cb7b8c23e06f06391

### Response Summary
**City**: London
**Temperature**: 11.7°C
 **Weather Description**: Clear sky
 **Status Code**: 200 OK

### Reflection on Query Parameters

Correct usage of query parameters is crucial when working with APIs. They define the input for the request (e.g., which city’s weather you want) and authenticate access (via the API key). Mistakes like a misspelled parameter name or missing API key often lead to errors or empty responses. Understanding how to structure these parameters helps ensure accurate and successful API calls.

## Weather API Collection - Postman Assignment

### Collection & Environment Setup
 Created a collection named **Weather API Collection** to store related requests.
 Created an environment called **Weather API Environment**.
 Added a variable named `weatherApiKey` to securely store and reuse the API key.

### Request Setup
 Each request was configured to use the variable:
`key={{weatherApiKey}}`
 Requests were sent to the endpoint:
`https://api.weatherbit.io/v2.0/current`
 Query parameter used: `city` with values like New York, Tokyo, and London.

### Example Request: GET https://api.weatherbit.io/v2.0/current?city=London&key={{weatherApiKey}}

### Benefits of Variables
 Centralized key management.
 Makes request templates reusable for any environment or user.
 Secure: API key isn't hardcoded into each request.

### Sample Response
```json
{
"data": [
{
"city_name": "London",
"temp": 23.8,
"weather": {
"description": "Broken clouds"
}
}
]
}