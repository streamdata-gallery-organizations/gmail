---
swagger: "2.0"
x-collection-name: Gmail
x-complete: 0
info:
  title: Gmail Get Message
  description: Lists the messages in the user's mailbox.
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
  /{userId}/history:
    get:
      summary: Get History
      description: Lists the history of all changes to the given mailbox. History
        results are returned in chronological order (increasing historyId).
      operationId: gmail.users.history.list
      x-api-path-slug: useridhistory-get
      parameters:
      - in: query
        name: historyTypes
        description: History types to be returned by the function
      - in: query
        name: labelId
        description: Only return messages with a label matching the ID
      - in: query
        name: maxResults
        description: The maximum number of history records to return
      - in: query
        name: pageToken
        description: Page token to retrieve a specific page of results in the list
      - in: query
        name: startHistoryId
        description: Required
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - History
  /{userId}/labels:
    get:
      summary: Get Labels
      description: Lists all labels in the user's mailbox.
      operationId: gmail.users.labels.list
      x-api-path-slug: useridlabels-get
      parameters:
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Label
    post:
      summary: Create Label
      description: Creates a new label.
      operationId: gmail.users.labels.create
      x-api-path-slug: useridlabels-post
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
      - Label
  /{userId}/labels/{id}:
    delete:
      summary: Delete Lbel
      description: Immediately and permanently deletes the specified label and removes
        it from any messages and threads that it is applied to.
      operationId: gmail.users.labels.delete
      x-api-path-slug: useridlabelsid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the label to delete
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Label
    get:
      summary: Get Label
      description: Gets the specified label.
      operationId: gmail.users.labels.get
      x-api-path-slug: useridlabelsid-get
      parameters:
      - in: path
        name: id
        description: The ID of the label to retrieve
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Label
    patch:
      summary: Update Label
      description: Updates the specified label. This method supports patch semantics.
      operationId: gmail.users.labels.patch
      x-api-path-slug: useridlabelsid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The ID of the label to update
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Label
    put:
      summary: Update Label
      description: Updates the specified label.
      operationId: gmail.users.labels.update
      x-api-path-slug: useridlabelsid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The ID of the label to update
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Label
  /{userId}/messages:
    get:
      summary: Get Message
      description: Lists the messages in the user's mailbox.
      operationId: gmail.users.messages.list
      x-api-path-slug: useridmessages-get
      parameters:
      - in: query
        name: includeSpamTrash
        description: Include messages from SPAM and TRASH in the results
      - in: query
        name: labelIds
        description: Only return messages with labels that match all of the specified
          label IDs
      - in: query
        name: maxResults
        description: Maximum number of messages to return
      - in: query
        name: pageToken
        description: Page token to retrieve a specific page of results in the list
      - in: query
        name: q
        description: Only return messages matching the specified query
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
x-streamrank:
  polling_total_time_average: "0.07"
  polling_size_download_average: "288.24"
  streaming_total_time_average: "0.04"
  streaming_size_download_average: "145.68"
  change_yes: "2"
  change_no: "2331"
  time_percentage: "43"
  size_percentage: "49"
  change_percentage: "0"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---