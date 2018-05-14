---
swagger: "2.0"
info:
  title: AWS CloudFront API Create Streaming Distribution
  version: 1.0.0
  description: Creates a new RMTP distribution.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateStreamingDistribution:
    get:
      summary: ' Create Streaming Distribution '
      description: Creates a new RMTP distribution
      operationId: createStreamingDistribution
      parameters:
      - in: query
        name: CreateStreamingDistributionRequest
        description: Root level tag for the CreateStreamingDistributionRequest parameters
        type: string
      - in: query
        name: StreamingDistributionConfig
        description: The streaming distribution's configuration information
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - streaming
      - distribution
definitions: []
x-collection-name: AWS CloudFront
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