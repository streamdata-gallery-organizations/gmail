{
  "info": {
    "name": "Gmail Send Verification Email",
    "_postman_id": "396ac97d-4eba-48fd-8ed4-44085127b43d",
    "description": "Sends a verification email to the specified send-as alias address. The verification status must be pending.\n\nThis method is only available to service account clients that have been delegated domain-wide authority.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "verification",
      "item": [
        {
          "id": "3e9e2b07-d377-44ed-9434-3b1fd1deaef3",
          "name": "gmail.users.settings.sendAs.verify",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "gmail",
                "v1",
                "users",
                ":userId/settings/sendAs/:sendAsEmail/verify"
              ],
              "variable": [
                {
                  "id": "sendAsEmail",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Sends a verification email to the specified send-as alias address"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6d78a4b3-5881-44b1-bc62-58194a504b29"
            }
          ]
        }
      ]
    }
  ]
}