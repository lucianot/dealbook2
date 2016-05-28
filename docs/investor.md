
__Investor__

`GET /v1/investors`
Get a list of investors

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
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
      ],
      "markets": [
        "fintech",
        "e-commerce",
        "saas"
      ],
      "locations": [
        "São Paulo, Brazil"
      ],
      "investments": [
        {
          "id": "42",
          "href": "https://api.dealbook.co/v1/companies/42",
          "company": "Magnetis",
          "deal": "1234"
        },
        {
          "id": "24",
          "href": "https://api.dealbook.co/v1/companies/24",
          "company": "RockContent",
          "deal": "2345"
        }
      ],
      "persons": [
        {
          "id": "101",
          "href": "https://api.dealbook.co/v1/persons/101",
          "name": "Eric",
          "role": "Partner",
          "image": "/persons/101/mug.png"
        },
        {
          "id": "102",
          "href": "https://api.dealbook.co/v1/persons/102",
          "name": "Marcelo",
          "role": "Partner",
          "image": "/persons/102/mug.png"
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
      "id": "1002",
      "href": "https://api.dealbook.co/v1/investors/1002",
      "name": "Redpoint e.ventures",
      "description": "Redpoint is a VC",
      "logo": "/investors/1002/logo.png",
      "website": "rpev.com.br",
      "social_links": [
        "twitter.com/@rpev"
      ],
      "markets": [
        "content marketing",
        "saas"
      ],
      "locations": [
        "São Paulo, Brazil"
      ],
      "investments": [
        {
          "id": "42",
          "href": "https://api.dealbook.co/v1/companies/42",
          "company": "Magnetis",
          "deal": "1234"
        },
        {
          "id": "24",
          "href": "https://api.dealbook.co/v1/companies/24",
          "company": "RockContent",
          "deal": "2345"
        }
      ],
      "persons": [
        {
          "id": "201",
          "href": "https://api.dealbook.co/v1/persons/201",
          "name": "Manoel",
          "role": "Partner",
          "image": "/persons/201/mug.png"
        },
        {
          "id": "202",
          "href": "https://api.dealbook.co/v1/persons/202",
          "name": "Anderson",
          "role": "Partner",
          "image": "/persons/202/mug.png"
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

`GET /v1/investors/{{investor_id}}`
Get a single investor

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "investor": {
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
    "investments": [
      {
        "id": "42",
        "company": "Magnetis",
        "deal": "1234"
      },
      {
        "id": "24",
        "company": "RockContent",
        "deal": "2345"
      }
    ],
    "persons": [
      {
        "id": "101",
        "name": "Eric",
        "role": "Partner",
        "image": "/persons/101/mug.png"
      },
      {
        "id": "102",
        "name": "Marcelo",
        "role": "Partner",
        "image": "/persons/102/mug.png"
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

`POST /1/investors`
Create a new investor

* Required permission: write

````
{
  "investor": {
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
    ]
  }
}
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "investor": {
    "id": "1001",
    "href": "https://api.dealbook.co/v1/investors/1001",
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
    "investments": [
      {
        "id": "42",
        "href": "https://api.dealbook.co/v1/companies/42",
        "company": "Magnetis",
        "deal": "1234"
      },
      {
        "id": "24",
        "href": "https://api.dealbook.co/v1/companies/24",
        "company": "RockContent",
        "deal": "2345"
      }
    ],
    "persons": [
      {
        "id": "101",
        "href": "https://api.dealbook.co/v1/persons/101",
        "name": "Eric",
        "role": "Partner",
        "image": "/persons/101/mug.png"
      },
      {
        "id": "102",
        "href": "https://api.dealbook.co/v1/persons/102",
        "name": "Marcelo",
        "role": "Partner",
        "image": "/persons/102/mug.png"
      }
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

`PUT /v1/investors/{{investor_id}}`
Update an investor

* Required permission: write

````
{
  "investor": {
    "description": "Monashees is a cool VC"
  }
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "investor": {
    "id": "1001",
    "href": "https://api.dealbook.co/v1/investors/1001",
    "name": "Monashees Capital",
    "description": "Monashees is a cool VC",
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
    }
  }
}
````
===

`DELETE /v1/investors/{{investor_id}}`
Destroy an investor

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
