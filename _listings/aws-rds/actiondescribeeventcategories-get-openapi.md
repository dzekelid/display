---
swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 0
info:
  title: Amazon RDS API Describe Event Categories
  version: 1.0.0
  description: Displays a list of categories for all event source types, or, if specified,
    for a specified source type.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeEventCategories:
    get:
      summary: Describe Event Categories
      description: Displays a list of categories for all event source types, or, if
        specified, for a specified source type.
      operationId: describeeventcategories
      x-api-path-slug: actiondescribeeventcategories-get
      parameters:
      - in: query
        name: Filters.Filter.N
        description: This parameter is not currently supported
        type: string
      - in: query
        name: SourceType
        description: The type of source that will be generating the events
        type: string
      responses:
        200:
          description: OK
      tags:
      - Event Categories
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