---
swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 1
info:
  title: AWS RDS API
  version: 1.0.0
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
---