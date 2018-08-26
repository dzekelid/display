---
swagger: "2.0"
x-collection-name: AWS Redshift
x-complete: 1
info:
  title: AWS Redshift API
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
      description: |-
        Displays a list of event categories for all event source types, or for a specified
                    source type.
      operationId: describeEventCategories
      x-api-path-slug: actiondescribeeventcategories-get
      parameters:
      - in: query
        name: SourceType
        description: The source type, such as cluster or parameter group, to which
          the described event            categories apply
        type: string
      responses:
        200:
          description: OK
      tags:
      - Event Categories
---