---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Import Image
  version: 1.0.0
  description: Displays details about an import virtual machine or import snapshot
    tasks that are already created.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeImportImageTasks:
    get:
      summary: Describe Import Image Tasks
      description: Displays details about an import virtual machine or import snapshot
        tasks that are already created.
      operationId: describeimportimagetasks
      x-api-path-slug: actiondescribeimportimagetasks-get
      responses:
        200:
          description: OK
      tags:
      - Import Image Tasks
  /?Action=ImportImage:
    get:
      summary: Import Image
      description: Displays details about an import virtual machine or import snapshot
        tasks that are already created.
      operationId: importimage
      x-api-path-slug: actionimportimage-get
      responses:
        200:
          description: OK
      tags:
      - Import Image
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