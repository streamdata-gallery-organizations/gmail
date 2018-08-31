{
  "info": {
    "name": "Gmail Get Auto-Forwarding Settings",
    "_postman_id": "4a8de11e-af9a-411e-8a83-d192dd91ef15",
    "description": "Gets the auto-forwarding setting for the specified account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "settings",
      "item": [
        {
          "id": "50ad775b-8236-4376-bb91-1c4b46820379",
          "name": "gmail.users.settings.getAutoForwarding",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "gmail",
                "v1",
                "users",
                ":userId/settings/autoForwarding"
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
            "description": "Gets the auto-forwarding setting for the specified account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "694848fb-c8d3-4ddd-bded-641e59c6180f"
            }
          ]
        }
      ]
    }
  ]
}