---
swagger: "2.0"
x-collection-name: AWS AppStream
x-complete: 0
info:
  title: AWS AppStream 2.0 API Create Streaming URL
  description: Creates a URL to start an AppStream 2.
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateStreamingURL:
    get:
      summary: Create Streaming URL
      description: Creates a URL to start an AppStream 2.
      operationId: CreateStreamingURL
      x-api-path-slug: actioncreatestreamingurl-get
      parameters:
      - in: query
        name: ApplicationId
        description: The ID of the application that must be launched after the session
          starts
        type: string
      - in: query
        name: FleetName
        description: The fleet for which the URL is generated
        type: string
      - in: query
        name: SessionContext
        description: The sessionContext of the streaming URL
        type: string
      - in: query
        name: StackName
        description: The stack for which the URL is generated
        type: string
      - in: query
        name: UserId
        description: A unique user ID for whom the URL is generated
        type: string
      - in: query
        name: Validity
        description: The validity duration of the URL in seconds
        type: string
      responses:
        200:
          description: OK
      tags:
      - URL
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