---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Display Delete
  description: Delete a Display
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
  /display/{displayId}:
    put:
      summary: Display Edit
      description: Edit a Display
      operationId: displayEdit
      x-api-path-slug: displaydisplayid-put
      parameters:
      - in: formData
        name: alertTimeout
        description: How long in seconds should this display wait before alerting
          when it hasnt connected
      - in: formData
        name: auditingUntil
        description: A date this Display records auditing information until
      - in: formData
        name: broadCastAddress
        description: The BroadCast Address for this Display - used by Wake On LAN
      - in: formData
        name: cidr
        description: The CIDR configuration for this Display
      - in: formData
        name: clearCachedData
        description: Clear all Cached data for this display
      - in: formData
        name: defaultLayoutId
        description: A Layout ID representing the Default Layout for this Display
      - in: formData
        name: description
        description: A description of the Display
      - in: formData
        name: display
        description: The Display Name
      - in: path
        name: displayId
        description: The Display ID
      - in: formData
        name: displayProfileId
        description: The Display Settings Profile ID
      - in: formData
        name: emailAlert
        description: Flag indicating whether the Display generates up/down email alerts
      - in: formData
        name: incSchedule
        description: Flag indicating whether the Default Layout should be included
          in the Schedule
      - in: formData
        name: latitude
        description: The Latitude of this Display
      - in: formData
        name: license
        description: The hardwareKey to use as the licence key for this Display
      - in: formData
        name: licensed
        description: Flag indicating whether this display is licensed
      - in: formData
        name: longitude
        description: The Longitude of this Display
      - in: formData
        name: rekeyXmr
        description: Clear the cached XMR configuration and send a rekey
      - in: formData
        name: secureOn
        description: The secure on configuration for this Display
      - in: formData
        name: tags
        description: A comma separated list of tags for this item
      - in: formData
        name: timeZone
        description: The timezone for this display, or empty to use the CMS timezone
      - in: formData
        name: wakeOnLanEnabled
        description: Flag indicating if Wake On LAN is enabled for this Display
      - in: formData
        name: wakeOnLanTime
        description: A h:i string representing the time that the Display should receive
          its Wake on LAN command
      responses:
        200:
          description: OK
      tags:
      - Display
      - Edit
    delete:
      summary: Display Delete
      description: Delete a Display
      operationId: displayDelete
      x-api-path-slug: displaydisplayid-delete
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      responses:
        200:
          description: OK
      tags:
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