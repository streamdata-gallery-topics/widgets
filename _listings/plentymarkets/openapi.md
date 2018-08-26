---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/shop_builder/widgets:
    get:
      summary: List all widgets provided by all frontend plugins of a given plugin
        set.
      description: List all widgets provided by all frontend plugins of a given plugin
        set..
      operationId: getRestShopBuilderWgets
      x-api-path-slug: restshop-builderwidgets-get
      parameters:
      - in: query
        name: identifier
        description: Filter results by widget identifier
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
        200:
          description: OK
      tags:
      - List
      - ""
      - Widgets
      - Provided
      - By
      - ""
      - Frontend
      - Plugins
      - Of
      - Given
      - Plugin
      - Set
---