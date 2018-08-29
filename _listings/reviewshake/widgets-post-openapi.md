---
swagger: "2.0"
x-collection-name: Reviewshake
x-complete: 0
info:
  title: Reviewshake Create widget
  description: |-
    You can create the following widget types:

    1. List
    2. Caroussel
    3. Slider
    4. Grid
    5. Quote
  version: "1.0"
host: subdomain.reviewshake.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /widgets:
    get:
      summary: List widgets
      description: List widgets.
      operationId: WidgetsGet
      x-api-path-slug: widgets-get
      parameters:
      - in: header
        name: Content-Type
      - in: header
        name: X-Spree-Token
      responses:
        200:
          description: OK
      tags:
      - List
      - Widgets
    post:
      summary: Create widget
      description: |-
        You can create the following widget types:

        1. List
        2. Caroussel
        3. Slider
        4. Grid
        5. Quote
      operationId: WidgetsPost
      x-api-path-slug: widgets-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: X-Spree-Token
      responses:
        200:
          description: OK
      tags:
      - Widget
  /widgets/<id>:
    delete:
      summary: Delete widget
      description: Delete widget.
      operationId: WidgetsIdDelete
      x-api-path-slug: widgetsid-delete
      parameters:
      - in: header
        name: Content-Type
      - in: header
        name: X-Spree-Token
      responses:
        200:
          description: OK
      tags:
      - Widget
    put:
      summary: Update widget
      description: Update widget.
      operationId: WidgetsIdPut
      x-api-path-slug: widgetsid-put
      parameters:
      - in: header
        name: Content-Type
      - in: header
        name: X-Spree-Token
      responses:
        200:
          description: OK
      tags:
      - Widget
  /widgets/1:
    get:
      summary: View widget
      description: View widget.
      operationId: Widgets1Get
      x-api-path-slug: widgets1-get
      parameters:
      - in: header
        name: Content-Type
      - in: header
        name: X-Spree-Token
      responses:
        200:
          description: OK
      tags:
      - View
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