---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Return all Negotiator keys for the side bar display.
  version: 1.0.0
  description: Return all negotiator keys for the side bar display..
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/group/{id}/displaysettings:
    put:
      summary: Edit Display settings for the Group. Primarily shown in the GroupHub
        e.g. the icon and background image.
      description: Edit display settings for the group. primarily shown in the grouphub
        e.g. the icon and background image..
      operationId: Group_SetDisplaySettingsByidBygroupDisplaySettingsDataContract
      x-api-path-slug: apigroupiddisplaysettings-put
      parameters:
      - in: body
        name: groupDisplaySettingsDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Display
      - Settingsthe
      - Group
      - ""
      - Primarily
      - Shown
      - In
      - GroupHub
      - E
      - G
      - ""
      - Icon
      - Background
      - Image
  /api/negotiator/my/keys:
    get:
      summary: Return all Negotiator keys for the side bar display.
      description: Return all negotiator keys for the side bar display..
      operationId: Negotiator_KeysBypageSizeBypageNumberBycheckedOutOnly
      x-api-path-slug: apinegotiatormykeys-get
      parameters:
      - in: query
        name: checkedOutOnly
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Return
      - ""
      - Negotiator
      - Keysthe
      - Side
      - Bar
      - Display
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