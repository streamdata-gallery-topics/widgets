{
  "info": {
    "name": "Xibo API Edit a Widget",
    "_postman_id": "26f79ebd-04f9-46bb-a587-f0e1e13c1109",
    "description": "Edit a Widget, please refer to individual widget Add documentation for module specific parameters",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Order",
      "item": [
        {
          "id": "1bb640f6-1787-4e9b-9a8e-261fd0a7ef1e",
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
              "id": "114da712-c518-4480-be98-1cd4c502b4bf"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "7c2478d9-1752-4b88-9498-370d7905c2b4",
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
              "id": "f91bb7e8-08c3-443a-89b4-8700b8bc1ffe"
            }
          ]
        }
      ]
    },
    {
      "name": "Widget",
      "item": [
        {
          "id": "c1de8c7c-0966-46e7-992d-85a3e168e8f4",
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
              "id": "aba83394-74e4-495a-837f-d449542ece39"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersedting",
      "item": [
        {
          "id": "dfd7436d-df7e-42c6-b251-8ec7ca977a23",
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
              "id": "03103c17-0aed-4a5f-b8af-5126f1e3b968"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "55a9d202-5bcb-425e-b96b-e72982fc4dd1",
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
              "id": "6540b9f1-fae0-4bdb-88e9-a606059e2b04"
            }
          ]
        }
      ]
    },
    {
      "name": "Playlist",
      "item": [
        {
          "id": "cd8b4565-c61c-47c3-8613-9a24316d409b",
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
              "id": "186160ee-d57a-439b-9ea0-36558039f557"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "0d416c88-8e2b-4d5e-901e-020c744adc71",
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
              "id": "0f7deed4-d0a3-4721-a301-e7d241077e0e"
            }
          ]
        }
      ]
    },
    {
      "name": "Chart",
      "item": [
        {
          "id": "0156e113-c1a9-49b8-9e9f-b21d3d0b1609",
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
              "id": "e972bb7c-4de4-4e09-8868-82c0c4c52a37"
            }
          ]
        }
      ]
    },
    {
      "name": "Clock",
      "item": [
        {
          "id": "0084c63b-1593-4251-a69c-4a0beade1809",
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
              "id": "81066088-7e66-47b0-9cb7-2ca7de69ac78"
            }
          ]
        }
      ]
    },
    {
      "name": "Currencies",
      "item": [
        {
          "id": "b5efbef1-5147-4ef6-92bf-d6a9cf102d47",
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
              "id": "128885f6-d4c7-4bc8-bf1e-fab8991cc2fa"
            }
          ]
        }
      ]
    },
    {
      "name": "DataSetView",
      "item": [
        {
          "id": "2b9fc7d6-ca0e-4cf8-9b30-eed8cd5bb2e3",
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
              "id": "e14da28c-c674-4d3f-894c-e72674131a66"
            }
          ]
        }
      ]
    },
    {
      "name": "Embedded",
      "item": [
        {
          "id": "cd636c5c-eac1-4bf2-be14-cfb3049ec28b",
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
              "id": "9c48a141-91df-4592-aaa6-56d62315fe42"
            }
          ]
        }
      ]
    },
    {
      "name": "Finance",
      "item": [
        {
          "id": "0cbd36c5-7e1d-4b33-b92c-f7332215b4ef",
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
              "id": "1ad2f315-a2bc-4d28-bda6-508a1c90bc22"
            }
          ]
        }
      ]
    },
    {
      "name": "Weather",
      "item": [
        {
          "id": "0d944cd1-3321-4101-872d-86a36825c362",
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
              "id": "32864a45-24fc-492f-bc34-3eb639cc1da4"
            }
          ]
        }
      ]
    },
    {
      "name": "Google",
      "item": [
        {
          "id": "b2716919-d641-41e0-a86d-7bcbdb2a9d92",
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
              "id": "bc8c2065-5943-4a6a-8325-d805a47eff9e"
            }
          ]
        }
      ]
    },
    {
      "name": "HLS",
      "item": [
        {
          "id": "459395f9-4030-49b0-a418-996311b39c56",
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
              "id": "86889630-3e1c-4e94-b1ea-e4bc650882b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Local",
      "item": [
        {
          "id": "65295218-59de-4f0e-ab8f-1da21d935547",
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
              "id": "5349003a-b108-4cc9-8d5e-726e781dd0e9"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "c3b09c67-f22d-4281-b774-aab8abbc6cb4",
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
              "id": "d7587baa-8124-4067-82fc-8c6cd08b87ec"
            }
          ]
        }
      ]
    },
    {
      "name": "Shell",
      "item": [
        {
          "id": "6873d559-39e6-49e9-bd06-e024822906ea",
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
              "id": "bb54849a-c354-4ec2-a237-81406b5b4e97"
            }
          ]
        }
      ]
    },
    {
      "name": "Stocks",
      "item": [
        {
          "id": "0d7e5b2b-0c05-4ad6-9a2f-07889f4fadf7",
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
                  "description": "Items wanted, can be comma separated"
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
                  "description": "Use pre-configured templates, available options: stocks1, stocks2"
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
                }
              ]
            },
            "description": "Add a new Stocks Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97acf60b-bb1c-4be6-8450-505a4b8cb08d"
            }
          ]
        }
      ]
    },
    {
      "name": "Text",
      "item": [
        {
          "id": "406b9fbf-cf53-4404-bcf8-0b35ac5c2038",
          "name": "WidgetTextAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/text/:playlistId"
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
                  "key": "backgroundcolor",
                  "value": "{}",
                  "disabled": false,
                  "description": "A HEX color to use as the background color of this widget"
                },
                {
                  "key": "duration",
                  "value": "{}",
                  "disabled": false,
                  "description": "The Widget Duration"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft"
                },
                {
                  "key": "javaScript",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional JavaScript"
                },
                {
                  "key": "marqueeInlineSelector",
                  "value": "{}",
                  "disabled": false,
                  "description": "The selector to use for stacking marquee items in a line when scrolling left/right"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "speed",
                  "value": "{}",
                  "disabled": false,
                  "description": "The transition speed of the selected effect in milliseconds (1000 = normal) or the Marquee speed in a low to high scale (normal = 1)"
                },
                {
                  "key": "text",
                  "value": "{}",
                  "disabled": false,
                  "description": "Enter the text to display"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Text Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58ceb42c-9a9f-4b6f-ba7c-7b20d994dbca"
            }
          ]
        }
      ]
    },
    {
      "name": "Ticker",
      "item": [
        {
          "id": "2475cb61-22b8-4bec-93d6-6708ba4c78b5",
          "name": "WidgetTickerAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/ticker/:playlistId"
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
                  "key": "allowedAttributes",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only and SourceId=1 - A comma separated list of attributes that should not be stripped from the feed"
                },
                {
                  "key": "backgroundColor",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - A HEX color to use as the background color of this widget"
                },
                {
                  "key": "copyright",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only and SourceId=1 - Copyright information to display as the last item in this feed"
                },
                {
                  "key": "css",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional StyleSheet Pass only with overrideTemplate set to 1 or with sourceId=2"
                },
                {
                  "key": "dataSetId",
                  "value": "{}",
                  "disabled": false,
                  "description": "For sourceId=2, Create ticker Widget using provided dataSetId of an existing dataSet"
                },
                {
                  "key": "dateFormat",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - The date format to apply to all dates returned by the ticker"
                },
                {
                  "key": "disableDateSort",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=1 - Should the date sort applied to the feed be disabled?"
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
                  "description": "A flag (0, 1), The duration specified is per item, otherwise it is per feed"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft"
                },
                {
                  "key": "filter",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=2 - SQL clause for filter this dataSet"
                },
                {
                  "key": "itemsPerPage",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - When in single mode, how many items per page should be shown"
                },
                {
                  "key": "itemsSideBySide",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag (0, 1), Should items be shown side by side"
                },
                {
                  "key": "javaScript",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional JavaScript, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "lowerLimit",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=2 - Lower low limit for this dataSet, 0 for nor limit"
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
                  "key": "numItems",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only and SourceId=1 - The number of RSS items you want to display"
                },
                {
                  "key": "ordering",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=2- SQL clause for how this dataSet should be ordered"
                },
                {
                  "key": "overrideTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=1 - flag (0, 1) override template checkbox"
                },
                {
                  "key": "randomiseItems",
                  "value": "{}",
                  "disabled": false,
                  "description": "A flag (0, 1), whether to randomise the feed"
                },
                {
                  "key": "sourceId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Add only - 1 for rss feed, 2 for dataset"
                },
                {
                  "key": "speed",
                  "value": "{}",
                  "disabled": false,
                  "description": "Edit only - The transition speed of the selected effect in milliseconds (1000 = normal) or the Marquee speed in a low to high scale (normal = 1)"
                },
                {
                  "key": "stripTags",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only and SourceId=1 - A comma separated list of attributes that should be stripped from the feed"
                },
                {
                  "key": "takeItemsFrom",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only and SourceId=1 - Take the items form the beginning or the end of the list, available options: start, end"
                },
                {
                  "key": "template",
                  "value": "{}",
                  "disabled": false,
                  "description": "Template for each item, replaces [itemsTemplate] in main template, Pass only with overrideTemplate set to 1 or with sourceId=2"
                },
                {
                  "key": "templateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=1 - Template youd like to apply, options available: title-only, prominent-title-with-desc-and-name-separator, media-rss-with-title, media-rss-wth-left-hand-text, media-rss-image-only"
                },
                {
                  "key": "textDirection",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=1 - Which direction does the text in the feed use? Available options: ltr, rtl"
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
                  "description": "EDIT Only, SourceId=2 - Upper low limit for this dataSet, 0 for nor limit"
                },
                {
                  "key": "uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "For sourceId=1, the link for the rss feed"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                },
                {
                  "key": "useFilteringClause",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=2 - flag (0,1) Use advanced filter clause - set to 1 if filter is provided"
                },
                {
                  "key": "useOrderingClause",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only, SourceId=2 - flag (0,1) Use advanced order clause - set to 1 if ordering is provided"
                }
              ]
            },
            "description": "Add a new ticker Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ab871829-3e34-4ce6-9cdb-ec171cae21f6"
            }
          ]
        }
      ]
    },
    {
      "name": "Twitter",
      "item": [
        {
          "id": "58b0d55d-1fef-4629-ba28-b666d4df8848",
          "name": "WidgetTwitterAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/twitter/:playlistId"
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
                  "description": "A flag (0, 1), The duration specified is per page/item, otherwise the widget duration is divided between the number of pages/items"
                },
                {
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind"
                },
                {
                  "key": "itemsPerPage",
                  "value": "{}",
                  "disabled": false,
                  "description": "EDIT Only - When in single mode, how many items per page should be shown"
                },
                {
                  "key": "javaScript",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional JavaScript, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "language",
                  "value": "{}",
                  "disabled": false,
                  "description": "Language in which tweets should be returned"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "noTweetsMessage",
                  "value": "{}",
                  "disabled": false,
                  "description": "A message to display when there are no tweets returned by the search query"
                },
                {
                  "key": "overrideTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0, 1) set to 0 and use templateId or set to 1 and provide whole template in the next parameters"
                },
                {
                  "key": "removeHashtags",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should the hashtags (#something) be removed from the tweet text"
                },
                {
                  "key": "removeMentions",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should mentions (@someone) be removed from the tweet text?"
                },
                {
                  "key": "removeUrls",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should the URLs be removed from the tweet text?"
                },
                {
                  "key": "resultContent",
                  "value": "{}",
                  "disabled": false,
                  "description": "Intended content Type, available Options: 0 - All Tweets 1 - Tweets with the text only content 2 - Tweets with the text and image content"
                },
                {
                  "key": "resultType",
                  "value": "{}",
                  "disabled": false,
                  "description": "1 - Mixed, 2 -Recent 3 - Popular, Recent shows only recent tweets, Popular the most popular tweets and Mixed included both popular and recent"
                },
                {
                  "key": "searchTerm",
                  "value": "{}",
                  "disabled": false,
                  "description": "Twitter search term, you can test your search term in twitter"
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
                  "key": "template",
                  "value": "{}",
                  "disabled": false,
                  "description": "Main template, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "templateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use pre-configured templates, available options: full-timeline-np, full-timeline, tweet-only, tweet-with-profileimage-left, tweet-with-profileimage-right, tweet-1, tweet-2, tweet-4"
                },
                {
                  "key": "tweetCount",
                  "value": "{}",
                  "disabled": false,
                  "description": "The number of tweets to return"
                },
                {
                  "key": "tweetDistance",
                  "value": "{}",
                  "disabled": false,
                  "description": "Distance in miles that the tweets should be returned from"
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
                  "key": "widgetOriginalPadding",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended Padding of the template and is used to scale the Widget within its region when the template is applied, Pass only with overrideTemplate set to 1"
                },
                {
                  "key": "widgetOriginalWidth",
                  "value": "{}",
                  "disabled": false,
                  "description": "This is the intended Width of the template and is used to scale the Widget within its region when the template is applied, Pass only with overrideTemplate set to 1"
                }
              ]
            },
            "description": "Add a new Twitter Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d2829231-4851-4093-a37e-ac36b8ef0cf3"
            }
          ]
        },
        {
          "id": "23ac38a1-11bc-487c-be5d-7965a230da5b",
          "name": "WidgetTwitterMetroAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/twittermetro/:playlistId"
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
                  "key": "colorTemplateId",
                  "value": "{}",
                  "disabled": false,
                  "description": "Use pre-configured templates, available options: default, full, gray, light, soft, vivid"
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
                  "key": "effect",
                  "value": "{}",
                  "disabled": false,
                  "description": "Effect that will be used to transitions between items, available options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle, tileSlide, tileBlind"
                },
                {
                  "key": "language",
                  "value": "{}",
                  "disabled": false,
                  "description": "Language in which tweets should be returned"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "noTweetsMessage",
                  "value": "{}",
                  "disabled": false,
                  "description": "A message to display when there are no tweets returned by the search query"
                },
                {
                  "key": "overrideColorTemplate",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0, 1) set to 0 and use colorTemplateId or set to 1 and provide colours to use in templateColours parameter"
                },
                {
                  "key": "removeHashtags",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should the hashtags (#something) be removed from the tweet text"
                },
                {
                  "key": "removeMentions",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should mentions (@someone) be removed from the tweet text?"
                },
                {
                  "key": "removeRetweets",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should retweets be filtered?"
                },
                {
                  "key": "removeUrls",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag (0, 1) Should the URLs be removed from the tweet text?"
                },
                {
                  "key": "resultContent",
                  "value": "{}",
                  "disabled": false,
                  "description": "Intended content Type, available Options: 0 - All Tweets 1 - Tweets with the text only content 2 - Tweets with the text and image content"
                },
                {
                  "key": "resultType",
                  "value": "{}",
                  "disabled": false,
                  "description": "1 - Mixed, 2 -Recent 3 - Popular, Recent shows only recent tweets, Popular the most popular tweets and Mixed included both popular and recent"
                },
                {
                  "key": "searchTerm",
                  "value": "{}",
                  "disabled": false,
                  "description": "Twitter search term, you can test your search term in twitter"
                },
                {
                  "key": "speed",
                  "value": "{}",
                  "disabled": false,
                  "description": "The transition speed of the selected effect in milliseconds (1000 = normal)"
                },
                {
                  "key": "templateColours",
                  "value": "{}",
                  "disabled": false,
                  "description": "Provide a string of new HEX colour codes to use, separated by |, for example: #e0d2c8|#5e411d|#fccf12|#82ff00|#64bae8"
                },
                {
                  "key": "tweetCount",
                  "value": "{}",
                  "disabled": false,
                  "description": "The number of tweets to return"
                },
                {
                  "key": "tweetDistance",
                  "value": "{}",
                  "disabled": false,
                  "description": "Distance in miles that the tweets should be returned from"
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
                }
              ]
            },
            "description": "Add a new Twitter Metro Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e4316294-5673-4daf-a868-d2fb2ab8fafb"
            }
          ]
        }
      ]
    },
    {
      "name": "Video",
      "item": [
        {
          "id": "4cdb4bf6-e578-42b2-92cb-f092b92dd5ef",
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
              "id": "fe63d886-a9d9-4f0b-b1cd-bc8455c4a2cb"
            }
          ]
        }
      ]
    },
    {
      "name": "Web",
      "item": [
        {
          "id": "3a1ce172-82b3-4c7d-9c59-d88f8f0d4183",
          "name": "WidgetWebpageAdd",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "playlist/widget/webpage/:playlistId"
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
                  "description": "The Web page Duration"
                },
                {
                  "key": "modeId",
                  "value": "{}",
                  "disabled": false,
                  "description": "The mode option for Web page, 1- Open Natively, 2- Manual Position, 3- Best Ft"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional Widget Name"
                },
                {
                  "key": "offsetLeft",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Manual position, the starting point from the left in pixels"
                },
                {
                  "key": "offsetTop",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Manual position, the starting point from the Top in pixels"
                },
                {
                  "key": "pageHeight",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Manual Position and Best Fit, The height of the page - if empty it will use region height"
                },
                {
                  "key": "pageWidth",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Manual Position and Best Fit, The width of the page - if empty it will use region width"
                },
                {
                  "key": "scaling",
                  "value": "{}",
                  "disabled": false,
                  "description": "For Manual position the percentage to scale the Web page (0-100)"
                },
                {
                  "key": "transparency",
                  "value": "{}",
                  "disabled": false,
                  "description": "flag (0,1) should the HTML be shown with a transparent background?"
                },
                {
                  "key": "uri",
                  "value": "{}",
                  "disabled": false,
                  "description": "string containing the location (URL) of the web page"
                },
                {
                  "key": "useDuration",
                  "value": "{}",
                  "disabled": false,
                  "description": "(0, 1) Select 1 only if you will provide duration parameter as well"
                }
              ]
            },
            "description": "Add a new Web page Widget to the specified playlist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6b65c5e7-5c35-46b5-bfa1-90d5170e98c5"
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