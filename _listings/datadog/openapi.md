swagger: "2.0"
x-collection-name: Datadog
x-complete: 1
info:
  title: DataDog Merged API
  version: 1.0.0
basePath: api/v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /downtime:
    post:
      summary: Add Downtime
      description: Schedule monitor downtime
      operationId: postDowntime
      x-api-path-slug: downtime-post
      parameters:
      - in: query
        name: period
        description: how often to repeat as an integer
        type: string
      - in: query
        name: type
        description: the type of recurrence
        type: string
      - in: query
        name: until_date
        description: (optional) the date at which the recurrence should end as a POSIX
          timestmap
        type: string
      - in: query
        name: until_occurrences
        description: (optional) how many times the downtime will be rescheduled
        type: string
      - in: query
        name: week_days
        description: (optional) a list of week days to repeat on
        type: string
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Downtime
    get:
      summary: Get Downtime
      description: Get all monitor downtimes
      operationId: getDowntime
      x-api-path-slug: downtime-get
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Downtime
  /downtime/:downtime_id:
    put:
      summary: Put Downtime Downtime
      description: Update monitor downtime
      operationId: putDowntimeDowntime
      x-api-path-slug: downtimedowntime-id-put
      parameters:
      - in: query
        name: period
        description: how often to repeat as an integer
        type: string
      - in: query
        name: type
        description: the type of recurrence
        type: string
      - in: query
        name: until_date
        description: (optional) the date at which the recurrence should end as a POSIX
          timestmap
        type: string
      - in: query
        name: until_occurrences
        description: (optional) how many times the downtime will be rescheduled
        type: string
      - in: query
        name: week_days
        description: (optional) a list of week days to repeat on
        type: string
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Downtime
      - Downtime
    delete:
      summary: Delete Downtime Downtime
      description: DELETE downtime downtime
      operationId: deleteDowntimeDowntime
      x-api-path-slug: downtimedowntime-id-delete
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Downtime
      - Downtime
    get:
      summary: Get Downtime Downtime
      description: Get a monitor downtime
      operationId: getDowntimeDowntime
      x-api-path-slug: downtimedowntime-id-get
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Downtime
      - Downtime