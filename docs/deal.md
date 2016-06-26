
__Deal__

`GET /v1/deals`
Get a list of deals

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "deals": [
    {
      "id": "1234",
      "href": "https://api.dealbook.co/v1/deals/1234",
      "date": "2015-08-01",
      "type": "raised funds",
      "series": "seed",
      "currency": "BRL",
      "amount": 3_000_000,
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
        ]
      },
      "investors": [
        {
          "id": "1001",
          "href": "https://api.dealbook.co/v1/investors/1001",
          "name": "Monashees Capital",
          "description": "Monashees is a VC",
          "logo": "/investors/1001/logo.png",
          "website": "monashees.com.br",
          "social_links": [
            "twitter.com/@monashees"
          ]
        },
        {
          "id": "1002",
          "href": "https://api.dealbook.co/v1/investors/1002",
          "name": "Redpoint e.ventures",
          "description": "Redpoint is a VC",
          "logo": "/investors/1002/logo.png",
          "website": "rpev.com.br",
          "social_links": [
            "twitter.com/@rpev"
          ]
        }
      ],
      "source_urls": [
        "http://g1.com.br/magnetis-capta-rodada"
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
      ...
    }
  ]
}
````

===

`GET /v1/deals/{{deal_id}}`
Get a single deal

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "deal": {
    "id": "1234",
    "href": "https://api.dealbook.co/v1/deals/1234",
    "date": "2015-08-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
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
      ]
    },
    "investors": [
      {
        "id": "1001",
        "href": "https://api.dealbook.co/v1/investors/1001",
        "name": "Monashees Capital",
        "description": "Monashees is a VC",
        "logo": "/investors/1001/logo.png",
        "website": "monashees.com.br",
        "social_links": [
          "twitter.com/@monashees"
        ]
      },
      {
        "id": "1002",
        "href": "https://api.dealbook.co/v1/investors/1002",
        "name": "Redpoint e.ventures",
        "description": "Redpoint is a VC",
        "logo": "/investors/1002/logo.png",
        "website": "rpev.com.br",
        "social_links": [
          "twitter.com/@rpev"
        ]
      }
    ],
    "source_urls": [
      "http://g1.com.br/magnetis-capta-rodada"
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

`POST /v1/deals`
Create a new deal

* Required permission: write

````
{
  "deal": {
    "date": "2015-08-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
    "company_id": "42",
    "investor_ids": [
      "1001",
      "1002"
    ],
    "source_urls": [
      "http://g1.com.br/magnetis-capta-rodada"
    ]
  }
}
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "deal": {
    "id": "1234",
    "href": "https://api.dealbook.co/v1/investors/1234",
    "date": "2015-08-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
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
      ]
    },
    "investors": [
      {
        "id": "1001",
        "href": "https://api.dealbook.co/v1/investors/1001",
        "name": "Monashees Capital",
        "description": "Monashees is a VC",
        "logo": "/investors/1001/logo.png",
        "website": "monashees.com.br",
        "social_links": [
          "twitter.com/@monashees"
        ]
      },
      {
        "id": "1002",
        "href": "https://api.dealbook.co/v1/investors/1002",
        "name": "Redpoint e.ventures",
        "description": "Redpoint is a VC",
        "logo": "/investors/1002/logo.png",
        "website": "rpev.com.br",
        "social_links": [
          "twitter.com/@rpev"
        ]
      }
    ],
    "source_urls": [
      "http://g1.com.br/magnetis-capta-rodada"
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

`PUT /v1/deals/{{deal_id}}`
Update a deal

* Required permission: write

````
{
  "deal": {
    "date": "2015-09-01"
  }
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "deal": {
    "id": "1234",
    "href": "https://api.dealbook.co/v1/deals/1234",
    "date": "2015-09-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
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
      ]
    },
    "investors": [
      {
        "id": "1001",
        "href": "https://api.dealbook.co/v1/investors/1001",
        "name": "Monashees Capital",
        "description": "Monashees is a VC",
        "logo": "/investors/1001/logo.png",
        "website": "monashees.com.br",
        "social_links": [
          "twitter.com/@monashees"
        ]
      },
      {
        "id": "1002",
        "href": "https://api.dealbook.co/v1/investors/1002",
        "name": "Redpoint e.ventures",
        "description": "Redpoint is a VC",
        "logo": "/investors/1002/logo.png",
        "website": "rpev.com.br",
        "social_links": [
          "twitter.com/@rpev"
        ]
      }
    ],
    "source_urls": [
      "http://g1.com.br/magnetis-capta-rodada"
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

`DELETE /v1/deals/{{deal_id}}`
Destroy a deal

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
