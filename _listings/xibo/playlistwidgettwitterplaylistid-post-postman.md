{
  "info": {
    "name": "Xibo API Add a Twitter Widget",
    "_postman_id": "9264cc97-afe3-42cc-a5d4-42599425d406",
    "description": "Add a new Twitter Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Order",
      "item": [
        {
          "id": "42e03588-a252-44ee-bfc9-762ac5ac45f6",
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
              "id": "85be7f48-57e1-4f85-a17f-8487b69ea23a"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "3fb31de2-b96d-4160-ad27-52c4f8ef9b8f",
          "name": "WidgetEdit",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/:widgetId"
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
              "mode": "raw"
            },
            "description": "Edit a Widget, please refer to individual widget Add documentation for module specific parameters"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6fe9768b-0687-4089-8a59-ff87bf33ac44"
            }
          ]
        }
      ]
    },
    {
      "name": "Widget",
      "item": [
        {
          "id": "84e16ad7-d923-412c-a346-59ac89ffe9df",
          "name": "WidgetDelete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/:widgetId"
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
            "description": "Deleted a specified widget"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3ce49025-c5c9-4782-a31e-1280b8f1e87e"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersedting",
      "item": [
        {
          "id": "69510a7d-4cae-4831-8906-d66d569b4426",
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
              "id": "b2cc4e4c-5ffc-41f7-b876-d3aa0515b1e7"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "3d954b44-d214-4956-8c96-fe55882d2a7b",
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
              "id": "aca56780-9243-467a-a056-2ebea6361655"
            }
          ]
        }
      ]
    },
    {
      "name": "Playlist",
      "item": [
        {
          "id": "01f9ee5b-f085-4ebb-8b8d-550c690617a9",
          "name": "playlistSearch",
          "request": {
            "url": "{{default}}/playlist/widget",
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
            "description": "Search widgets on a Playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cf2e10a3-2f2b-4df8-aba0-1a70fe51e55c"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "85874c57-2036-4f8c-9166-7bb5d9396ddd",
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
              "id": "6ec2b9ec-483e-4643-8ba0-0c654dcadbe5"
            }
          ]
        }
      ]
    },
    {
      "name": "Chart",
      "item": [
        {
          "id": "6dd14178-8b05-49f7-807d-06a079fecdf4",
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
              "id": "87c59623-d9ea-468c-a444-aab40d51dba5"
            }
          ]
        }
      ]
    },
    {
      "name": "Clock",
      "item": [
        {
          "id": "98139b5d-d434-4e02-b6bc-1be56f0e5705",
          "name": "WidgetClockAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/clock/:playlistId"
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
                  "key": "ClockFace",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Flip Clock, supported options: TwelveHourClock TwentyFourHourClock HourlyCounter MinuteCounter DailyCounter"
                },
                {
                  "key": "clockTypeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Type of a clock widget 1-Analogue, 2-Digital, 3-Flip clock"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "format",
                  "value": "{}",
                  "disabled": false,
                  "description": "For digital clock, format in which the time should be displayed example [HH:mm]"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "offset",
                  "value": "{}",
                  "disabled": false,
                  "description": "The offset in minutes that should be applied to the current time, if a counter is selected then date/time to run from in the format Y-m-d H:i:s"
                },
                {
                  "key": "showSeconds",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Flip Clock, should the clock show seconds or not"
                },
                {
                  "key": "themeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0 , 1) for Analogue clock the light and dark theme"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Clock Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1dbb33b-5921-4a12-b5c6-ea75c5cd1d1a"
            }
          ]
        }
      ]
    },
    {
      "name": "Currencies",
      "item": [
        {
          "id": "717070f6-3974-424d-a42c-352454e468a6",
          "name": "WidgetCurrenciesAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/currencies/:playlistId"
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
                  "description": "A HEX color to use as the background color of this widget"
                },
                {
                  "key": "base",
                  "value": "{}",
                  "disabled": false,
                  "description": "The base currency"
                },
                {
                  "key": "dateFormat",
                  "value": "{}",
                  "disabled": false,
                  "description": "The format to apply to all dates returned by he widget"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Widget Duration"
                },
                {
                  "key": "durationIsPerPage",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag (0, 1), The duration specified is per page/item, otherwise the widget duration is divided between the number of pages/items"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind"
                },
                {
                  "key": "items",
                  "value": "{}",
                  "disabled": false,
                  "description": "Items wanted"
                },
                {
                  "key": "itemtemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Template for each item, replaces [itemsTemplate] in main template, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "javaScript",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional JavaScript, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "mainTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Main template, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "maxItemsPerPage",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended number of items on each page"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "noRecordsMessage",
                  "value": "{}",
                  "disabled": false,
                  "description": "A message to display when there are no records returned by the search query"
                },
                {
                  "key": "overrideTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0, 1) set to 0 and use templateId or set to 1 and provide whole template in the next parameters"
                },
                {
                  "key": "reverseConversion",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 if youd like your base currency to be used as the comparison currency youve entered"
                },
                {
                  "key": "speed",
                  "value": "{}",
                  "disabled": false,
                  "description": "The transition speed of the selected effect in milliseconds (1000 = normal)"
                },
                {
                  "key": "styleSheet",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional StyleSheet Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "templateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use pre-configured templates, available options: currencies1, currencies2"
                },
                {
                  "key": "updateInterval",
                  "value": "{}",
                  "disabled": false,
                  "description": "Update interval in minutes, should be kept as high as possible, if data change once per hour, this should be set to 60"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "widgetOriginalHeight",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended Height of the template and is used to scale the Widget within its region when the template is applied, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "widgetOriginalWidth",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended Width of the template and is used to scale the Widget within its region when the template is applied, Pass only with overrideTemplate set to 1"
                }
              ]
            },
            "description": "Add a new Currencies Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b523acd1-ec21-4144-8823-7a5e76e70230"
            }
          ]
        }
      ]
    },
    {
      "name": "DataSetView",
      "item": [
        {
          "id": "4014e215-f6ce-4cc6-a31e-fdd3881180a6",
          "name": "WidgetdataSetViewAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/dataSetView/:playlistId"
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
                  "key": "dataSetColumnId",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT only - Array of dataSetColumn IDs to assign"
                },
                {
                  "key": "dataSetId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Create dataSetView Widget using provided dataSetId of an existing dataSet"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - The dataSetView Duration"
                },
                {
                  "key": "filter",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - SQL clause for filter this dataSet"
                },
                {
                  "key": "lowerLimit",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Lower low limit for this dataSet, 0 for nor limit"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "noDataMessage",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - A message to display when no data is returned from the source"
                },
                {
                  "key": "ordering",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - SQL clause for how this dataSet should be ordered"
                },
                {
                  "key": "overrideTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - flag (0, 1) override template checkbox"
                },
                {
                  "key": "rowsPerPage",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Number of rows per page, 0 for no pages"
                },
                {
                  "key": "showHeadings",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Should the table show Heading? (0,1)"
                },
                {
                  "key": "templateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Template youd like to apply, options available: empty, light-green"
                },
                {
                  "key": "updateInterval",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Update interval in minutes"
                },
                {
                  "key": "upperLimit",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - Upper low limit for this dataSet, 0 for nor limit"
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
                }
              ]
            },
            "description": "Add a new dataSetView Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "81232582-583e-4dd9-9e81-63855543da90"
            }
          ]
        }
      ]
    },
    {
      "name": "Embedded",
      "item": [
        {
          "id": "03c35e23-1ec6-49e5-afa3-5b578e5b25d2",
          "name": "WidgetEmbeddedAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/embedded/:playlistId"
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
                  "key": "embedHtml",
                  "value": "{}",
                  "disabled": false,
                  "description": "HTML to embed"
                },
                {
                  "key": "embedScript",
                  "value": "{}",
                  "disabled": false,
                  "description": "HEAD content to Embed (including script tags)"
                },
                {
                  "key": "embedStyle",
                  "value": "{}",
                  "disabled": false,
                  "description": "Custom Style Sheets (CSS)"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "scaleContent",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0,1) - Should the embedded content be scaled along with the layout?"
                },
                {
                  "key": "transparency",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0,1) - Should the HTML be shown with transparent background? - not available on Windows Clients"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Embedded Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "917730a1-386c-40ef-8b8c-4a4dd0f94cc9"
            }
          ]
        }
      ]
    },
    {
      "name": "Finance",
      "item": [
        {
          "id": "1aa2e578-9fd8-40d2-8901-ee3f9b96582c",
          "name": "WidgetFinanceAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/finance/:playlistId"
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
                  "description": "A HEX color to use as the background color of this widget"
                },
                {
                  "key": "dateFormat",
                  "value": "{}",
                  "disabled": false,
                  "description": "The format to apply to all dates returned by he widget"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Widget Duration"
                },
                {
                  "key": "durationIsPerItem",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag (0, 1), The duration specified is per item, otherwise the widget duration is divided between the number of items"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft"
                },
                {
                  "key": "item",
                  "value": "{}",
                  "disabled": false,
                  "description": "Items wanted, can be comma separated (example EURUSD, GBPUSD), pass only with overrideTemplate set to 1"
                },
                {
                  "key": "javaScript",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional JavaScript, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "noRecordsMessage",
                  "value": "{}",
                  "disabled": false,
                  "description": "A message to display when there are no records returned by the search query"
                },
                {
                  "key": "overrideTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0, 1) set to 0 and use templateId or set to 1 and provide whole template in the next parameters"
                },
                {
                  "key": "resultIdentifier",
                  "value": "{}",
                  "disabled": false,
                  "description": "The name of the result identifier returned by the YQL, pass only with overrideTemplate set to 1"
                },
                {
                  "key": "speed",
                  "value": "{}",
                  "disabled": false,
                  "description": "The transition speed of the selected effect in milliseconds (1000 = normal) or the Marquee speed in a low to high scale (normal = 1)"
                },
                {
                  "key": "styleSheet",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional StyleSheet Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "template",
                  "value": "{}",
                  "disabled": false,
                  "description": "Main template, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "templateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use pre-configured templates, available options: currency-simple, stock-simple"
                },
                {
                  "key": "updateInterval",
                  "value": "{}",
                  "disabled": false,
                  "description": "Update interval in minutes, should be kept as high as possible, if data change once per hour, this should be set to 60"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "yql",
                  "value": "{}",
                  "disabled": false,
                  "description": "The YQL query to use for data, pass only with overrideTemplate set to 1"
                }
              ]
            },
            "description": "Add a new Finance Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b75ffb3f-fd60-47d9-a40f-cedbcf67f483"
            }
          ]
        }
      ]
    },
    {
      "name": "Weather",
      "item": [
        {
          "id": "887e73f9-012e-4225-a796-4797834a3369",
          "name": "WidgetWeatherAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/forecastIo/:playlistId"
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
                  "key": "currentTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Current template, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "dailyTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Replaces [dailyForecast] in main template, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "dayConditionsOnly",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Would you like to only show the Daytime weather conditions"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Widget Duration"
                },
                {
                  "key": "lang",
                  "value": "{}",
                  "disabled": false,
                  "description": "Language youd like to use, supported languages ar, az, be, bs, cs, de, en, el, es, fr, hr, hu, id, it, is, kw, nb, nl, pl, pt, ru, sk, sr, sv, tet, tr, uk, x-pig-latin, zh, zh-tw"
                },
                {
                  "key": "latitude",
                  "value": "{}",
                  "disabled": false,
                  "description": "The latitude for this weather widget, only pass if useDisplayLocation set to 0"
                },
                {
                  "key": "longitude",
                  "value": "{}",
                  "disabled": false,
                  "description": "The longitude for this weather widget, only pass if useDisplayLocation set to 0"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "overrideTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0, 1) set to 0 and use templateId or set to 1 and provide whole template in the next parameters"
                },
                {
                  "key": "styleSheet",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional StyleSheet, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "templateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use pre-configured templates, available options: weather-module0-5day, weather-module0-singleday, weather-module0-singleday2, weather-module1l, weather-module1p, weather-module2l, weather-module2p, weather-module3l, weather-module3p, weather-module4l, weather-module4p, weather-module5l, weather-module6v, weather-module6h"
                },
                {
                  "key": "units",
                  "value": "{}",
                  "disabled": false,
                  "description": "Units you would like to use, available options: auto, ca, si, uk2, us"
                },
                {
                  "key": "updateInterval",
                  "value": "{}",
                  "disabled": false,
                  "description": "Update interval in minutes, should be kept as high as possible, if data change once per hour, this should be set to 60"
                },
                {
                  "key": "useDisplayLocation",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Use the location configured on display"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "widgetOriginalHeight",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended Height of the template and is used to scale the Widget within its region when the template is applied, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "widgetOriginalWidth",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended Width of the template and is used to scale the Widget within its region when the template is applied, Pass only with overrideTemplate set to 1"
                }
              ]
            },
            "description": "Add a new Weather Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dd36df47-0c6f-4bcc-b480-58d689bd42eb"
            }
          ]
        }
      ]
    },
    {
      "name": "Google",
      "item": [
        {
          "id": "b6d2bdc0-84da-4d73-aac1-a1ca62fc35e1",
          "name": "WidgetGoogleTrafficAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/googleTraffic/:playlistId"
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
                  "key": "latitude",
                  "value": "{}",
                  "disabled": false,
                  "description": "The latitude for this weather widget, only pass if useDisplayLocation set to 0"
                },
                {
                  "key": "longitude",
                  "value": "{}",
                  "disabled": false,
                  "description": "The longitude for this weather widget, only pass if useDisplayLocation set to 0"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "useDisplayLocation",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Use the location configured on display"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "zoom",
                  "value": "{}",
                  "disabled": false,
                  "description": "How far should the map be zoomed in? The higher the number the closer the zoom, 1 represents entire globe"
                }
              ]
            },
            "description": "Add a new Google traffic Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a5fdf3e9-d419-4012-9550-9c90f33d872f"
            }
          ]
        }
      ]
    },
    {
      "name": "HLS",
      "item": [
        {
          "id": "e96f677d-3771-43e0-b223-7177e8a6a6db",
          "name": "WidgetHlsAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/hls/:playlistId"
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "transparency",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1), This causes some android devices to switch to a hardware accelerated web view"
                },
                {
                  "key": "uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "URL to HLS video stream"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit Only - (0, 1) Select only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new HLS Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5bd3e98f-74b6-4bf1-8fef-a30934a9f4e6"
            }
          ]
        }
      ]
    },
    {
      "name": "Local",
      "item": [
        {
          "id": "c3e5b7a2-6d3d-4a11-a6e9-466e8c7eca5c",
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
              "id": "e8e08b13-1f51-4dc8-b9f8-520dca5062ed"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "708f9b5e-2b5e-4798-a572-541eddbc4f0b",
          "name": "WidgetNotificationAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/notificationview/:playlistId"
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
                  "key": "age",
                  "value": "{}",
                  "disabled": false,
                  "description": "The maximum notification age in minutes - 0 for all"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "durationIsPerItem",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag (0, 1), The duration specified is per page/item, otherwise the widget duration is divided between the number of pages/items"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind"
                },
                {
                  "key": "embedStyle",
                  "value": "{}",
                  "disabled": false,
                  "description": "Custom Style Sheets (CSS)"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "noDataMessage",
                  "value": "{}",
                  "disabled": false,
                  "description": "Message to show when no notifications are available"
                },
                {
                  "key": "speed",
                  "value": "{}",
                  "disabled": false,
                  "description": "The transition speed of the selected effect in milliseconds (1000 = normal)"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Notification Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fc5f4a84-f9d0-4612-b309-fe3c1bbc06f3"
            }
          ]
        }
      ]
    },
    {
      "name": "Shell",
      "item": [
        {
          "id": "dcd64fb1-25ec-4f99-a4ec-286fcda8ef37",
          "name": "WidgetShellCommandAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/shellCommand/:playlistId"
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
                  "key": "commandCode",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter a reference code for exiting command in CMS"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "launchThroughCmd",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Windows only, Should the player launch this command through the windows command line (cmd"
                },
                {
                  "key": "linuxCommand",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter a Android / Linux command line compatible command"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "terminateCommand",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Should the player forcefully terminate the command after the duration specified, 0 to let the command terminate naturally"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "useTaskkill",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) Windows only, should the player use taskkill to terminate commands"
                },
                {
                  "key": "windowsCommand",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter a Windows command line compatible command"
                }
              ]
            },
            "description": "Add a new Shell Command Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11c04d34-3a50-4caf-8b19-84598c671c89"
            }
          ]
        }
      ]
    },
    {
      "name": "Stocks",
      "item": [
        {
          "id": "62a3a293-8520-4647-88f2-e8d72670f778",
          "name": "WidgetStocksAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/stocks/:playlistId"
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
                  "description": "A HEX color to use as the background color of this widget"
                },
                {
                  "key": "dateFormat",
                  "value": "{}",
                  "disabled": false,
                  "description": "The format to apply to all dates returned by he widget"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "Widget Duration"
                },
                {
                  "key": "durationIsPerPage",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag (0, 1), The duration specified is per page, otherwise the widget duration is divided between the number of pages/items"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind"
                },
                {
                  "key": "items",
                  "value": "{}",
                  "disabled": false,
    