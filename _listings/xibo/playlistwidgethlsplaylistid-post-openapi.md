---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Add a HLS Widget
  description: Add a new HLS Widget to the specified playlist
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /playlist/order/{playlistId}:
    post:
      summary: Order Widgets
      description: Set the order of widgets in the Playlist
      operationId: playlistOrder
      x-api-path-slug: playlistorderplaylistid-post
      parameters:
      - in: path
        name: playlistId
        description: The Playlist ID to Order
      - in: formData
        name: widgets
        description: Array of widgetIds and positions - all widgetIds present in the
          playlist need to be passed in the call with their positions
      responses:
        200:
          description: OK
      tags:
      - Order
      - Widgets
  /playlist/widget/{widgetId}:
    put:
      summary: Edit a Widget
      description: Edit a Widget, please refer to individual widget Add documentation
        for module specific parameters
      operationId: WidgetEdit
      x-api-path-slug: playlistwidgetwidgetid-put
      parameters:
      - in: path
        name: widgetId
        description: The widget ID to edit
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Widget
    delete:
      summary: Delete a Widget
      description: Deleted a specified widget
      operationId: WidgetDelete
      x-api-path-slug: playlistwidgetwidgetid-delete
      parameters:
      - in: path
        name: widgetId
        description: The widget ID to delete
      responses:
        200:
          description: OK
      tags:
      - Widget
  /playlist/widget/{widgetId}/audio:
    put:
      summary: Parameters for edting/adding audio file to a specific widget
      description: Parameters for edting/adding audio file to a specific widget
      operationId: WidgetAssignedAudioEdit
      x-api-path-slug: playlistwidgetwidgetidaudio-put
      parameters:
      - in: formData
        name: loop
        description: Flag (0, 1) Should the audio loop if it finishes before the widget
          has finished?
      - in: formData
        name: mediaId
        description: Id of a audio file in CMS library you wish to add to a widget
      - in: formData
        name: volume
        description: Volume percentage(0-100) for this audio to play at
      - in: path
        name: widgetId
        description: Id of a widget to which you want to add audio or edit existing
          audio
      responses:
        200:
          description: OK
      tags:
      - Parametersedting
      - Adding
      - Audio
      - File
      - To
      - Specific
      - Widget
    delete:
      summary: Delete assigned audio widget
      description: Delete assigned audio widget from specified widget ID
      operationId: WidgetAudioDelete
      x-api-path-slug: playlistwidgetwidgetidaudio-delete
      parameters:
      - in: path
        name: widgetId
        description: Id of a widget from which you want to delete the audio from
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Audio
      - Widget
  /playlist/widget:
    get:
      summary: Playlist Widget Search
      description: Search widgets on a Playlist
      operationId: playlistSearch
      x-api-path-slug: playlistwidget-get
      parameters:
      - in: formData
        name: playlistId
        description: The Playlist ID to Search
      - in: formData
        name: widgetId
        description: The widget ID to Search
      responses:
        200:
          description: OK
      tags:
      - Playlist
      - Widget
      - Search
  /playlist/widget/audio/{playlistId}:
    post:
      summary: Parameters for editing existing audio widget on a layout
      description: Parameters for editing existing audio widget on a layout, for adding
        new audio, please refer to POST /library documentation
      operationId: WidgetAudioEdit
      x-api-path-slug: playlistwidgetaudioplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: loop
        description: Edit only - Flag (0, 1) Should the audio loop (only for duration
          > 0 )?
      - in: formData
        name: mute
        description: Edit only - Flag (0, 1) Should the audio be muted?
      - in: formData
        name: name
        description: Edit Only - The Widget name
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Audio
      - Widget
      - "On"
      - Layout
  /playlist/widget/chart/{playlistId}:
    post:
      summary: Add a Chart Widget
      description: Add a new Chart Widget to the specified playlist
      operationId: WidgetChartAdd
      x-api-path-slug: playlistwidgetchartplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: EDIT Only - Background Color
      - in: formData
        name: columnType
        description: EDIT only - Array of Column Types (x-axis, y-axis, series-identifier)
          to assign
      - in: formData
        name: dataSetColumnId
        description: EDIT only - Array of dataSetColumn IDs to assign
      - in: formData
        name: dataSetId
        description: Create Chart Widget using provided dataSetId of an existing dataSet
      - in: formData
        name: duration
        description: EDIT Only - The Chart Duration
      - in: formData
        name: filter
        description: EDIT Only - SQL clause for filter this dataSet
      - in: formData
        name: fontColor
        description: EDIT Only - Font Color
      - in: formData
        name: fontSize
        description: EDIT Only - Font Size
      - in: formData
        name: graphType
        description: EDIT only - Chart Type
      - in: formData
        name: legendPosition
        description: EDIT Only - Where should the Legend be Shown (top, left, right,
          bottom)
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: ordering
        description: EDIT Only - SQL clause for how this dataSet should be ordered
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: showLegend
        description: EDIT Only - Should the Legend be Shown
      - in: formData
        name: startYAtZero
        description: EDIT Only - Start the Y-Axis at 0
      - in: formData
        name: title
        description: EDIT Only - Chart title
      - in: formData
        name: updateInterval
        description: EDIT Only - Update interval in minutes
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      - in: formData
        name: useFilteringClause
        description: EDIT Only - flag (0,1) Use advanced filter clause - set to 1
          if filter is provided
      - in: formData
        name: useOrderingClause
        description: EDIT Only - flag (0,1) Use advanced order clause - set to 1 if
          ordering is provided
      - in: formData
        name: x-axis-label
        description: EDIT Only - Chart x-axis label
      - in: formData
        name: y-axis-label
        description: EDIT Only - Chart y-axis label
      responses:
        200:
          description: OK
      tags:
      - Chart
      - Widget
  /playlist/widget/clock/{playlistId}:
    post:
      summary: Add a Clock Widget
      description: Add a new Clock Widget to the specified playlist
      operationId: WidgetClockAdd
      x-api-path-slug: playlistwidgetclockplaylistid-post
      parameters:
      - in: formData
        name: ClockFace
        description: 'For Flip Clock, supported options: TwelveHourClock TwentyFourHourClock
          HourlyCounter MinuteCounter DailyCounter'
      - in: formData
        name: clockTypeId
        description: Type of a clock widget 1-Analogue, 2-Digital, 3-Flip clock
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: format
        description: For digital clock, format in which the time should be displayed
          example [HH:mm]
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: offset
        description: The offset in minutes that should be applied to the current time,
          if a counter is selected then date/time to run from in the format Y-m-d
          H:i:s
      - in: path
        name: playlistId
        description: The playlist ID to add a Clock widget to
      - in: formData
        name: showSeconds
        description: For Flip Clock, should the clock show seconds or not
      - in: formData
        name: themeId
        description: Flag (0 , 1) for Analogue clock the light and dark theme
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Clock
      - Widget
  /playlist/widget/currencies/{playlistId}:
    post:
      summary: Add a Currencies Widget
      description: Add a new Currencies Widget to the specified playlist
      operationId: WidgetCurrenciesAdd
      x-api-path-slug: playlistwidgetcurrenciesplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: base
        description: The base currency
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerPage
        description: A flag (0, 1), The duration specified is per page/item, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: items
        description: Items wanted
      - in: formData
        name: itemtemplate
        description: Template for each item, replaces [itemsTemplate] in main template,
          Pass only with overrideTemplate set to 1
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: mainTemplate
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: maxItemsPerPage
        description: This is the intended number of items on each page
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noRecordsMessage
        description: A message to display when there are no records returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Currencies widget
      - in: formData
        name: reverseConversion
        description: (0, 1) Select 1 if youd like your base currency to be used as
          the comparison currency youve entered
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: currencies1,
          currencies2'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: widgetOriginalHeight
        description: This is the intended Height of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalWidth
        description: This is the intended Width of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      responses:
        200:
          description: OK
      tags:
      - Currencies
      - Widget
  /playlist/widget/dataSetView/{playlistId}:
    post:
      summary: Add a dataSetView Widget
      description: Add a new dataSetView Widget to the specified playlist
      operationId: WidgetdataSetViewAdd
      x-api-path-slug: playlistwidgetdatasetviewplaylistid-post
      parameters:
      - in: formData
        name: dataSetColumnId
        description: EDIT only - Array of dataSetColumn IDs to assign
      - in: formData
        name: dataSetId
        description: Create dataSetView Widget using provided dataSetId of an existing
          dataSet
      - in: formData
        name: duration
        description: EDIT Only - The dataSetView Duration
      - in: formData
        name: filter
        description: EDIT Only - SQL clause for filter this dataSet
      - in: formData
        name: lowerLimit
        description: EDIT Only - Lower low limit for this dataSet, 0 for nor limit
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noDataMessage
        description: EDIT Only - A message to display when no data is returned from
          the source
      - in: formData
        name: ordering
        description: EDIT Only - SQL clause for how this dataSet should be ordered
      - in: formData
        name: overrideTemplate
        description: EDIT Only - flag (0, 1) override template checkbox
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: rowsPerPage
        description: EDIT Only - Number of rows per page, 0 for no pages
      - in: formData
        name: showHeadings
        description: EDIT Only - Should the table show Heading? (0,1)
      - in: formData
        name: templateId
        description: 'EDIT Only - Template youd like to apply, options available:
          empty, light-green'
      - in: formData
        name: updateInterval
        description: EDIT Only - Update interval in minutes
      - in: formData
        name: upperLimit
        description: EDIT Only - Upper low limit for this dataSet, 0 for nor limit
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      - in: formData
        name: useFilteringClause
        description: EDIT Only - flag (0,1) Use advanced filter clause - set to 1
          if filter is provided
      - in: formData
        name: useOrderingClause
        description: EDIT Only - flag (0,1) Use advanced order clause - set to 1 if
          ordering is provided
      responses:
        200:
          description: OK
      tags:
      - DataSetView
      - Widget
  /playlist/widget/embedded/{playlistId}:
    post:
      summary: Add a Embedded Widget
      description: Add a new Embedded Widget to the specified playlist
      operationId: WidgetEmbeddedAdd
      x-api-path-slug: playlistwidgetembeddedplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: embedHtml
        description: HTML to embed
      - in: formData
        name: embedScript
        description: HEAD content to Embed (including script tags)
      - in: formData
        name: embedStyle
        description: Custom Style Sheets (CSS)
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add an Embedded Widget
      - in: formData
        name: scaleContent
        description: Flag (0,1) - Should the embedded content be scaled along with
          the layout?
      - in: formData
        name: transparency
        description: Flag (0,1) - Should the HTML be shown with transparent background?
          - not available on Windows Clients
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Embedded
      - Widget
  /playlist/widget/finance/{playlistId}:
    post:
      summary: Add a Finance Widget
      description: Add a new Finance Widget to the specified playlist
      operationId: WidgetFinanceAdd
      x-api-path-slug: playlistwidgetfinanceplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per item, otherwise
          the widget duration is divided between the number of items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft'
      - in: formData
        name: item
        description: Items wanted, can be comma separated (example EURUSD, GBPUSD),
          pass only with overrideTemplate set to 1
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noRecordsMessage
        description: A message to display when there are no records returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Finance widget
      - in: formData
        name: resultIdentifier
        description: The name of the result identifier returned by the YQL, pass only
          with overrideTemplate set to 1
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: template
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: currency-simple,
          stock-simple'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: yql
        description: The YQL query to use for data, pass only with overrideTemplate
          set to 1
      responses:
        200:
          description: OK
      tags:
      - Finance
      - Widget
  /playlist/widget/forecastIo/{playlistId}:
    post:
      summary: Add a Weather Widget
      description: Add a new Weather Widget to the specified playlist
      operationId: WidgetWeatherAdd
      x-api-path-slug: playlistwidgetforecastioplaylistid-post
      parameters:
      - in: formData
        name: currentTemplate
        description: Current template, Pass only with overrideTemplate set to 1
      - in: formData
        name: dailyTemplate
        description: Replaces [dailyForecast] in main template, Pass only with overrideTemplate
          set to 1
      - in: formData
        name: dayConditionsOnly
        description: Flag (0, 1) Would you like to only show the Daytime weather conditions
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: lang
        description: Language youd like to use, supported languages ar, az, be, bs,
          cs, de, en, el, es, fr, hr, hu, id, it, is, kw, nb, nl, pl, pt, ru, sk,
          sr, sv, tet, tr, uk, x-pig-latin, zh, zh-tw
      - in: formData
        name: latitude
        description: The latitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: longitude
        description: The longitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Weather widget
      - in: formData
        name: styleSheet
        description: Optional StyleSheet, Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: weather-module0-5day,
          weather-module0-singleday, weather-module0-singleday2, weather-module1l,
          weather-module1p, weather-module2l, weather-module2p, weather-module3l,
          weather-module3p, weather-module4l, weather-module4p, weather-module5l,
          weather-module6v, weather-module6h'
      - in: formData
        name: units
        description: 'Units you would like to use, available options: auto, ca, si,
          uk2, us'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDisplayLocation
        description: Flag (0, 1) Use the location configured on display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: widgetOriginalHeight
        description: This is the intended Height of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalWidth
        description: This is the intended Width of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Widget
  /playlist/widget/googleTraffic/{playlistId}:
    post:
      summary: Add a Google Traffic Widget
      description: Add a new Google traffic Widget to the specified playlist
      operationId: WidgetGoogleTrafficAdd
      x-api-path-slug: playlistwidgetgoogletrafficplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: latitude
        description: The latitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: longitude
        description: The longitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget
      - in: formData
        name: useDisplayLocation
        description: Flag (0, 1) Use the location configured on display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: zoom
        description: How far should the map be zoomed in? The higher the number the
          closer the zoom, 1 represents entire globe
      responses:
        200:
          description: OK
      tags:
      - Google
      - Traffic
      - Widget
  /playlist/widget/hls/{playlistId}:
    post:
      summary: Add a HLS Widget
      description: Add a new HLS Widget to the specified playlist
      operationId: WidgetHlsAdd
      x-api-path-slug: playlistwidgethlsplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: mute
        description: Flag (0, 1) Should the video be muted?
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: transparency
        description: Flag (0, 1), This causes some android devices to switch to a
          hardware accelerated web view
      - in: formData
        name: uri
        description: URL to HLS video stream
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select only if you will provide duration parameter
          as well
      responses:
        200:
          description: OK
      tags:
      - HLS
      - Widget
  /playlist/widget/localVideo/{playlistId}:
    post:
      summary: Add a Local Video Widget
      description: Add a new Local Video Widget to the specified playlist
      operationId: WidgetLocalVideoAdd
      x-api-path-slug: playlistwidgetlocalvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: mute
        description: Flag (0, 1) Should the video be muted?
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: uri
        description: A local file path or URL to the video
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Local
      - Video
      - Widget
  /playlist/widget/notificationview/{playlistId}:
    post:
      summary: Add a Notification Widget
      description: Add a new Notification Widget to the specified playlist
      operationId: WidgetNotificationAdd
      x-api-path-slug: playlistwidgetnotificationviewplaylistid-post
      parameters:
      - in: formData
        name: age
        description: The maximum notification age in minutes - 0 for all
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per page/item, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: embedStyle
        description: Custom Style Sheets (CSS)
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noDataMessage
        description: Message to show when no notifications are available
      - in: path
        name: playlistId
        description: The playlist ID to add an Notification Widget
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Widget
  /playlist/widget/shellCommand/{playlistId}:
    post:
      summary: Add a Shell Command Widget
      description: Add a new Shell Command Widget to the specified playlist
      operationId: WidgetShellCommandAdd
      x-api-path-slug: playlistwidgetshellcommandplaylistid-post
      parameters:
      - in: formData
        name: commandCode
        description: Enter a reference code for exiting command in CMS
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: launchThroughCmd
        description: flag (0,1) Windows only, Should the player launch this command
          through the windows command line (cmd
      - in: formData
        name: linuxCommand
        description: Enter a Android / Linux command line compatible command
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: terminateCommand
        description: flag (0,1) Should the player forcefully terminate the command
          after the duration specified, 0 to let the command terminate naturally
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: useTaskkill
        description: flag (0,1) Windows only, should the player use taskkill to terminate
          commands
      - in: formData
        name: windowsCommand
        description: Enter a Windows command line compatible command
      responses:
        200:
          description: OK
      tags:
      - Shell
      - Command
      - Widget
  /playlist/widget/stocks/{playlistId}:
    post:
      summary: Add a Stocks Widget
      description: Add a new Stocks Widget to the specified playlist
      operationId: WidgetStocksAdd
      x-api-path-slug: playlistwidgetstocksplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerPage
        description: A flag (0, 1), The duration specified is per page, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: items
        description: Items wanted, can be comma separated
      - in: formData
        name: itemtemplate
        description: Template for each item, replaces [itemsTemplate] in main template,
          Pass only with overrideTemplate set to 1
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: mainTemplate
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: maxItemsPerPage
        description: This is the intended number of items on each page
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noRecordsMessage
        description: A message to display when there are no records returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Stocks widget
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: stocks1, stocks2'
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Stocks
      - Widget
  /playlist/widget/text/{playlistId}:
    post:
      summary: Add a Text Widget
      description: Add a new Text Widget to the specified playlist
      operationId: WidgetTextAdd
      x-api-path-slug: playlistwidgettextplaylistid-post
      parameters:
      - in: formData
        name: backgroundcolor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight, marqueeLeft'
      - in: formData
        name: javaScript
        description: Optional JavaScript
      - in: formData
        name: marqueeInlineSelector
        description: The selector to use for stacking marquee items in a line when
          scrolling left/right
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: text
        description: Enter the text to display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Text
      - Widget
  /playlist/widget/ticker/{playlistId}:
    post:
      summary: Add a ticker Widget
      description: Add a new ticker Widget to the specified playlist
      operationId: WidgetTickerAdd
      x-api-path-slug: playlistwidgettickerplaylistid-post
      parameters:
      - in: formData
        name: allowedAttributes
        description: EDIT Only and SourceId=1 - A comma separated list of attributes
          that should not be stripped from the feed
      - in: formData
        name: backgroundColor
        description: Edit only - A HEX color to use as the background color of this
          widget
      - in: formData
        name: copyright
        description: EDIT Only and SourceId=1 - Copyright information to display as
          the last item in this feed
      - in: formData
        name: css
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
          or with sourceId=2
      - in: formData
        name: dataSetId
        description: For sourceId=2, Create ticker Widget using provided dataSetId
          of an existing dataSet
      - in: formData
        name: dateFormat
        description: EDIT Only - The date format to apply to all dates returned by
          the ticker
      - in: formData
        name: disableDateSort
        description: EDIT Only, SourceId=1 - Should the date sort applied to the feed
          be disabled?
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per item, otherwise
          it is per feed
      - in: formData
        name: effect
        description: 'Edit only - Effect that will be used to transitions between
          items, available options: fade, fadeout, scrollVert, scollHorz, flipVert,
          flipHorz, shuffle, tileSlide, tileBlind, marqueeUp, marqueeDown, marqueeRight,
          marqueeLeft'
      - in: formData
        name: filter
        description: EDIT Only, SourceId=2 - SQL clause for filter this dataSet
      - in: formData
        name: itemsPerPage
        description: EDIT Only - When in single mode, how many items per page should
          be shown
      - in: formData
        name: itemsSideBySide
        description: A flag (0, 1), Should items be shown side by side
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: lowerLimit
        description: EDIT Only, SourceId=2 - Lower low limit for this dataSet, 0 for
          nor limit
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noDataMessage
        description: EDIT Only - A message to display when no data is returned from
          the source
      - in: formData
        name: numItems
        description: EDIT Only and SourceId=1 - The number of RSS items you want to
          display
      - in: formData
        name: ordering
        description: EDIT Only, SourceId=2- SQL clause for how this dataSet should
          be ordered
      - in: formData
        name: overrideTemplate
        description: EDIT Only, SourceId=1 - flag (0, 1) override template checkbox
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: randomiseItems
        description: A flag (0, 1), whether to randomise the feed
      - in: formData
        name: sourceId
        description: Add only - 1 for rss feed, 2 for dataset
      - in: formData
        name: speed
        description: Edit only - The transition speed of the selected effect in milliseconds
          (1000 = normal) or the Marquee speed in a low to high scale (normal = 1)
      - in: formData
        name: stripTags
        description: EDIT Only and SourceId=1 - A comma separated list of attributes
          that should be stripped from the feed
      - in: formData
        name: takeItemsFrom
        description: 'EDIT Only and SourceId=1 - Take the items form the beginning
          or the end of the list, available options: start, end'
      - in: formData
        name: template
        description: Template for each item, replaces [itemsTemplate] in main template,
          Pass only with overrideTemplate set to 1 or with sourceId=2
      - in: formData
        name: templateId
        description: 'EDIT Only, SourceId=1 - Template youd like to apply, options
          available: title-only, prominent-title-with-desc-and-name-separator, media-rss-with-title,
          media-rss-wth-left-hand-text, media-rss-image-only'
      - in: formData
        name: textDirection
        description: 'EDIT Only, SourceId=1 - Which direction does the text in the
          feed use? Available options: ltr, rtl'
      - in: formData
        name: updateInterval
        description: EDIT Only - Update interval in minutes
      - in: formData
        name: upperLimit
        description: EDIT Only, SourceId=2 - Upper low limit for this dataSet, 0 for
          nor limit
      - in: formData
        name: uri
        description: For sourceId=1, the link for the rss feed
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: useFilteringClause
        description: EDIT Only, SourceId=2 - flag (0,1) Use advanced filter clause
          - set to 1 if filter is provided
      - in: formData
        name: useOrderingClause
        description: EDIT Only, SourceId=2 - flag (0,1) Use advanced order clause
          - set to 1 if ordering is provided
      responses:
        200:
          description: OK
      tags:
      - Ticker
      - Widget
  /playlist/widget/twitter/{playlistId}:
    post:
      summary: Add a Twitter Widget
      description: Add a new Twitter Widget to the specified playlist
      operationId: WidgetTwitterAdd
      x-api-path-slug: playlistwidgettwitterplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: durationIsPerItem
        description: A flag (0, 1), The duration specified is per page/item, otherwise
          the widget duration is divided between the number of pages/items
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: itemsPerPage
        description: EDIT Only - When in single mode, how many items per page should
          be shown
      - in: formData
        name: javaScript
        description: Optional JavaScript, Pass only with overrideTemplate set to 1
      - in: formData
        name: language
        description: Language in which tweets should be returned
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noTweetsMessage
        description: A message to display when there are no tweets returned by the
          search query
      - in: formData
        name: overrideTemplate
        description: flag (0, 1) set to 0 and use templateId or set to 1 and provide
          whole template in the next parameters
      - in: path
        name: playlistId
        description: The playlist ID to add a Twitter widget
      - in: formData
        name: removeHashtags
        description: Flag (0, 1) Should the hashtags (#something) be removed from
          the tweet text
      - in: formData
        name: removeMentions
        description: Flag (0, 1) Should mentions (@someone) be removed from the tweet
          text?
      - in: formData
        name: removeUrls
        description: Flag (0, 1) Should the URLs be removed from the tweet text?
      - in: formData
        name: resultContent
        description: 'Intended content Type, available Options: 0 - All Tweets 1 -
          Tweets with the text only content 2 - Tweets with the text and image content'
      - in: formData
        name: resultType
        description: 1 - Mixed, 2 -Recent 3 - Popular, Recent shows only recent tweets,
          Popular the most popular tweets and Mixed included both popular and recent
      - in: formData
        name: searchTerm
        description: Twitter search term, you can test your search term in twitter
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: styleSheet
        description: Optional StyleSheet Pass only with overrideTemplate set to 1
      - in: formData
        name: template
        description: Main template, Pass only with overrideTemplate set to 1
      - in: formData
        name: templateId
        description: 'Use pre-configured templates, available options: full-timeline-np,
          full-timeline, tweet-only, tweet-with-profileimage-left, tweet-with-profileimage-right,
          tweet-1, tweet-2, tweet-4'
      - in: formData
        name: tweetCount
        description: The number of tweets to return
      - in: formData
        name: tweetDistance
        description: Distance in miles that the tweets should be returned from
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: widgetOriginalHeight
        description: This is the intended Height of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalPadding
        description: This is the intended Padding of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      - in: formData
        name: widgetOriginalWidth
        description: This is the intended Width of the template and is used to scale
          the Widget within its region when the template is applied, Pass only with
          overrideTemplate set to 1
      responses:
        200:
          description: OK
      tags:
      - Twitter
      - Widget
  /playlist/widget/twittermetro/{playlistId}:
    post:
      summary: Add a Twitter Metro Widget
      description: Add a new Twitter Metro Widget to the specified playlist
      operationId: WidgetTwitterMetroAdd
      x-api-path-slug: playlistwidgettwittermetroplaylistid-post
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this widget
      - in: formData
        name: colorTemplateId
        description: 'Use pre-configured templates, available options: default, full,
          gray, light, soft, vivid'
      - in: formData
        name: dateFormat
        description: The format to apply to all dates returned by he widget
      - in: formData
        name: duration
        description: Widget Duration
      - in: formData
        name: effect
        description: 'Effect that will be used to transitions between items, available
          options: fade, fadeout, scrollVert, scollHorz, flipVert, flipHorz, shuffle,
          tileSlide, tileBlind'
      - in: formData
        name: language
        description: Language in which tweets should be returned
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: noTweetsMessage
        description: A message to display when there are no tweets returned by the
          search query
      - in: formData
        name: overrideColorTemplate
        description: flag (0, 1) set to 0 and use colorTemplateId or set to 1 and
          provide colours to use in templateColours parameter
      - in: path
        name: playlistId
        description: The playlist ID to add a Twitter Metro widget
      - in: formData
        name: removeHashtags
        description: Flag (0, 1) Should the hashtags (#something) be removed from
          the tweet text
      - in: formData
        name: removeMentions
        description: Flag (0, 1) Should mentions (@someone) be removed from the tweet
          text?
      - in: formData
        name: removeRetweets
        description: Flag (0, 1) Should retweets be filtered?
      - in: formData
        name: removeUrls
        description: Flag (0, 1) Should the URLs be removed from the tweet text?
      - in: formData
        name: resultContent
        description: 'Intended content Type, available Options: 0 - All Tweets 1 -
          Tweets with the text only content 2 - Tweets with the text and image content'
      - in: formData
        name: resultType
        description: 1 - Mixed, 2 -Recent 3 - Popular, Recent shows only recent tweets,
          Popular the most popular tweets and Mixed included both popular and recent
      - in: formData
        name: searchTerm
        description: Twitter search term, you can test your search term in twitter
      - in: formData
        name: speed
        description: The transition speed of the selected effect in milliseconds (1000
          = normal)
      - in: formData
        name: templateColours
        description: 'Provide a string of new HEX colour codes to use, separated by
          |, for example: #e0d2c8|#5e411d|#fccf12|#82ff00|#64bae8'
      - in: formData
        name: tweetCount
        description: The number of tweets to return
      - in: formData
        name: tweetDistance
        description: Distance in miles that the tweets should be returned from
      - in: formData
        name: updateInterval
        description: Update interval in minutes, should be kept as high as possible,
          if data change once per hour, this should be set to 60
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Twitter
      - Metro
      - Widget
  /playlist/widget/videoin/{playlistId}:
    post:
      summary: Add a Video In Widget
      description: Add a new Video In Widget to the specified playlist
      operationId: WidgetVideoInAdd
      x-api-path-slug: playlistwidgetvideoinplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: sourceId
        description: 'Which device input should be shown? available options: HDMI,
          RGB, DVI, DP, OPS'
      - in: formData
        name: useDuration
        description: Flag (0, 1) Select only if you will provide duration parameter
          as well
      responses:
        200:
          description: OK
      tags:
      - Video
      - In
      - Widget
  /playlist/widget/webpage/{playlistId}:
    post:
      summary: Add a Web page Widget
      description: Add a new Web page Widget to the specified playlist
      operationId: WidgetWebpageAdd
      x-api-path-slug: playlistwidgetwebpageplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Web page Duration
      - in: formData
        name: modeId
        description: The mode option for Web page, 1- Open Natively, 2- Manual Position,
          3- Best Ft
      - in: formData
        name: name
        description: Optional Widget Name
      - in: formData
        name: offsetLeft
        description: For Manual position, the starting point from the left in pixels
      - in: formData
        name: offsetTop
        description: For Manual position, the starting point from the Top in pixels
      - in: formData
        name: pageHeight
        description: For Manual Position and Best Fit, The height of the page - if
          empty it will use region height
      - in: formData
        name: pageWidth
        description: For Manual Position and Best Fit, The width of the page - if
          empty it will use region width
      - in: path
        name: playlistId
        description: The playlist ID to add a Web page to
      - in: formData
        name: scaling
        description: For Manual position the percentage to scale the Web page (0-100)
      - in: formData
        name: transparency
        description: flag (0,1) should the HTML be shown with a transparent background?
      - in: formData
        name: uri
        description: string containing the location (URL) of the web page
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Web
      - Page
      - Widget
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---