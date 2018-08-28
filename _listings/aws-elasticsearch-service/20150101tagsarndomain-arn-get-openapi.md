---
swagger: "2.0"
x-collection-name: AWS Elasticsearch Service
x-complete: 0
info:
  title: Amazon Elasticsearch Service API List Tags
  version: 1.0.0
  description: |-
    Displays all of the tags for an Amazon ES domain. Use the GET HTTP method
                    with this operation.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2015-01-01/domain:
    get:
      summary: List Domain Names
      description: Displays the names of all Amazon ES domains owned by the current
        user.
      operationId: listDomainNames
      x-api-path-slug: 20150101domain-get
      responses:
        200:
          description: OK
      tags:
      - Domains
  /2015-01-01/es/domain/{domain_name}/config:
    get:
      summary: Describe Elasticsearch Domain Config
      description: |-
        Displays the configuration of an Amazon ES domain. Use the HTTP GET method
                        with this operation.
      operationId: describeElasticsearchDomainConfig
      x-api-path-slug: 20150101esdomaindomain-nameconfig-get
      parameters:
      - in: query
        name: DomainName
        description: Name of the Amazon ES domain
        type: string
      responses:
        200:
          description: OK
      tags:
      - Domains
  /2015-01-01/tags?arn={domain_arn}:
    get:
      summary: List Tags
      description: |-
        Displays all of the tags for an Amazon ES domain. Use the GET HTTP method
                        with this operation.
      operationId: listTags
      x-api-path-slug: 20150101tagsarndomain-arn-get
      responses:
        200:
          description: OK
      tags:
      - Tags
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