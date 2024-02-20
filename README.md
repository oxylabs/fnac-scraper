# Fnac Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Fnac Scraper](https://oxylabs.io/products/scraper-api/ecommerce/fnac?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Fnac website effortlessly. This brief guide showcases how Fnac Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Fnac results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Fnac page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.fnacspectacles.com/?utm_campaign=onglet&utm_medium=text&utm_source=fnac.com&utm_term=billetterie'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/fnac-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n\n\n\n\n<!DOCTYPE html>\n<html lang=\"fr\" dir=\"ltr\">\n<head>\n<meta charset=\"utf-8\">\n<meta name=\"viewport\"  ... </html>",
      "created_at": "2024-02-20 12:46:34",
      "updated_at": "2024-02-20 12:46:40",
      "page": 1,
      "url": "https://www.fnacspectacles.com/?utm_campaign=onglet&utm_medium=text&utm_source=fnac.com&utm_term=billetterie",
      "job_id": "7165688182128775169",
      "status_code": 200
    }
  ]
}
```
With our Fnac Scraper, you can effortlessly extract public data from any Fnac web page. Gather valuable information about your favorite books, movies or gadgets, like their prices, customer reviews, and detailed descriptions, to keep a close eye on the market trends. For any queries or concerns, feel free to get in touch with our support team through live chat or email us at hello@oxylabs.io.