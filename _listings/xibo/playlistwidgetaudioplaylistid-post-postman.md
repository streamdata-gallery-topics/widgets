{
  "info": {
    "name": "Xibo API Parameters for editing existing audio widget on a layout",
    "_postman_id": "a63c5de1-c332-4c5c-9bc6-6f8a94c84c6e",
    "description": "Parameters for editing existing audio widget on a layout, for adding new audio, please refer to POST /library documentation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Parametersedting",
      "item": [
        {
          "id": "d89efeeb-d91f-4e7a-970a-d76c607ee26f",
          "name": "WidgetAssignedAudioEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/:widgetId/audio"
              ],
              "variable": [
                {
                  "id": "widgetId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
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
                  "key": "loop",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should the audio loop if it finishes before the widget has finished?"
                },
                {
                  "key": "mediaId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Id of a audio file in CMS library you wish to add to a widget"
                },
                {
                  "key": "volume",
                  "value": "{}",
                  "disabled": false,
                  "description": "Volume percentage(0-100) for this audio to play at"
                }
              ]
            },
            "description": "Parameters for edting/adding audio file to a specific widget"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a464f8fa-b33f-490d-ada8-41ce9e4f462c"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "bf7a0314-dab3-4cc8-88c8-9e8d212eaed8",
          "name": "WidgetAudioDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/:widgetId/audio"
              ],
              "variable": [
                {
                  "id": "widgetId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
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
            "description": "Delete assigned audio widget from specified widget ID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b06494f1-f58f-414e-91b5-39dc2a67c3ba"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "9ec8c062-2b14-4fe5-96f3-ee0ceccf6dc4",
          "name": "WidgetAudioEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/audio/:playlistId"
              ],
              "variable": [
                {
                  "id": "playlistId",
                  "value": "playlistId",
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
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget Duration"
                },
                {
                  "key": "loop",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the audio loop (only for duration > 0 )?"
                },
                {
                  "key": "mute",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the audio be muted?"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - The Widget name"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Parameters for editing existing audio widget on a layout, for adding new audio, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89355940-24da-4190-bee1-9d38fd265b49"
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