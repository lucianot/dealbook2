
__Company__

`GET /v1/companies`
Get a list of companies

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "companies": [
    {
      "id": "42",
      "href": "https://api.dealbook.co/v1/companies/42",
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
      "deals": [
        {
          "id": "1234",
          "href": "https://api.dealbook.co/v1/deals/1234",
          "date": "2015-08-01",
          "type": "raised funds",
          "series": "seed",
          "investors": [
            "Monashees",
            "Redpoint e.ventures",
            "500Startups"
          ],
          "currency": "BRL",
          "amount": 3_000_000
        }
      ],
      "persons": [
        {
          "id": "1",
          "href": "https://api.dealbook.co/v1/persons/1",
          "name": "Luciano Tavares",
          "role": "CEO",
          "image": "/persons/1/mug.png"
        },
        {
          "id": "2",
          "href": "https://api.dealbook.co/v1/persons/2",
          "name": "Fabiano Beselga",
          "role": "CTO",
          "image": "/persons/2/mug.png"
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
    },
    {
      "id": "84",
      "href": "https://api.dealbook.co/v1/companies/84",
      "name": "RockContent",
      "description": "RockContent rocks!",
      "logo": "/companies/84/logo.png",
      "website": "rockcontent.com.br",
      "social_links": [
        "twitter.com/@rockcontent"
      ],
      "markets": [
        "content marketing"
      ],
      "locations": [
        "Belo Horizonte, Brazil"
      ],
      "deals": [
        {
          "id": "2345",
          "href": "https://api.dealbook.co/v1/deals/2345",
          "date": "2014-08-01",
          "type": "raised funds",
          "series": "seed",
          "investors": [
            "Napkn Ventures"
          ],
          "currency": "BRL",
          "amount": 300_000
        }
      ],
      "persons": [
        {
          "id": "34",
          "href": "https://api.dealbook.co/v1/persons/34",
          "name": "Edmar Ferreira",
          "role": "CEO",
          "image": "/persons/34/mug.png"
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

===

`GET /v1/companies/{{company_id}}`
Get a single company

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "company": {
    "id": "42",
    "href": "https://api.dealbook.co/v1/companies/42",
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
    "deals": [
      {
        "id": "1234",
        "href": "https://api.dealbook.co/v1/deals/1234",
        "date": "2015-08-01",
        "type": "raised funds",
        "series": "seed",
        "investors": [
          "Monashees",
          "Redpoint e.ventures",
          "500Startups"
        ],
        "currency": "BRL",
        "amount": 3_000_000
      }
    ],
    "persons": [
      {
        "id": "1",
        "href": "https://api.dealbook.co/v1/persons/1",
        "name": "Luciano Tavares",
        "role": "CEO",
        "image": "/persons/1/mug.png"
      },
      {
        "id": "2",
        "href": "https://api.dealbook.co/v1/persons/2",
        "name": "Fabiano Beselga",
        "role": "CTO",
        "image": "/persons/2/mug.png"
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
}
````
===

`POST /v1/companies`
Create a new company

* Required permission: write

````
{
  "company": {
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
    ]
  }
}
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "company": {
    "id": "42",
    "href": "https://api.dealbook.co/v1/companies/42",
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
    }
  }
}
````
===

`PUT /v1/companies/{{company_id}}`
Update a company

* Required permission: write

````
{
  "company": {
    "description": "Magnetis is the most awesome online advisor ever"
  }
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "company": {
    "id": "42",
    "href": "https://api.dealbook.co/v1/companies/42",
    "name": "Magnetis",
    "description": "Magnetis is the most awesome online advisor ever",
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
    }
  }
}
````
===

`DELETE /v1/companies/{{company_id}}`
Destroy a company

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
