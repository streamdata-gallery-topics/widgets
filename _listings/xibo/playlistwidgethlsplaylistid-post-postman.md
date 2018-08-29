{
  "info": {
    "name": "Xibo API Add a HLS Widget",
    "_postman_id": "aaf70929-a6d8-404a-8e8b-25b41970c629",
    "description": "Add a new HLS Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Order",
      "item": [
        {
          "id": "38a28cef-4ddb-4e0d-920e-957936d67290",
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
              "id": "ff3785c4-aed9-4db1-960e-06fab6ca1077"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "5e02ac26-b659-4056-9665-56a34f8c9d9c",
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
              "id": "afdc2c28-479a-49af-bd2b-0230ff0f5569"
            }
          ]
        }
      ]
    },
    {
      "name": "Widget",
      "item": [
        {
          "id": "dc15d324-d1f4-4d34-b11b-c863bb37d4b5",
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
              "id": "0517ba0f-5962-4fff-b8e2-ef49ce7faecf"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersedting",
      "item": [
        {
          "id": "5e293cc3-2819-42d4-98c7-1d85b712a77b",
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
              "id": "9aeca1e3-046f-4f17-822a-8edad0356617"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "0550a22c-80d1-44e8-b700-4e09b63d10c1",
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
              "id": "e527e977-a7b4-435f-a70c-7f24cf8ef16b"
            }
          ]
        }
      ]
    },
    {
      "name": "Playlist",
      "item": [
        {
          "id": "53cd2b28-9695-48a0-aec9-08fec1472881",
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
              "id": "776b4740-50d1-4e62-acae-14b453521b8b"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "3fb01929-4c7f-40e8-851c-2005a9b46c08",
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
              "id": "18fa2731-f540-4644-8b44-3ebaa3025f23"
            }
          ]
        }
      ]
    },
    {
      "name": "Chart",
      "item": [
        {
          "id": "c7601b17-3481-4326-9fde-752580d71b3f",
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
              "id": "6a6721bc-e1d4-4602-b431-d6cc8be07f83"
            }
          ]
        }
      ]
    },
    {
      "name": "Clock",
      "item": [
        {
          "id": "c3fcf3e8-b7ee-4da0-ab1c-3eed91b9d1d9",
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
              "id": "5e7710ca-da8e-4c9e-b841-d657a6f61469"
            }
          ]
        }
      ]
    },
    {
      "name": "Currencies",
      "item": [
        {
          "id": "f5ac55fe-baf4-498f-bf84-8d5b5f869ff4",
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
              "id": "8b7961d5-d019-4672-9d3e-89d9a57a6720"
            }
          ]
        }
      ]
    },
    {
      "name": "DataSetView",
      "item": [
        {
          "id": "09c6fd41-a7d1-41fd-afbc-6b44af21dd57",
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
              "id": "d2a94635-83c4-4822-bdff-fbf951ffb1b9"
            }
          ]
        }
      ]
    },
    {
      "name": "Embedded",
      "item": [
        {
          "id": "ca1f92db-4f28-431d-9dde-ed80b4c85572",
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
              "id": "5ba56c4f-76c1-45f0-b04d-84182e56bd9c"
            }
          ]
        }
      ]
    },
    {
      "name": "Finance",
      "item": [
        {
          "id": "0e3effc4-609d-4b52-a94d-41f51a64d23d",
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
              "id": "0763acd8-4662-4bf4-b94c-619e3078779b"
            }
          ]
        }
      ]
    },
    {
      "name": "Weather",
      "item": [
        {
          "id": "31993238-cd1f-4cac-b822-83de935344d4",
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
              "id": "92c32876-c118-40e6-91f1-2fc7d6987071"
            }
          ]
        }
      ]
    },
    {
      "name": "Google",
      "item": [
        {
          "id": "32779310-190c-48b4-8ee6-254c4b4b7275",
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
              "id": "1521d4fc-534d-4f97-ad26-e17e6b987b28"
            }
          ]
        }
      ]
    },
    {
      "name": "HLS",
      "item": [
        {
          "id": "8f80712a-e291-44e1-b816-3316eee5edeb",
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
              "id": "0a26de69-7e43-4a9d-a0fd-31b233bc61b9"
            }
          ]
        }
      ]
    },
    {
      "name": "Local",
      "item": [
        {
          "id": "a9020083-4059-411d-84cc-12dd4841ad1f",
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
              "id": "9702bbfa-bff4-4903-b200-8861042a09a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "46cf69c8-3397-4d60-ad38-2fa420ddef47",
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
              "id": "9db2a519-7d6c-4f41-8313-87781647ea43"
            }
          ]
        }
      ]
    },
    {
      "name": "Shell",
      "item": [
        {
          "id": "9b2db610-9d78-4b72-bab6-1ff1bc6c62ac",
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
              "id": "9c70680d-02a3-40dc-a5c5-fb6c93820e2b"
            }
          ]
        }
      ]
    },
    {
      "name": "Stocks",
      "item": [
        {
          "id": "2144a85c-695f-46f7-a661-e88973353c84",
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
            