---
swagger: "2.0"
x-collection-name: Reverb
x-complete: 0
info:
  title: Reverb Get Articles Slug
  description: Display a single article
  termsOfService: https://reverb.com/page/terms
  contact:
    name: Reverb API
    url: https://dev.reverb.com
    email: integrations@reverb.com
  version: "3.0"
host: api.reverb.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /currencies/display:
    get:
      summary: Get Currencies Display
      description: List of supported display currencies for browsing listings
      operationId: getCurrenciesDisplay
      x-api-path-slug: currenciesdisplay-get
      responses:
        200:
          description: OK
      tags:
      - Currencies
      - Display
  /articles/{slug}:
    get:
      summary: Get Articles Slug
      description: Display a single article
      operationId: getArticlesSlug
      x-api-path-slug: articlesslug-get
      parameters:
      - in: path
        name: slug
      responses:
        200:
          description: OK
      tags:
      - Articles
      - Slug
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