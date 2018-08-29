{
  "info": {
    "name": "Xibo API Add a Video In Widget",
    "_postman_id": "be6438bc-5ef6-46a1-973b-468e4b5fd652",
    "description": "Add a new Video In Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Local",
      "item": [
        {
          "id": "5474fd30-470f-48da-b4e3-7854336c14a7",
          "name": "WidgetLocalVideoAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/localVideo/:playlistId"
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
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "mute",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should the video be muted?"
                },
                {
                  "key": "scaleTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "How should the video be scaled, available options: aspect, stretch"
                },
                {
                  "key": "uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "A local file path or URL to the video"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Local Video Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea80cce6-810b-47b7-981e-e95f2158a7f4"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "8a51b054-5404-494c-9e17-ee70bf98186c",
          "name": "WidgetVideoEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/video/:playlistId"
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
                  "description": "Edit only - Flag (0, 1) Should the video loop (only for duration > 0 )?"
                },
                {
                  "key": "mute",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Flag (0, 1) Should the video be muted?"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Optional Widget Name"
                },
                {
                  "key": "scaleTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "How should the video be scaled, available options: aspect, stretch"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Parameters for editing existing video on a layout, for adding new videos, please refer to POST /library documentation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68d19530-9993-4c8c-a1b3-d2e1b3453bd2"
            }
          ]
        }
      ]
    },
    {
      "name": "Video",
      "item": [
        {
          "id": "d323f7e9-07a8-470f-ac2c-a2174d0db8d5",
          "name": "WidgetVideoInAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/videoin/:playlistId"
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
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "sourceId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Which device input should be shown? available options: HDMI, RGB, DVI, DP, OPS"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Select only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Video In Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0e566fbd-821d-4929-b0ca-d1d137c38d90"
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