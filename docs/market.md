
__Market__

`GET /1/markets.json`
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

`GET /1/markets/{{market_id}}.json`
Get a single market

* Required permission: read
* Sample response:

````
HTTP/1.1 200 OK
{  
  "market": {
    "id": "101",
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

`POST /1/markets.json`
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

`PUT /1/markets/{{market_id}}.json`
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

`DELETE /1/companies/{{company_id}}.json`
Destroy a company

* Required permission: write
* Sample response:

````
HTTP/1.1 200 OK
{}
````
