swagger: "2.0"
x-collection-name: Google Cloud Spanner
x-complete: 1
info:
  title: Cloud Spanner
  description: cloud-spanner-is-a-managed-missioncritical-globally-consistent-and-scalable-relational-database-service-
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