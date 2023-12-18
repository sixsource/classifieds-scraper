# Classifieds Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Classifieds Scraper](https://oxylabs.io/products/scraper-api/web/classifieds-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any Classifieds website effortlessly. This brief guide explains how a Classifieds Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Classifieds results by providing your own URLs to our service. We can return the HTML for any Classifieds page you like.

#### Python code example

The example below illustrates how you can obtain Craigslist classifieds HTML results.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://newyork.craigslist.org/search/ata#search=1~gallery~0~0'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/classifieds-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html>\n<head>\n    \n\t<meta charset=\"UTF-8\">\n\t<meta http-equiv=\"X-UA-Compatible\" conte ... </html>",
      "created_at": "2023-12-18 11:34:01",
      "updated_at": "2023-12-18 11:34:02",
      "page": 1,
      "url": "https://newyork.craigslist.org/search/ata#search=1~gallery~0~0",
      "job_id": "7142477098865715201",
      "status_code": 200
    }
  ]
}
```
With our Classifieds Scraper, you can seamlessly gather public data from any Classifieds web page. Collect vital real estate information like property prices, locality reviews, and property descriptions to understand the property market better and outsmart your competitors. If you need assistance, feel free to interact with our support team through live chat or email us at hello@oxylabs.io.
