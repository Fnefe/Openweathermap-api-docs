# Getting Started With Open WeatherMap 
Before using any Open WeatherMap API endpoints you need to create an account and get an API key for authentication.

## Create and Open WeatherMap Account:
1. On your browser go to: https://home.openweathermap.org/users/sign_up
2.  Fill in your credentials and create an account. 
3. Confirm your email address through the verification email. 

## Get your API Key
1. Log in to: https://home.openweathermap.org/
2. Click **API Keys** in the top navigation bar
3. You'll see a default API key listed. You can rename it or click **Generate** to create a new key.
4. Copy and store the key securely.

**“Your api key is required for authentication and must be included in all your requests". If the API key is missing or invalid, the request will fail with a 401 Unauthorized error**.

**Sample request format**:

```http
https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY
```

### Base URL

All requests are made to:  
[`https://api.openweathermap.org/data/2.5/`](https://api.openweathermap.org/data/2.5/)

