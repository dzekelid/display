---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Display Search
  description: Search Displays for this User
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
  /display:
    get:
      summary: Display Search
      description: Search Displays for this User
      operationId: displaySearch
      x-api-path-slug: display-get
      parameters:
      - in: formData
        name: authorised
        description: Filter by authorised flag
      - in: formData
        name: clientVersion
        description: Filter by Client Version
      - in: formData
        name: display
        description: Filter by Display Name
      - in: formData
        name: displayGroupId
        description: Filter by DisplayGroup Id
      - in: formData
        name: displayId
        description: Filter by Display Id
      - in: formData
        name: displayProfileId
        description: Filter by Display Profile
      - in: formData
        name: embed
        description: Embed related data, namely displaygroups
      - in: formData
        name: hardwareKey
        description: Filter by Hardware Key
      - in: formData
        name: macAddress
        description: Filter by Mac Address
      responses:
        200:
          description: OK
      tags:
      - Display
      - Search
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