# Best Practices & Use Cases


##  Best Practices

- **Secure Your API Key**  
  Never expose your API key in public code or client-side applications. Use environment variables or a backend proxy.

- **Use Units and Language Parameters**  
  For better user experience, set `units=metric` for Celsius or `imperial` for Fahrenheit. Set `lang=xx` to localize descriptions.

- **Implement Caching**  
  Store frequently requested data temporarily to reduce API calls and improve performance.

- **Handle Errors Gracefully**  
  Always check HTTP status codes in your app and provide meaningful error messages to users.

- **Avoid Excessive Requests**  
  Be mindful of rate limits. Avoid polling the API too often unless you’re on a plan that supports it.

---

## Use Cases

| Use Case                                      | Endpoint(s) Used             |
|----------------------------------------------|------------------------------|
| Displaying current weather in a dashboard     | `current weather`            |
| Forecasting for travel or events              | `5-day / 3-hour forecast`     |
| Mobile weather apps or browser extensions     | All 2                        |
| Classroom or bootcamp API training exercises  | `current` + `forecast`       |

---

By following these practices and structuring requests thoughtfully, you ensure better performance, cleaner code, and a more reliable user experience.