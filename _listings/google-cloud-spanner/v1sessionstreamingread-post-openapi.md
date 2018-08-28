---
swagger: "2.0"
x-collection-name: Google Cloud Spanner
x-complete: 0
info:
  title: Google Cloud Spanner API Streaming Read
  description: |-
    Like Read, except returns the result set as a
    stream. Unlike Read, there is no limit on the
    size of the returned result set. However, no individual row in
    the result set can exceed 100 MiB, and no column value can exceed
    10 MiB.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: spanner.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{session}:streamingRead:
    post:
      summary: Streaming Read
      description: |-
        Like Read, except returns the result set as a
        stream. Unlike Read, there is no limit on the
        size of the returned result set. However, no individual row in
        the result set can exceed 100 MiB, and no column value can exceed
        10 MiB.
      operationId: spanner.projects.instances.databases.sessions.streamingRead
      x-api-path-slug: v1sessionstreamingread-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: session
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Streaming
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