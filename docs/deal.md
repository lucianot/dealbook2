
__Deal__

`GET /1/deals.json`
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
      "date": "2015-08-01",
      "type": "raised funds",
      "series": "seed",
      "currency": "BRL",
      "amount": 3_000_000,
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
      },
      "investors": [
        {
          "id": "1001",
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
          "name": "Redpoint e.ventures",
          "description": "Redpoint is a VC",
          "logo": "/investors/1002/logo.png",
          "website": "rpev.com.br",
          "social_links": [
            "twitter.com/@rpev"
          ]
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
      ...
    }
  ]
}
````

===

`GET /1/deals/{{deal_id}}.json`
Get a single deal

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "deal": {
    "id": "1234",
    "date": "2015-08-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
    "company": {
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
      ]
    },
    "investors": [
      {
        "id": "1001",
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
        "name": "Redpoint e.ventures",
        "description": "Redpoint is a VC",
        "logo": "/investors/1002/logo.png",
        "website": "rpev.com.br",
        "social_links": [
          "twitter.com/@rpev"
        ]
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

`POST /1/deals.json`
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
    "date": "2015-08-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
    "company": {
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
      ]
    },
    "investors": [
      {
        "id": "1001",
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
        "name": "Redpoint e.ventures",
        "description": "Redpoint is a VC",
        "logo": "/investors/1002/logo.png",
        "website": "rpev.com.br",
        "social_links": [
          "twitter.com/@rpev"
        ]
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
    }
  }
}
````
===

`PUT /1/deals/{{deal_id}}.json`
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
    "date": "2015-09-01",
    "type": "raised funds",
    "series": "seed",
    "currency": "BRL",
    "amount": 3_000_000,
    "company": {
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
      ]
    },
    "investors": [
      {
        "id": "1001",
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
        "name": "Redpoint e.ventures",
        "description": "Redpoint is a VC",
        "logo": "/investors/1002/logo.png",
        "website": "rpev.com.br",
        "social_links": [
          "twitter.com/@rpev"
        ]
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
    }
  }
}
````
===

`DELETE /1/deals/{{deal_id}}.json`
Destroy a deal

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
