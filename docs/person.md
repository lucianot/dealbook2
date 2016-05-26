
__Person__

`GET /1/persons.json`
Get a list of people

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
      "name": "Luciano Tavares",
      "image": "/people/1/mug.png",
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
      "id": "2",
      "name": "Fabiano Beselga",
      "image": "/people/2/mug.png",
      "website": "beselga.com",
      "social_links": [
        "twitter.com/@fbzga"
      ],
      "companies": [
        {
          "id": "42",
          "name": "Magnetis",
          "role": "CTO"
        }
      ],
      "investors": [],
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

`GET /1/persons/{{person_id}}.json`
Get a single person

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{
  "person": {
    "id": "1",
    "name": "Luciano Tavares",
    "image": "/people/1/mug.png",
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
}
````
===

`POST /1/persons.json`
Create a new person

* Required permission: write

````
{
  "person": {
    "name": "Luciano Tavares",
    "image": "/people/1/mug.png",
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
    "name": "Luciano Tavares",
    "image": "/people/1/mug.png",
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
      "image": "/people/42/mug.png"
    }
  }
}
````
===

`PUT /1/persons/{{person_id}}.json`
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
    "name": "Luciano Mascarenhas Tavares",
    "image": "/people/1/mug.png",
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
      "image": "/people/42/mug.png"
    },
    "modified": {
      "time": "2012-02-15T15:12:21-05:00",
      "user_id: 48,
      "name": "Elon Musk",
      "image": "/people/48/mug.png"
    }
  }
}
````
===

`DELETE /1/persons/{{person_id}}.json`
Destroy a person

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
