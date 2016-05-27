
__Search__

`GET /1/search.json`
Get information about companies, investors or persons that match a keyword string.

* Required permission: read
* Arguments:
    + `q`: search query's keywords (required)
    + `type`: comma-separated list of item types to search across.
              Valid types are: company, investor, person (default: all)
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "companies": [
    {
      "id": "42",
      "name": "Magnetis",
      "description": "Magnetis is the best online advisor ever",
      "logo": "/companies/42/logo.png",
      "website": "magnetis.com.br",
      "social_links": [
        "twitter.com/@magnetis"
      ],
      "markets": [
        "financial services",
        "advisor"
      ],
      "locations": [
        "São Paulo, Brazil"
      ],
      "created": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 42,
        "name": "Diego Gomes",
        "image": "/persons/42/mug.png"
      },
      "modified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 48,
        "name": "Elon Musk",
        "image": "/persons/48/mug.png"
      },
      "verified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id": "42",
        "name": "Diego Gomes",
        "image": "/persons/42/mug.png"
      }
    }
  ],
  "investors": [
    {
      "id": "1001",
      "name": "Monashees Capital",
      "description": "Monashees is a VC",
      "logo": "/investors/1001/logo.png",
      "website": "monashees.com.br",
      "social_links": [
        "twitter.com/@monashees"
      ],
      "markets": [
        "fintech",
        "e-commerce",
        "saas"
      ],
      "locations": [
        "São Paulo, Brazil"
      ],
      "created": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 42,
        "name": "Diego Gomes",
        "image": "/persons/42/mug.png"
      },
      "modified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 48,
        "name": "Elon Musk",
        "image": "/persons/48/mug.png"
      },
      "verified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id": "42",
        "name": "Diego Gomes",
        "image": "/persons/42/mug.png"
      }
    }
  ],
  "persons": [
    {
      "id": "1",
      "name": "Luciano Tavares",
      "image": "/persons/1/mug.png",
      "website": "napkn.co",
      "social_links": [
        "twitter.com/@lucianot"
      ],
      "companies": [
        {
          "id": "42",
          "name": "Magnetis",
          "role": "CEO"
        }
      ],
      "investors": [
        {
          "id": "1000",
          "name": "Napkn Ventures",
          "role": "partner"
        }
      ],
      "created": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 42,
        "name": "Diego Gomes",
        "image": "/persons/42/mug.png"
      },
      "modified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 48,
        "name": "Elon Musk",
        "image": "/persons/48/mug.png"
      },
      "verified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id": "42",
        "name": "Diego Gomes",
        "image": "/persons/42/mug.png"
      }
    }
  ]
}
````
