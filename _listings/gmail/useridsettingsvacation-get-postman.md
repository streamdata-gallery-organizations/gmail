{
  "info": {
    "name": "Gmail Get Vacation Settings",
    "_postman_id": "d38706b3-974c-4780-a9dd-cc9180741b31",
    "description": "Gets vacation responder settings.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "vacation settings",
      "item": [
        {
          "id": "5d5f165b-4520-411f-9b3b-ee4fb8c086fb",
          "name": "gmail.users.settings.getVacation",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "gmail",
                "v1",
                "users",
                ":userId/settings/vacation"
              ],
              "variable": [
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets vacation responder settings"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60d5c1a4-b325-4cb1-bdea-936350df020f"
            }
          ]
        }
      ]
    }
  ]
}