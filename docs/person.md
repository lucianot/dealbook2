
__Person__

`GET /v1/persons`
Get a list of persons

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "persons": [
    {
      "id": "1",
      "href": "https://api.dealbook.co/v1/persons/1",
      "name": "Luciano Tavares",
      "image": "/persons/1/mug.png",
      "website": "napkn.co",
      "social_links": [
        "twitter.com/@lucianot"
      ],
      "companies": [
        {
          "id": "42",
          "href": "https://api.dealbook.co/v1/companies/42",
          "name": "Magnetis",
          "role": "CEO"
        }
      ],
      "investors": [
        {
          "id": "1000",
          "href": "https://api.dealbook.co/v1/investors/1000",
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
    },
    {
      "id": "2",
      "href": "https://api.dealbook.co/v1/persons/2",
      "name": "Fabiano Beselga",
      "image": "/persons/2/mug.png",
      "website": "beselga.com",
      "social_links": [
        "twitter.com/@fbzga"
      ],
      "companies": [
        {
          "id": "42",
          "href": "https://api.dealbook.co/v1/companies/42",
          "name": "Magnetis",
          "role": "CTO"
        }
      ],
      "investors": [],
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

`GET /v1/persons/{{person_id}}`
Get a single person

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "person": {
    "id": "1",
    "href": "https://api.dealbook.co/v1/persons/1",
    "name": "Luciano Tavares",
    "image": "/persons/1/mug.png",
    "website": "napkn.co",
    "social_links": [
      "twitter.com/@lucianot"
    ],
    "companies": [
      {
        "id": "42",
        "href": "https://api.dealbook.co/v1/companies/42",
        "name": "Magnetis",
        "role": "CEO"
      }
    ],
    "investors": [
      {
        "id": "1000",
        "href": "https://api.dealbook.co/v1/investors/1000",
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
}
````
===

`POST /v1/persons`
Create a new person

* Required permission: write

````
{
  "person": {
    "name": "Luciano Tavares",
    "image": "/persons/1/mug.png",
    "website": "napkn.co",
    "social_links": [
      "twitter.com/@lucianot"
    ]
  }
}
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "person": {
    "id": "1",
    "href": "https://api.dealbook.co/v1/persons/1",
    "name": "Luciano Tavares",
    "image": "/persons/1/mug.png",
    "website": "napkn.co",
    "social_links": [
      "twitter.com/@lucianot"
    ],
    "companies": [
      {
        "id": "42",
        "href": "https://api.dealbook.co/v1/companies/42",
        "name": "Magnetis",
        "role": "CEO"
      }
    ],
    "investors": [
      {
        "id": "1000",
        "href": "https://api.dealbook.co/v1/investors/1000",
        "name": "Napkn Ventures",
        "role": "partner"
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

`PUT /v1/persons/{{person_id}}`
Update a person

* Required permission: write

````
{
  "person": {
    "name": "Luciano Mascarenhas Tavares"
  }
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "person": {
    "id": "1",
    "href": "https://api.dealbook.co/v1/persons/1",
    "name": "Luciano Mascarenhas Tavares",
    "image": "/persons/1/mug.png",
    "website": "napkn.co",
    "social_links": [
      "twitter.com/@lucianot"
    ],
    "companies": [
      {
        "id": "42",
        "href": "https://api.dealbook.co/v1/companies/42",
        "name": "Magnetis",
        "role": "CEO"
      }
    ],
    "investors": [
      {
        "id": "1000",
        "href": "https://api.dealbook.co/v1/investors/1000",
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
    }
  }
}
````
===

`DELETE /v1/persons/{{person_id}}`
Destroy a person

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
