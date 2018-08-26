{
  "info": {
    "name": "Xibo API Add a Weather Widget",
    "_postman_id": "0ea454e7-91a4-47e8-9332-28b556a9e445",
    "description": "Add a new Weather Widget to the specified playlist",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Weather",
      "item": [
        {
          "id": "5148fe1a-e5f1-4973-9b82-a00de9234f97",
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
              "id": "f172d038-29eb-463d-bf03-752e7fd19105"
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