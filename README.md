# Product-Hunt Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Product-Hunt Scraper](https://oxylabs.io/products/scraper-api/web/producthunt?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Product-Hunt website effortlessly. This brief guide explains how an Product-Hunt Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Product-Hunt results by providing your own URLs to our service. We can return the HTML for any Product-Hunt page you like.

#### Python code example

The example below illustrates how you can get HTML of Product-Hunt page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.producthunt.com/topics/productivity'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/product-hunt-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><title> The Best Productivity Apps and P ... </html>",
      "created_at": "2023-12-18 11:12:21",
      "updated_at": "2023-12-18 11:12:22",
      "page": 1,
      "url": "https://www.producthunt.com/topics/productivity",
      "job_id": "7142471646333449217",
      "status_code": 200
    }
  ]
}
```
With our Product-Hunt Scraper, you're empowered to seamlessly glean public data from any Product-Hunt page. Easily gather desired product details including tech specs, user reactions, and upvote count, to keep yourself updated on the latest trends and stay cognizant of your industry peers. Should you require assistance, our stellar support team is available via live chat or you can reach us at hello@oxylabs.io.