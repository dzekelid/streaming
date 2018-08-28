swagger: "2.0"
x-collection-name: Meetup
x-complete: 1
info:
  title: Meetup
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2/rsvps:
    ws:
      summary: WebSockets RSVP Stream
      description: |-
        For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
        efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
        any messages received from the client after the socket is open.

        Because browser support for WebSockets is limited, we recommend that you consume this stream
        through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
      operationId: streams
      x-api-path-slug: 2rsvps-ws
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Return recent RSVPs with an mtime greater than the supplied time,
          in milliseconds since the epoch
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Streaming
      - Websockets