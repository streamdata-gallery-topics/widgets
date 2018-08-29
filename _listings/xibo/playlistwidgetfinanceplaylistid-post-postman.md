{
  "info": {
    "name": "Xibo API Add a Finance Widget",
    "_postman_id": "a07e05c9-3502-4aba-bb16-b4fb4489f1ca",
    "description": "Add a new Finance Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Order",
      "item": [
        {
          "id": "30c83a62-4262-47ae-ba4e-05f2b9b9a3a1",
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
              "id": "8c1b2688-5967-47fd-a7bb-6ef1fb8e97b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "b8474ad6-eaf1-4574-86a5-bc1634a42055",
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
              "id": "f2e8afe4-e01c-48ae-99c2-2fee9b6741be"
            }
          ]
        }
      ]
    },
    {
      "name": "Widget",
      "item": [
        {
          "id": "cd1e9524-d49b-40c4-ab95-28ff1ba5035f",
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
              "id": "d77c97f2-99fb-4b22-9da7-1ab2f5a45d16"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersedting",
      "item": [
        {
          "id": "6c50bd35-a86e-4beb-937d-cbbbda459ea1",
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
              "id": "c67cb0f4-9975-46de-a251-ab7fed8c5bd6"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "12c2d24f-7068-4739-9930-8e1a62ba0166",
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
              "id": "8a231eb4-6ad1-440f-8bc8-60f7fcc051a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Playlist",
      "item": [
        {
          "id": "6e80aa7c-8b9d-4f07-9607-bba06c7091f7",
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
              "id": "5291fbd7-b0a5-4b07-a185-579f64c4e3dd"
            }
          ]
        }
      ]
    },
    {
      "name": "Parametersediting",
      "item": [
        {
          "id": "cee79222-c76b-48b6-90d7-5536d4246b95",
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
              "id": "ceaceee3-1b3e-4153-9365-9ffe7c669b7c"
            }
          ]
        }
      ]
    },
    {
      "name": "Chart",
      "item": [
        {
          "id": "e8328a30-f627-4ce1-bc80-46267b113bdc",
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
              "id": "fb61dfd2-8c59-42a3-89e2-82c847469b0e"
            }
          ]
        }
      ]
    },
    {
      "name": "Clock",
      "item": [
        {
          "id": "9d17b4ce-5e2b-482a-bad3-413d5562a59a",
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
              "id": "7c001cad-0104-4cc8-baa0-cfe91349ce4c"
            }
          ]
        }
      ]
    },
    {
      "name": "Currencies",
      "item": [
        {
          "id": "e740db47-3aa7-4cef-a9d8-7e8d09ea3239",
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
              "id": "67be0070-2665-4f78-9e7a-0bdac5c40cc0"
            }
          ]
        }
      ]
    },
    {
      "name": "DataSetView",
      "item": [
        {
          "id": "a74b8e01-f757-4e87-b70d-7d9d421d7338",
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
              "id": "cd452207-48af-42bd-b2dd-3e7bd0f75d5c"
            }
          ]
        }
      ]
    },
    {
      "name": "Embedded",
      "item": [
        {
          "id": "731716ee-2b53-42f8-8ee9-961c2047cca8",
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
              "id": "41325f09-9c96-45b5-bd70-65134877209a"
            }
          ]
        }
      ]
    },
    {
      "name": "Finance",
      "item": [
        {
          "id": "b4006920-8c46-4ca0-94fe-a89487d93e97",
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
              "id": "076f9636-ee61-413f-9443-e1379f51f546"
            }
          ]
        }
      ]
    },
    {
      "name": "Weather",
      "item": [
        {
          "id": "b68114a1-a677-431b-afa3-47639f5ce510",
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
              "id": "ee8ed813-c991-456f-9faa-fcb23f9d47eb"
            }
          ]
        }
      ]
    },
    {
      "name": "Google",
      "item": [
        {
          "id": "1fa951be-3bbb-4c95-a55d-2d4a681b6afd",
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
              "id": "08da0d61-39d5-4d9c-b5d2-98da75938961"
            }
          ]
        }
      ]
    },
    {
      "name": "HLS",
      "item": [
        {
          "id": "050b868f-915c-4a33-b850-a84245b9236c",
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
              "id": "156f54d5-d077-4725-a835-6b1a163b5145"
            }
          ]
        }
      ]
    },
    {
      "name": "Local",
      "item": [
        {
          "id": "6efa7052-e810-4cf2-9f8d-799628edcc0a",
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
              "id": "4dfcfd21-0328-4027-a4bc-7fa6d90acba4"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "c75123ee-7ed1-4467-8dd8-c7e39567effd",
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
              "id": "38ea189c-c4bc-4cb7-aff9-a629816548df"
            }
          ]
        }
      ]
    },
    {
      "name": "Shell",
      "item": [
        {
          "id": "7532f91e-cf60-4de4-9ad9-9676023390d2",
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
              "id": "1814c26d-37ad-4027-9711-fe4a1e8a7a89"
            }
          ]
        }
      ]
    },
    {
      "name": "Stocks",
      "item": [
        {
          "id": "07f4d083-482e-4e8f-b991-bba37881755f",
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
    