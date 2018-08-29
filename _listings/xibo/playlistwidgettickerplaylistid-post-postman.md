{
  "info": {
    "name": "Xibo API Add a ticker Widget",
    "_postman_id": "9985df1b-7bd1-4986-adfa-770f4c90ba1b",
    "description": "Add a new ticker Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Ticker",
      "item": [
        {
          "id": "7ae3394a-10d9-4677-b005-7c7a6c6bf716",
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
              "id": "d6a3d80b-7253-4c93-8295-5f62e1098a40"
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