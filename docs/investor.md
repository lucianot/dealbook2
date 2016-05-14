
__Investor__

`GET /1/investors.json`
Get a list of investors

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "object": "list",
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
      "people": [
        {
          "id": "101",
          "name": "Eric",
          "role": "Partner",
          "image": "/people/101/mug.png"
        },
        {
          "id": "102",
          "name": "Marcelo",
          "role": "Partner",
          "image": "/people/102/mug.png"
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
      "id": "1002",
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
          "company": "Magnetis",
          "deal": "1234"
        },
        {
          "id": "24",
          "company": "RockContent",
          "deal": "2345"
        }
      ],
      "people": [
        {
          "id": "201",
          "name": "Manoel",
          "role": "Partner",
          "image": "/people/201/mug.png"
        },
        {
          "id": "202",
          "name": "Anderson",
          "role": "Partner",
          "image": "/people/202/mug.png"
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

`GET /1/investors/{{investor_id}}.json`
Get a single investor

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "object": "investor",
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
  "people": [
    {
      "id": "101",
      "name": "Eric",
      "role": "Partner",
      "image": "/people/101/mug.png"
    },
    {
      "id": "102",
      "name": "Marcelo",
      "role": "Partner",
      "image": "/people/102/mug.png"
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

`POST /1/investors.json`
Create a new investor

* Required permission: write

````
{
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
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "object": "investor",
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
  "people": [
    {
      "id": "101",
      "name": "Eric",
      "role": "Partner",
      "image": "/people/101/mug.png"
    },
    {
      "id": "102",
      "name": "Marcelo",
      "role": "Partner",
      "image": "/people/102/mug.png"
    }
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

`PUT /1/investors/{{investor_id}}.json`
Update an investor

* Required permission: write

````
{
  "description": "Monashees is a cool VC"
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "object": "investor",
  "id": "1001",
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
    "image": "/people/42/mug.png"
  },
  "modified": {
    "time": "2012-02-15T15:12:21-05:00",
    "user_id: 48,
    "name": "Elon Musk",
    "image": "/people/48/mug.png"
  }
}
````
===

`DELETE /1/investors/{{investor_id}}.json`
Destroy an investor

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
