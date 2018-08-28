swagger: "2.0"
x-collection-name: AWS AppStream
x-complete: 1
info:
  title: AWS AppStream 2.0 API
  description: amazon-appstream-2-0-is-a-fully-managed-secure-application-streaming-service-that-allows-you-to-stream-desktop-applications-from-aws-to-any-device-running-a-web-browser-without-rewriting-them--amazon-appstream-2-0-provides-users-instanton-access-to-the-applications-they-need-and-a-responsive-fluid-user-experience-on-the-device-of-their-choice-
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