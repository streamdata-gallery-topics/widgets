{
  "info": {
    "name": "Plentymarkets List all widgets provided by all frontend plugins of a given plugin set.",
    "_postman_id": "17249078-acf9-4d30-b017-4810e5764543",
    "description": "List all widgets provided by all frontend plugins of a given plugin set..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "5e9cbd2c-0086-4484-b73f-09218b8edcb6",
          "name": "getRestShopBuilderWgets",
          "request": {
            "url": "http://example.com/rest/shop_builder/widgets?identifier=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List all widgets provided by all frontend plugins of a given plugin set.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dd5785c3-f358-4b83-b5a8-87150a211db3"
            },
            {
              "status": "app_allow",
              "code": 500,
              "name": "Response_500",
              "id": "ac17e33f-8827-4962-b925-1717a626fa08"
            }
          ]
        }
      ]
    }
  ]
}