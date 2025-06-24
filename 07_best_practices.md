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
## Supported Languages

You can customize the language of weather descriptions using the `lang` query parameter. Below are the accepted values:

| Language             | Code(s)     | Language             | Code(s)     |
|----------------------|-------------|----------------------|-------------|
| Albanian             | `sq`        | Polish               | `pl`        |
| Afrikaans            | `af`        | Portuguese           | `pt`        |
| Arabic               | `ar`        | Portuguese (Brazil)  | `pt_br`     |
| Azerbaijani          | `az`        | Romanian             | `ro`        |
| Basque               | `eu`        | Russian              | `ru`        |
| Belarusian           | `be`        | Serbian              | `sr`        |
| Bulgarian            | `bg`        | Slovak               | `sk`        |
| Catalan              | `ca`        | Slovenian            | `sl`        |
| Chinese (Simplified) | `zh_cn`     | Spanish              | `sp`, `es`  |
| Chinese (Traditional)| `zh_tw`     | Swedish              | `sv`, `se`  |
| Croatian             | `hr`        | Thai                 | `th`        |
| Czech                | `cz`        | Turkish              | `tr`        |
| Danish               | `da`        | Ukrainian            | `ua`, `uk`  |
| Dutch                | `nl`        | Vietnamese           | `vi`        |
| English              | `en`        | Zulu                 | `zu`        |
| Finnish              | `fi`        | Hebrew               | `he`        |
| French               | `fr`        | Hindi                | `hi`        |
| Galician             | `gl`        | Hungarian            | `hu`        |
| German               | `de`        | Icelandic            | `is`        |
| Greek                | `el`        | Indonesian           | `id`        |
| Japanese             | `ja`        | Korean               | `kr`        |
| Kurdish (Kurmanji)   | `ku`        | Latvian              | `la`        |
| Lithuanian           | `lt`        | Macedonian           | `mk`        |
| Norwegian            | `no`        | Persian (Farsi)      | `fa`        |

> Example usage:  
> `https://api.openweathermap.org/data/2.5/weather?q=Lagos&lang=fr&appid=YOUR_API_KEY`  
> Returns weather description in **French**

---

## Unit Preferences

Customize the unit of measurement for temperature, wind speed, and more using the `units` query parameter.

---

### Supported Unit Systems

| Unit System | Query Value | Temperature    | Wind Speed   |
|-------------|-------------|----------------|--------------|
| Standard    | `standard`  | Kelvin (K)     | meter/sec    |
| Metric      | `metric`    | Celsius (°C)   | meter/sec    |
| Imperial    | `imperial`  | Fahrenheit (°F)| miles/hour   |


> Example:  
> `https://api.openweathermap.org/data/2.5/weather?q=Abuja&units=metric&appid=YOUR_API_KEY`  
> Returns temperature in **Celsius** and wind speed in **meters per second**.

> Tip: Combine `units=metric` with `lang=fr` for fully localized responses.

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