---
swagger: "2.0"
x-collection-name: AWS Direct Connect
x-complete: 1
info:
  title: AWS Direct Connect API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeConnections:
    get:
      summary: Describe Connections
      description: Displays all connections in this region.
      operationId: describeConnections
      x-api-path-slug: actiondescribeconnections-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=DescribeVirtualInterfaces:
    get:
      summary: Describe Virtual Interfaces
      description: Displays all virtual interfaces for an AWS account.
      operationId: describeVirtualInterfaces
      x-api-path-slug: actiondescribevirtualinterfaces-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
---