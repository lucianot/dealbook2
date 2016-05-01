# dealbook2
Dealbook 2.0

__Company__

`GET /1/companies.json`
Get a list of companies

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "object": "list",
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
      "deals": [
        {
          "id": "1234",
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
      "people": [
        {
          "id": "1",
          "name": "Luciano Tavares",
          "role": "CEO",
          "image": "/people/1/mug.png"
        },
        {
          "id": "2",
          "name": "Fabiano Beselga",
          "role": "CTO",
          "image": "/people/2/mug.png"
        }
      ],
      "created": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 42,
        "name": "Diego Gomes",
        "image": "/people/42/mug.png"
      },
      "modified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 48,
        "name": "Elon Musk",
        "image": "/people/48/mug.png"
      },
      "verified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id": "42",
        "name": "Diego Gomes",
        "image": "/people/42/mug.png"
      }
    },
    {
      "id": "84",
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
      "people": [
        {
          "id": "34",
          "name": "Edmar Ferreira",
          "role": "CEO",
          "image": "/people/34/mug.png"
        }
      ],
      "created": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 42,
        "name": "Diego Gomes",
        "image": "/people/42/mug.png"
      },
      "modified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id: 48,
        "name": "Elon Musk",
        "image": "/people/48/mug.png"
      },
      "verified": {
        "time": "2012-02-15T15:12:21-05:00",
        "user_id": "42",
        "name": "Diego Gomes",
        "image": "/people/42/mug.png"
      }
    }
  ]
}
````

===

`GET /1/companies/{{company_id}}.json`
Get a single company

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "object": "company",
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
  "deals": [
    {
      "id": "1234",
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
  "people": [
    {
      "id": "1",
      "name": "Luciano Tavares",
      "role": "CEO",
      "image": "/people/1/mug.png"
    },
    {
      "id": "2",
      "name": "Fabiano Beselga",
      "role": "CTO",
      "image": "/people/2/mug.png"
    }
  ],
  "created": {
    "time": "2012-02-15T15:12:21-05:00",
    "user_id: 42,
    "name": "Diego Gomes",
    "image": "/people/42/mug.png"
  },
  "modified": {
    "time": "2012-02-15T15:12:21-05:00",
    "user_id: 48,
    "name": "Elon Musk",
    "image": "/people/48/mug.png"
  },
  "verified": {
    "time": "2012-02-15T15:12:21-05:00",
    "user_id": "42",
    "name": "Diego Gomes",
    "image": "/people/42/mug.png"
  }
}
````
===

`POST /1/companies.json`
Create a new company

* Required permission: write

````
{
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
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "object": "company",
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
    "image": "/people/42/mug.png"
  }
}
````
===

`PUT /1/companies/{{company_id}}.json`
Update a company

* Required permission: write

````
{
  "description": "Magnetis is the most awesome online advisor ever"
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "object": "company",
  "id": "42",
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
    "image": "/people/42/mug.png"
  }
}
````
===

`DELETE /1/companies/{{company_id}}.json`
Update a company

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
