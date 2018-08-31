---
swagger: "2.0"
x-collection-name: Gmail
x-complete: 0
info:
  title: Gmail Update Draft
  description: Replaces a draft's content.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /gmail/v1/users
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{userId}/drafts:
    get:
      summary: Get Drafts
      description: Lists the drafts in the user's mailbox.
      operationId: gmail.users.drafts.list
      x-api-path-slug: useriddrafts-get
      parameters:
      - in: query
        name: includeSpamTrash
        description: Include drafts from SPAM and TRASH in the results
      - in: query
        name: maxResults
        description: Maximum number of drafts to return
      - in: query
        name: pageToken
        description: Page token to retrieve a specific page of results in the list
      - in: query
        name: q
        description: Only return draft messages matching the specified query
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
    post:
      summary: Update Draft
      description: Creates a new draft with the DRAFT label.
      operationId: gmail.users.drafts.create
      x-api-path-slug: useriddrafts-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/drafts/send:
    post:
      summary: Send Draft
      description: Sends the specified, existing draft to the recipients in the To,
        Cc, and Bcc headers.
      operationId: gmail.users.drafts.send
      x-api-path-slug: useriddraftssend-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/drafts/{id}:
    delete:
      summary: Delete Draft
      description: Immediately and permanently deletes the specified draft. Does not
        simply trash it.
      operationId: gmail.users.drafts.delete
      x-api-path-slug: useriddraftsid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the draft to delete
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
    get:
      summary: Get Draft
      description: Gets the specified draft.
      operationId: gmail.users.drafts.get
      x-api-path-slug: useriddraftsid-get
      parameters:
      - in: query
        name: format
        description: The format to return the draft in
      - in: path
        name: id
        description: The ID of the draft to retrieve
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
    put:
      summary: Update Draft
      description: Replaces a draft's content.
      operationId: gmail.users.drafts.update
      x-api-path-slug: useriddraftsid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The ID of the draft to update
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
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