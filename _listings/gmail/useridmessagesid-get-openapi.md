---
swagger: "2.0"
x-collection-name: Gmail
x-complete: 0
info:
  title: Gmail Get Message
  description: Gets the specified message.
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
    post:
      summary: Create Message
      description: Directly inserts a message into only this user's mailbox similar
        to IMAP APPEND, bypassing most scanning and classification. Does not send
        a message.
      operationId: gmail.users.messages.insert
      x-api-path-slug: useridmessages-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: deleted
        description: Mark the email as permanently deleted (not TRASH) and only visible
          in Google Vault to a Vault administrator
      - in: query
        name: internalDateSource
        description: Source for Gmails internal date of the message
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/messages/batchDelete:
    post:
      summary: Delete Messages
      description: Deletes many messages by message ID. Provides no guarantees that
        messages were not already deleted or even existed at all.
      operationId: gmail.users.messages.batchDelete
      x-api-path-slug: useridmessagesbatchdelete-post
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
  /{userId}/messages/batchModify:
    post:
      summary: Update Label
      description: Modifies the labels on the specified messages.
      operationId: gmail.users.messages.batchModify
      x-api-path-slug: useridmessagesbatchmodify-post
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
  /{userId}/messages/import:
    post:
      summary: Import Message
      description: Imports a message into only this user's mailbox, with standard
        email delivery scanning and classification similar to receiving via SMTP.
        Does not send a message.
      operationId: gmail.users.messages.import
      x-api-path-slug: useridmessagesimport-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: deleted
        description: Mark the email as permanently deleted (not TRASH) and only visible
          in Google Vault to a Vault administrator
      - in: query
        name: internalDateSource
        description: Source for Gmails internal date of the message
      - in: query
        name: neverMarkSpam
        description: Ignore the Gmail spam classifier decision and never mark this
          email as SPAM in the mailbox
      - in: query
        name: processForCalendar
        description: Process calendar invites in the email and add any extracted meetings
          to the Google Calendar for this user
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/messages/send:
    post:
      summary: Send Message
      description: Sends the specified message to the recipients in the To, Cc, and
        Bcc headers.
      operationId: gmail.users.messages.send
      x-api-path-slug: useridmessagessend-post
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
  /{userId}/messages/{id}:
    delete:
      summary: Delete Message
      description: Immediately and permanently deletes the specified message. This
        operation cannot be undone. Prefer messages.trash instead.
      operationId: gmail.users.messages.delete
      x-api-path-slug: useridmessagesid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the message to delete
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
    get:
      summary: Get Message
      description: Gets the specified message.
      operationId: gmail.users.messages.get
      x-api-path-slug: useridmessagesid-get
      parameters:
      - in: query
        name: format
        description: The format to return the message in
      - in: path
        name: id
        description: The ID of the message to retrieve
      - in: query
        name: metadataHeaders
        description: When given and format is METADATA, only include headers specified
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