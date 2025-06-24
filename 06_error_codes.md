# 🚨 Error Codes & Troubleshooting

## ⚠️ Common Error Responses

| Code | Message        | Cause                                                        | Solution                                                              |
|------|----------------|---------------------------------------------------------------|-----------------------------------------------------------------------|
| 400  | Bad Request    | Malformed request syntax or missing required parameters       | Check for typos and ensure all required query parameters are present  |
| 401  | Unauthorized   | API key is missing, invalid, or restricted                   | Confirm your API key is correct and active                            |
| 403  | Forbidden      | API access restricted (e.g. using a paid-only endpoint)       | Use a supported endpoint or upgrade your plan                         |
| 404  | Not Found      | The location or resource could not be found                  | Verify the city name or coordinates in your request                   |
| 429  | Too Many Calls | Rate limit exceeded (too many requests in a short time)       | Wait before making more requests or upgrade your account              |
| 500  | Server Error   | OpenWeatherMap's server had an internal error                 | Retry the request later                                               |

---

## 🧰 Troubleshooting Tips

- **Double-check your endpoint**: Make sure you're using the correct path (e.g. `/data/2.5/weather`)

- **Verify your parameters**: Ensure all required parameters (`q`, `appid`, etc.) are included

- **Watch for typos**: Especially in the city name or URL format

- **Respect rate limits**: Too many requests can lead to temporary blocks

- **Check plan access**: Some endpoints (like historical data) require a paid subscription.

