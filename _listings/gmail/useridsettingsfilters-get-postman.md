{
  "info": {
    "name": "Gmail Get Message Filters",
    "_postman_id": "090e40a1-b4eb-4511-8ebd-9bbd38b5697c",
    "description": "Lists the message filters of a Gmail user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Filters",
      "item": [
        {
          "id": "c86a399b-6bb4-4ae4-b7d4-97a30ceb2f9a",
          "name": "gmail.users.settings.filters.list",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "gmail",
                "v1",
                "users",
                ":userId/settings/filters"
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
            "description": "Lists the message filters of a Gmail user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c155aa0e-958f-4e1a-b2d9-9811ddff0d44"
            }
          ]
        }
      ]
    }
  ]
}