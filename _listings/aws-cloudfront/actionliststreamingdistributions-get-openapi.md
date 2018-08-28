---
swagger: "2.0"
x-collection-name: AWS CloudFront
x-complete: 0
info:
  title: AWS CloudFront API List Streaming Distributions
  version: 1.0.0
  description: List streaming distributions.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateStreamingDistribution:
    get:
      summary: Create Streaming Distribution
      description: Creates a new RMTP distribution.
      operationId: createStreamingDistribution
      x-api-path-slug: actioncreatestreamingdistribution-get
      parameters:
      - in: query
        name: CreateStreamingDistributionRequest
        description: Root level tag for the CreateStreamingDistributionRequest parameters
        type: string
      - in: query
        name: StreamingDistributionConfig
        description: The streaming distributions configuration information
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - Streaming
      - Distribution
  /?Action=CreateStreamingDistributionWithTags:
    get:
      summary: Create Streaming Distribution With Tags
      description: Create a new streaming distribution with tags.
      operationId: createStreamingDistributionWithTags
      x-api-path-slug: actioncreatestreamingdistributionwithtags-get
      parameters:
      - in: query
        name: CreateStreamingDistributionWithTagsRequest
        description: Root level tag for the CreateStreamingDistributionWithTagsRequest
          parameters
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: StreamingDistributionConfigWithTags
        description: The streaming distributions configuration information
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC
        type: string
      responses:
        200:
          description: OK
      tags:
      - Streaming
      - Distribution
      - Tags
  /?Action=DeleteStreamingDistribution:
    get:
      summary: Delete Streaming Distribution
      description: Delete a streaming distribution.
      operationId: deleteStreamingDistribution
      x-api-path-slug: actiondeletestreamingdistribution-get
      parameters:
      - in: query
        name: CustomerGatewayId
        description: The ID of the customer gateway
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,             and provides an error response
        type: string
      - in: query
        name: Id
        description: The distribution ID
        type: string
      - in: query
        name: If-Match
        description: The value of the ETag header that you received when you disabled
          the      streaming distribution
        type: string
      responses:
        200:
          description: OK
      tags:
      - Streaming
      - Distribution
  /?Action=GetStreamingDistribution:
    get:
      summary: Get Streaming Distribution
      description: |-
        Gets information about a specified RTMP distribution, including the distribution
              configuration.
      operationId: getStreamingDistribution
      x-api-path-slug: actiongetstreamingdistribution-get
      parameters:
      - in: query
        name: HostIdSet.N
        description: The ID/s of the Dedicated Host/s that the reservation will be
          associated            with
        type: string
      - in: query
        name: Id
        description: The streaming distributions ID
        type: string
      - in: query
        name: OfferingId
        description: The offering ID of the reservation
        type: string
      responses:
        200:
          description: OK
      tags:
      - Streaming
      - Distribution
  /?Action=GetStreamingDistributionConfig:
    get:
      summary: Get Streaming Distribution Config
      description: Get the configuration information about a streaming distribution.
      operationId: getStreamingDistributionConfig
      x-api-path-slug: actiongetstreamingdistributionconfig-get
      parameters:
      - in: query
        name: AutoPlacement
        description: Specify whether to enable or disable auto-placement
        type: string
      - in: query
        name: HostId.N
        description: The host IDs of the Dedicated Hosts you want to modify
        type: string
      - in: query
        name: Id
        description: The streaming distributions ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Streaming
      - Distribution
      - Config
  /?Action=ListStreamingDistributions:
    get:
      summary: List Streaming Distributions
      description: List streaming distributions.
      operationId: listStreamingDistributions
      x-api-path-slug: actionliststreamingdistributions-get
      parameters:
      - in: query
        name: DhcpConfiguration.N
        description: A DHCP configuration option
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Marker
        description: The value that you provided for the Marker request parameter
        type: string
      - in: query
        name: MaxItems
        description: The value that you provided for the MaxItems request parameter
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Streaming
      - Distributions
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