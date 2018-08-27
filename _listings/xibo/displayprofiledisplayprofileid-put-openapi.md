---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Edit Display Profile
  description: Edit a Display Profile
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
  /displaygroup:
    get:
      summary: Get Display Groups
      description: ""
      operationId: displayGroupSearch
      x-api-path-slug: displaygroup-get
      parameters:
      - in: formData
        name: displayGroup
        description: Filter by DisplayGroup Name
      - in: formData
        name: displayGroupId
        description: Filter by DisplayGroup Id
      - in: formData
        name: displayId
        description: Filter by DisplayGroups containing a specific display
      - in: formData
        name: dynamicCriteria
        description: Filter by DisplayGroups containing a specific dynamic criteria
      - in: formData
        name: forSchedule
        description: Should the list be refined for only those groups the User can
          Schedule against?
      - in: formData
        name: isDisplaySpecific
        description: Filter by whether the Display Group belongs to a Display or is
          user created
      - in: formData
        name: nestedDisplayId
        description: Filter by DisplayGroups containing a specific display in there
          nesting
      responses:
        200:
          description: OK
      tags:
      - Display
      - Groups
    post:
      summary: Add a Display Group
      description: Add a new Display Group to the CMS
      operationId: displayGroupAdd
      x-api-path-slug: displaygroup-post
      parameters:
      - in: formData
        name: description
        description: The Display Group Description
      - in: formData
        name: displayGroup
        description: The Display Group Name
      - in: formData
        name: dynamicContent
        description: The filter criteria for this dynamic group
      - in: formData
        name: isDynamic
        description: Flag indicating whether this DisplayGroup is Dynamic
      - in: formData
        name: tags
        description: A comma separated list of tags for this item
      responses:
        200:
          description: OK
      tags:
      - Display
      - Group
  /displaygroup/{displayGroupId}:
    put:
      summary: Edit a Display Group
      description: Edit an existing Display Group identified by its Id
      operationId: displayGroupEdit
      x-api-path-slug: displaygroupdisplaygroupid-put
      parameters:
      - in: formData
        name: description
        description: The Display Group Description
      - in: formData
        name: displayGroup
        description: The Display Group Name
      - in: path
        name: displayGroupId
        description: The displayGroupId to edit
      - in: formData
        name: dynamicCriteria
        description: The filter criteria for this dynamic group
      - in: formData
        name: isDynamic
        description: Flag indicating whether this DisplayGroup is Dynamic
      - in: formData
        name: tags
        description: A comma separated list of tags for this item
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Display
      - Group
    delete:
      summary: Delete a Display Group
      description: Delete an existing Display Group identified by its Id
      operationId: displayGroupDelete
      x-api-path-slug: displaygroupdisplaygroupid-delete
      parameters:
      - in: path
        name: displayGroupId
        description: The displayGroupId to delete
      responses:
        200:
          description: OK
      tags:
      - Display
      - Group
  /displaygroup/{displayGroupId}/display/assign:
    post:
      summary: Assign one or more Displays to a Display Group
      description: Adds the provided Displays to the Display Group
      operationId: displayGroupDisplayAssign
      x-api-path-slug: displaygroupdisplaygroupiddisplayassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: displayId
        description: The Display Ids to assign
      - in: formData
        name: unassignDisplayId
        description: An optional array of Display IDs to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Displays
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/display/unassign:
    post:
      summary: Unassigns one or more Displays to a Display Group
      description: Removes the provided Displays from the Display Group
      operationId: displayGroupDisplayUnassign
      x-api-path-slug: displaygroupdisplaygroupiddisplayunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: displayId
        description: The Display Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassigns
      - More
      - Displays
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/displayGroup/assign:
    post:
      summary: Assign one or more DisplayGroups to a Display Group
      description: Adds the provided DisplayGroups to the Display Group
      operationId: displayGroupDisplayGroupAssign
      x-api-path-slug: displaygroupdisplaygroupiddisplaygroupassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: displayGroupId
        description: The displayGroup Ids to assign
      - in: formData
        name: unassignDisplayGroupId
        description: An optional array of displayGroup IDs to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - DisplayGroups
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/displayGroup/unassign:
    post:
      summary: Unassigns one or more DisplayGroups to a Display Group
      description: Removes the provided DisplayGroups from the Display Group
      operationId: displayGroupDisplayGroupUnassign
      x-api-path-slug: displaygroupdisplaygroupiddisplaygroupunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: displayGroupId
        description: The DisplayGroup Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassigns
      - More
      - DisplayGroups
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/media/assign:
    post:
      summary: Assign one or more Media items to a Display Group
      description: Adds the provided Media to the Display Group
      operationId: displayGroupMediaAssign
      x-api-path-slug: displaygroupdisplaygroupidmediaassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: mediaId
        description: The Media Ids to assign
      - in: formData
        name: unassignMediaId
        description: Optional array of Media Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Media
      - Items
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/media/unassign:
    post:
      summary: Unassign one or more Media items from a Display Group
      description: Removes the provided from the Display Group
      operationId: displayGroupMediaUnassign
      x-api-path-slug: displaygroupdisplaygroupidmediaunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: mediaId
        description: The Media Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassign
      - More
      - Media
      - Items
      - From
      - Display
      - Group
  /displaygroup/{displayGroupId}/layout/assign:
    post:
      summary: Assign one or more Layouts items to a Display Group
      description: Adds the provided Layouts to the Display Group
      operationId: displayGroupLayoutsAssign
      x-api-path-slug: displaygroupdisplaygroupidlayoutassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: layoutId
        description: The Layouts Ids to assign
      - in: formData
        name: unassignLayoutId
        description: Optional array of Layouts Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Layouts
      - Items
      - To
      - Display
      - Group
  /displaygroup/{displayGroupId}/layout/unassign:
    post:
      summary: Unassign one or more Layout items from a Display Group
      description: Removes the provided from the Display Group
      operationId: displayGroupLayoutUnassign
      x-api-path-slug: displaygroupdisplaygroupidlayoutunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: layoutId
        description: The Layout Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassign
      - More
      - Layout
      - Items
      - From
      - Display
      - Group
  /displaygroup/{displayGroupId}/version:
    post:
      summary: Set the Version for this Display
      description: Sets the version instructions on all Displays in the Group
      operationId: displayGroupDisplayVersion
      x-api-path-slug: displaygroupdisplaygroupidversion-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group ID
      - in: formData
        name: mediaId
        description: The Media Id of the Installer File
      responses:
        200:
          description: OK
      tags:
      - Set
      - Versionthis
      - Display
  /displayprofile:
    get:
      summary: Display Profile Search
      description: Search this users Display Profiles
      operationId: displayProfileSearch
      x-api-path-slug: displayprofile-get
      parameters:
      - in: formData
        name: displayProfile
        description: Filter by DisplayProfile Name
      - in: formData
        name: displayProfileId
        description: Filter by DisplayProfile Id
      - in: formData
        name: type
        description: Filter by DisplayProfile Type (windows|android)
      responses:
        200:
          description: OK
      tags:
      - Display
      - Profile
      - Search
    post:
      summary: Add Display Profile
      description: Add a Display Profile
      operationId: displayProfileAdd
      x-api-path-slug: displayprofile-post
      parameters:
      - in: formData
        name: isDefault
        description: Flag indicating if this is the default profile for the client
          type
      - in: formData
        name: name
        description: The Name of the Display Profile
      - in: formData
        name: type
        description: The Client Type this Profile will apply to
      responses:
        200:
          description: OK
      tags:
      - Display
      - Profile
  /displayprofile/{displayProfileId}:
    put:
      summary: Edit Display Profile
      description: Edit a Display Profile
      operationId: displayProfileEdit
      x-api-path-slug: displayprofiledisplayprofileid-put
      parameters:
      - in: path
        name: displayProfileId
        description: The Display Profile ID
      - in: formData
        name: isDefault
        description: Flag indicating if this is the default profile for the client
          type
      - in: formData
        name: name
        description: The Name of the Display Profile
      - in: formData
        name: type
        description: The Client Type this Profile will apply to
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Display
      - Profile
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