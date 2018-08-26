{
  "info": {
    "name": "Xibo API Order Widgets",
    "_postman_id": "1c57bfc9-5866-4cdc-a567-e2fe3f62d4c5",
    "description": "Set the order of widgets in the Playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Order",
      "item": [
        {
          "id": "2878247b-a220-41f5-a381-66148f1c395c",
          "name": "playlistOrder",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/order/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "widgets",
                  "value": "{}",
                  "disabled": false,
                  "description": "Array of widgetIds and positions - all widgetIds present in the playlist need to be passed in the call with their positions"
                }
              ]
            },
            "description": "Set the order of widgets in the Playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d36f61c2-2559-473f-b93a-c1be57d3ad53"
            }
          ]
        }
      ]
    }
  ],
  "variable": [
    {
      "key": "default",
      "value": "http://www.example.com/api"
    }
  ]
}