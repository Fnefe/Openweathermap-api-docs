# 🌦️ 5-Day / 3-Hour Forecast Endpoint

Get detailed weather forecasts in 3-hour intervals for the next 5 days.

---

## 🧭 Endpoint

```http
GET https://api.openweathermap.org/data/2.5/forecast
```
---
## 🔐 Required Parameters

| Parameter | Type   | Required | Description                                               |
|-----------|--------|----------|-----------------------------------------------------------|
| `q`       | string | ✅ Yes   | City name (e.g., `Lagos`)                                 |
| `appid`   | string | ✅ Yes   | Your API key                                              |
| `units`   | string | ❌ No    | Use `metric` for Celsius, `imperial` for Fahrenheit       |
| `lang`    | string | ❌ No    | Language code (e.g., `en`, `fr`, `es`)                    |

--- 

## 🧪 Sample Request

```HTTP
GET https://api.openweathermap.org/data/2.5/forecast?q=Lagos&units=metric&appid=YOUR_API_KEY
```

---

## 📥 Sample Response (Shortened)

```json
{
  "list": [
    {
      "dt_txt": "2025-06-24 12:00:00",
      "main": {
        "temp": 28.81,
        "feels_like": 32.2,
        "humidity": 70
      },
      "weather": [{
        "main": "Rain",
        "description": "light rain"
      }],
      "wind": {
        "speed": 3.52
      }
    },
    {
      "dt_txt": "2025-06-24 15:00:00",
      "main": {
        "temp": 26.13,
        "feels_like": 26.13,
        "humidity": 81
      },
      "weather": [{
        "main": "Clouds",
        "description": "broken clouds"
      }],
      "wind": {
        "speed": 3.07
      }
    }
    {
      "dt_txt": "2025-06-24 21:00:00",
      "main": {
        "temp": 25.09,
        "feels_like": 25.95,
        "humidity": 88
      },
      "weather": [{
        "main": "Clouds",
        "description": "overcast clouds"
      }],
      "wind": {
        "speed": 2.62
      }
    }
  ],
  "city": {
    "name": "Lagos",
    "country": "NG"
  }
}
```

--- 

## ⚠️ Common Errors

| Code | Message        | Cause                                         |
|------|----------------|-----------------------------------------------|
| 401  | Unauthorized   | API key is missing or incorrect               |
| 404  | Not Found      | Invalid city name or location not found       |
| 429  | Too Many Calls | You’ve exceeded the API rate limit            |