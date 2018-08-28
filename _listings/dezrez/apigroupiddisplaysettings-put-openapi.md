---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Edit Display settings for the Group. Primarily shown in the GroupHub
    e.g. the icon and background image.
  version: 1.0.0
  description: Edit display settings for the group. primarily shown in the grouphub
    e.g. the icon and background image..
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