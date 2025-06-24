# Get the Current Weather for Any City

Get instant weather updates for any city worldwide. Each request provides complete **current weather** conditions: temperature, humidity, wind speed, and weather descriptions.

---

## Endpoint Summary

**HTTP Method:** `GET`  
**URL:** `https://api.openweathermap.org/data/2.5/weather`

---

## Required Parameters

| Parameter | Type   | Required | Example      | Description                                                      |
|-----------|--------|----------|--------------|------------------------------------------------------------------|
| `q`       | string | Yes   | `Lagos`      | City name (can include country code, e.g. `Lagos,NG`)            |
| `appid`   | string | Yes   | `abc123`     | Your personal API key                                            |
| `units`   | string | No       | `metric`     | Use `metric` (°C), `imperial` (°F), or leave blank for Kelvin    |
| `lang`    | string | No       | `en`         | Language of the weather description                              |

---

## 🧪 Sample Request

```bash
GET https://api.openweathermap.org/data/2.5/weather?q=Lagos&units=metric&appid=YOUR_API_KEY
 ```



## Sample Response (Shortened)

```json
{
  "weather": [{ "id":804
    "main": "Clouds",
    "description": "overcast clouds"
  }],
  "main": {
    "temp": 28.1,
    "feels_like": 31.88,
    "humidity": 77
  },
  "wind": {
    "speed":1.3,"deg":243,"gust":1.77
  },
  "name": "Lagos"
}
```
---

## Key Fields Explained
 
| Field                | Meaning                                      |
|----------------------|----------------------------------------------|
| `main.temp`          | Current temperature in specified units       |
| `main.feels_like`    | Perceived ("feels like") temperature         |
| `main.humidity`      | Humidity in %                                |
| `weather.description`| Text description like "light rain"           |
| `wind.speed`         | Wind speed in meters per second              |
| `name`               | Name of the city returned                    |


---
## Common Errors

| Code | Message        | Cause                                         |
|------|----------------|-----------------------------------------------|
| 401  | Unauthorized   | API key is missing or incorrect               |
| 404  | Not Found      | Invalid city name or location not found       |
| 429  | Too Many Calls | You’ve exceeded the API rate limit            |

---

Pro Tip

To get temperature in Celsius, add units=metric to your request.
To change language, add lang=fr for French, lang=es for Spanish. 