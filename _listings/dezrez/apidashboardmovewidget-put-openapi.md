---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Move widget onto another dashboard
  version: 1.0.0
  description: Move widget onto another dashboard.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/dashboard/{id}/removewidgets:
    put:
      summary: Remove widgets from a dashboard
      description: Remove widgets from a dashboard.
      operationId: Dashboard_RemoveWidgetsFromDashboardByid
      x-api-path-slug: apidashboardidremovewidgets-put
      parameters:
      - in: path
        name: id
        description: Dashboard Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Widgets
      - From
      - Dashboard
  /api/dashboard/{id}/setwidget:
    put:
      summary: Add widget to dashboard
      description: Add widget to dashboard.
      operationId: Dashboard_SetWidgetByidBydataContract
      x-api-path-slug: apidashboardidsetwidget-put
      parameters:
      - in: body
        name: dataContract
        description: Widget to be added to dashboard
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Dashboard Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Widget
      - To
      - Dashboard
  /api/dashboard/{id}/deletewidget/{widgetId}:
    delete:
      summary: Delete widget on dashboard
      description: Delete widget on dashboard.
      operationId: Dashboard_DeleteWidgetByidBywidgetId
      x-api-path-slug: apidashboardiddeletewidgetwidgetid-delete
      parameters:
      - in: path
        name: id
        description: Dashboard Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: widgetId
        description: Widget Id to be deleted
      responses:
        200:
          description: OK
      tags:
      - Widget
      - "On"
      - Dashboard
  /api/dashboard/movewidget:
    put:
      summary: Move widget onto another dashboard
      description: Move widget onto another dashboard.
      operationId: Dashboard_MoveWidgetBydataContract
      x-api-path-slug: apidashboardmovewidget-put
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Move
      - Widget
      - Onto
      - Another
      - Dashboard
  /api/dashboard/{id}/setlayout:
    put:
      summary: Set widget layout on dashboards
      description: Set widget layout on dashboards.
      operationId: Dashboard_SetWidgetLayoutByidBylayouts
      x-api-path-slug: apidashboardidsetlayout-put
      parameters:
      - in: path
        name: id
        description: Dashboard Id
      - in: body
        name: layouts
        description: Array of layout objects
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Widget
      - Layout
      - "On"
      - Dashboards
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