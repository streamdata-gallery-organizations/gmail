---
swagger: "2.0"
x-collection-name: Gmail
x-complete: 0
info:
  title: Gmail Get Alias
  description: Gets the specified send-as alias. Fails with an HTTP 404 error if the
    specified address is not a member of the collection.
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
  /{userId}/messages/{id}/modify:
    post:
      summary: Modify message
      description: Modifies the labels on the specified message.
      operationId: gmail.users.messages.modify
      x-api-path-slug: useridmessagesidmodify-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The ID of the message to modify
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/messages/{id}/trash:
    post:
      summary: Trash Message
      description: Moves the specified message to the trash.
      operationId: gmail.users.messages.trash
      x-api-path-slug: useridmessagesidtrash-post
      parameters:
      - in: path
        name: id
        description: The ID of the message to Trash
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/messages/{id}/untrash:
    post:
      summary: UnTrash Message
      description: Removes the specified message from the trash.
      operationId: gmail.users.messages.untrash
      x-api-path-slug: useridmessagesiduntrash-post
      parameters:
      - in: path
        name: id
        description: The ID of the message to remove from Trash
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/messages/{messageId}/attachments/{id}:
    get:
      summary: Get Attachments
      description: Gets the specified message attachment.
      operationId: gmail.users.messages.attachments.get
      x-api-path-slug: useridmessagesmessageidattachmentsid-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      - in: path
        name: messageId
        description: The ID of the message containing the attachment
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - Email
  /{userId}/profile:
    get:
      summary: Get Profile
      description: Gets the current user's Gmail profile.
      operationId: gmail.users.getProfile
      x-api-path-slug: useridprofile-get
      parameters:
      - in: path
        name: userId
        description: The users email address
      responses:
        200:
          description: OK
      tags:
      - User
  /{userId}/settings/autoForwarding:
    get:
      summary: Get Auto-Forwarding Settings
      description: Gets the auto-forwarding setting for the specified account.
      operationId: gmail.users.settings.getAutoForwarding
      x-api-path-slug: useridsettingsautoforwarding-get
      parameters:
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Settings
    put:
      summary: Update Auto-Forwarding Settings
      description: |-
        Updates the auto-forwarding setting for the specified account. A verified forwarding address must be specified when auto-forwarding is enabled.

        This method is only available to service account clients that have been delegated domain-wide authority.
      operationId: gmail.users.settings.updateAutoForwarding
      x-api-path-slug: useridsettingsautoforwarding-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Settings
  /{userId}/settings/filters:
    get:
      summary: Get Message Filters
      description: Lists the message filters of a Gmail user.
      operationId: gmail.users.settings.filters.list
      x-api-path-slug: useridsettingsfilters-get
      parameters:
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Filters
    post:
      summary: Create Message Filters
      description: Creates a filter.
      operationId: gmail.users.settings.filters.create
      x-api-path-slug: useridsettingsfilters-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Filters
  /{userId}/settings/filters/{id}:
    delete:
      summary: Delete Message Filter
      description: Deletes a filter.
      operationId: gmail.users.settings.filters.delete
      x-api-path-slug: useridsettingsfiltersid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter to be deleted
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Filters
    get:
      summary: Get Message Filter
      description: Gets a filter.
      operationId: gmail.users.settings.filters.get
      x-api-path-slug: useridsettingsfiltersid-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter to be fetched
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Filters
  /{userId}/settings/forwardingAddresses:
    get:
      summary: Get Forward Addresses
      description: Lists the forwarding addresses for the specified account.
      operationId: gmail.users.settings.forwardingAddresses.list
      x-api-path-slug: useridsettingsforwardingaddresses-get
      parameters:
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Forwarding Address
    post:
      summary: Create Forward Addresse
      description: |-
        Creates a forwarding address. If ownership verification is required, a message will be sent to the recipient and the resource's verification status will be set to pending; otherwise, the resource will be created with verification status set to accepted.

        This method is only available to service account clients that have been delegated domain-wide authority.
      operationId: gmail.users.settings.forwardingAddresses.create
      x-api-path-slug: useridsettingsforwardingaddresses-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Forwarding Address
  /{userId}/settings/forwardingAddresses/{forwardingEmail}:
    delete:
      summary: Delete Forward Address
      description: |-
        Deletes the specified forwarding address and revokes any verification that may have been required.

        This method is only available to service account clients that have been delegated domain-wide authority.
      operationId: gmail.users.settings.forwardingAddresses.delete
      x-api-path-slug: useridsettingsforwardingaddressesforwardingemail-delete
      parameters:
      - in: path
        name: forwardingEmail
        description: The forwarding address to be deleted
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Forwarding Address
    get:
      summary: GGetet Forward Address
      description: Gets the specified forwarding address.
      operationId: gmail.users.settings.forwardingAddresses.get
      x-api-path-slug: useridsettingsforwardingaddressesforwardingemail-get
      parameters:
      - in: path
        name: forwardingEmail
        description: The forwarding address to be retrieved
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Forwarding Address
  /{userId}/settings/imap:
    get:
      summary: Gets IMAP Settings
      description: Gets IMAP settings.
      operationId: gmail.users.settings.getImap
      x-api-path-slug: useridsettingsimap-get
      parameters:
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - IMAP Settings
    put:
      summary: Update IMAP Setting
      description: Updates IMAP settings.
      operationId: gmail.users.settings.updateImap
      x-api-path-slug: useridsettingsimap-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - IMAP Settings
  /{userId}/settings/pop:
    get:
      summary: Gets POP Settings
      description: Gets POP settings.
      operationId: gmail.users.settings.getPop
      x-api-path-slug: useridsettingspop-get
      parameters:
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - ""
    put:
      summary: Update IMAP Setting
      description: Updates POP settings.
      operationId: gmail.users.settings.updatePop
      x-api-path-slug: useridsettingspop-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - POP Settings
  /{userId}/settings/sendAs:
    get:
      summary: Send As Alias
      description: Lists the send-as aliases for the specified account. The result
        includes the primary send-as address associated with the account as well as
        any custom "from" aliases.
      operationId: gmail.users.settings.sendAs.list
      x-api-path-slug: useridsettingssendas-get
      parameters:
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Alias
    post:
      summary: Create Alias
      description: |-
        Creates a custom "from" send-as alias. If an SMTP MSA is specified, Gmail will attempt to connect to the SMTP service to validate the configuration before creating the alias. If ownership verification is required for the alias, a message will be sent to the email address and the resource's verification status will be set to pending; otherwise, the resource will be created with verification status set to accepted. If a signature is provided, Gmail will sanitize the HTML before saving it with the alias.

        This method is only available to service account clients that have been delegated domain-wide authority.
      operationId: gmail.users.settings.sendAs.create
      x-api-path-slug: useridsettingssendas-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Alias
  /{userId}/settings/sendAs/{sendAsEmail}:
    delete:
      summary: Delete Alias
      description: |-
        Deletes the specified send-as alias. Revokes any verification that may have been required for using it.

        This method is only available to service account clients that have been delegated domain-wide authority.
      operationId: gmail.users.settings.sendAs.delete
      x-api-path-slug: useridsettingssendassendasemail-delete
      parameters:
      - in: path
        name: sendAsEmail
        description: The send-as alias to be deleted
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Alias
    get:
      summary: Get Alias
      description: Gets the specified send-as alias. Fails with an HTTP 404 error
        if the specified address is not a member of the collection.
      operationId: gmail.users.settings.sendAs.get
      x-api-path-slug: useridsettingssendassendasemail-get
      parameters:
      - in: path
        name: sendAsEmail
        description: The send-as alias to be retrieved
      - in: path
        name: userId
        description: Users email address
      responses:
        200:
          description: OK
      tags:
      - Alias
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