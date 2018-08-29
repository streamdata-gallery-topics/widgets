---
swagger: "2.0"
x-collection-name: Reviewshake
x-complete: 0
info:
  title: Reviewshake List widgets
  description: List widgets.
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