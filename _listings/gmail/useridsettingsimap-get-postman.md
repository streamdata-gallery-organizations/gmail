{
  "info": {
    "name": "Gmail Gets IMAP Settings",
    "_postman_id": "d7ef0c00-1431-4d5d-b35a-d1ead9357676",
    "description": "Gets IMAP settings.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "imap settings",
      "item": [
        {
          "id": "fdcb825c-3a2b-4919-8fdc-3a4ca0b1cfed",
          "name": "gmail.users.settings.getImap",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "gmail",
                "v1",
                "users",
                ":userId/settings/imap"
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
            "description": "Gets IMAP settings"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "02eeb4ea-c979-4188-917c-6e0aa986f1d8"
            }
          ]
        }
      ]
    }
  ]
}