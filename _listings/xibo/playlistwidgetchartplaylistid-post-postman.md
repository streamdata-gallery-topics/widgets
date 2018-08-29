{
  "info": {
    "name": "Xibo API Add a Chart Widget",
    "_postman_id": "4d533cfe-c909-4973-a712-e453097d0ffb",
    "description": "Add a new Chart Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Chart",
      "item": [
        {
          "id": "0ff1906e-3370-4024-8cab-97c1db0f3255",
          "name": "WidgetChartAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/chart/:playlistId"
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
                  "key": "backgroundColor",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Background Color"
                },
                {
                  "key": "columnType",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT only - Array of Column Types (x-axis, y-axis, series-identifier) to assign"
                },
                {
                  "key": "dataSetColumnId",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT only - Array of dataSetColumn IDs to assign"
                },
                {
                  "key": "dataSetId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Create Chart Widget using provided dataSetId of an existing dataSet"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - The Chart Duration"
                },
                {
                  "key": "filter",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - SQL clause for filter this dataSet"
                },
                {
                  "key": "fontColor",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Font Color"
                },
                {
                  "key": "fontSize",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Font Size"
                },
                {
                  "key": "graphType",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT only - Chart Type"
                },
                {
                  "key": "legendPosition",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Where should the Legend be Shown (top, left, right, bottom)"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "ordering",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - SQL clause for how this dataSet should be ordered"
                },
                {
                  "key": "showLegend",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Should the Legend be Shown"
                },
                {
                  "key": "startYAtZero",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Start the Y-Axis at 0"
                },
                {
                  "key": "title",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Chart title"
                },
                {
                  "key": "updateInterval",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Update interval in minutes"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "useFilteringClause",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - flag (0,1) Use advanced filter clause - set to 1 if filter is provided"
                },
                {
                  "key": "useOrderingClause",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - flag (0,1) Use advanced order clause - set to 1 if ordering is provided"
                },
                {
                  "key": "x-axis-label",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Chart x-axis label"
                },
                {
                  "key": "y-axis-label",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Chart y-axis label"
                }
              ]
            },
            "description": "Add a new Chart Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3083a208-fcd7-44f1-9557-39078fbea5bd"
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