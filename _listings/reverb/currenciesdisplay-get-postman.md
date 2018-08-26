{
  "info": {
    "name": "reverb Get Currencies Display",
    "_postman_id": "ad850870-6da7-4e87-93d1-c430e55e272a",
    "description": "List of supported display currencies for browsing listings",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Currencies",
      "item": [
        {
          "id": "c107f5ab-3544-402d-94dc-6dc2198bb08b",
          "name": "getCurrenciesDisplay",
          "request": {
            "url": "http://api.reverb.com/api/currencies/display",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List of supported display currencies for browsing listings"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "752f75d3-aded-43a4-92c1-f8071f08841e"
            }
          ]
        }
      ]
    }
  ]
}