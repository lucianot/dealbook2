
__Market__

`GET /v1/markets`
Get a list of markets

* Required permission: read
* Arguments:
    + `limit`: amount of results (default: 50)
    + `page`: page to show (default: 1)
* Sample response:

````
HTTP/1.1 200 OK
{
  "markets": [
    {
      "id": "101",
      "href": "https://api.dealbook.co/v1/markets/101",
      "name": "financial services",
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
    },
    {
      "id": "102",
      "href": "https://api.dealbook.co/v1/markets/102",
      "name": "content marketing",
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
  ]
}
````

===

`GET /v1/markets/{{market_id}}`
Get a single market

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{  
  "market": {
    "id": "101",
    "href": "https://api.dealbook.co/v1/markets/101",
    "name": "financial services",
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

`POST /v1/markets`
Create a new market

* Required permission: write

````
{
  "market": {
    "name": "accounting software"
  }
}
````
* Sample response:

````
HTTP/1.1 201 Created
{
  "market": {
    "id": "101",
    "href": "https://api.dealbook.co/v1/markets/101",
    "name": "financial services",
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

`PUT /v1/markets/{{market_id}}`
Update a market

* Required permission: write

````
{
  "market": {
    "name": "investment services"
  }
}
````
* Sample response:

````
HTTP/1.1 200 OK
{
  "market": {
    "id": "101",
    "href": "https://api.dealbook.co/v1/markets/101",
    "name": "investment services",
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
