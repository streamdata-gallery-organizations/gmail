---
name: Gmail
x-slug: gmail
description: The Gmail API is a RESTful API that can be used to access Gmail mailboxes
  and send mail. For most web applications (including mobile apps), the Gmail API
  is the best choice for authorized access to a users Gmail data.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Gmail
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/apis.md
specificationVersion: "0.14"
apis:
- name: Gmail Get Drafts
  x-api-slug: gmail
  description: Lists the drafts in the user's mailbox.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/drafts
  tags: Email
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddrafts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddrafts-get-openapi.md
- name: Gmail Update Draft
  x-api-slug: gmail
  description: Creates a new draft with the DRAFT label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/drafts
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddrafts-post-openapi.md
- name: Gmail Send Draft
  x-api-slug: gmail
  description: Sends the specified, existing draft to the recipients in the To, Cc,
    and Bcc headers.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/drafts/send
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddraftssend-post-openapi.md
- name: Gmail Delete Draft
  x-api-slug: gmail
  description: Immediately and permanently deletes the specified draft. Does not simply
    trash it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/drafts/{id}
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddraftsid-delete-openapi.md
- name: Gmail Get Draft
  x-api-slug: gmail
  description: Gets the specified draft.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/drafts/{id}
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddraftsid-get-openapi.md
- name: Gmail Update Draft
  x-api-slug: gmail
  description: Replaces a draft's content.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/drafts/{id}
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useriddraftsid-put-openapi.md
- name: Gmail Get History
  x-api-slug: gmail
  description: Lists the history of all changes to the given mailbox. History results
    are returned in chronological order (increasing historyId).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/history
  tags: History
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridhistory-get-openapi.md
- name: Gmail Get Labels
  x-api-slug: gmail
  description: Lists all labels in the user's mailbox.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/labels
  tags: Label
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridlabels-get-openapi.md
- name: Gmail Create Label
  x-api-slug: gmail
  description: Creates a new label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/labels
  tags: Label
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridlabels-post-openapi.md
- name: Gmail Delete Lbel
  x-api-slug: gmail
  description: Immediately and permanently deletes the specified label and removes
    it from any messages and threads that it is applied to.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/labels/{id}
  tags: Label
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridlabelsid-delete-openapi.md
- name: Gmail Get Label
  x-api-slug: gmail
  description: Gets the specified label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/labels/{id}
  tags: Label
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridlabelsid-get-openapi.md
- name: Gmail Update Label
  x-api-slug: gmail
  description: Updates the specified label. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/labels/{id}
  tags: Label
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridlabelsid-patch-openapi.md
- name: Gmail Update Label
  x-api-slug: gmail
  description: Updates the specified label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/labels/{id}
  tags: Label
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridlabelsid-put-openapi.md
- name: Gmail Get Message
  x-api-slug: gmail
  description: Lists the messages in the user's mailbox.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessages-get-openapi.md
- name: Gmail Create Message
  x-api-slug: gmail
  description: Directly inserts a message into only this user's mailbox similar to
    IMAP APPEND, bypassing most scanning and classification. Does not send a message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessages-post-openapi.md
- name: Gmail Delete Messages
  x-api-slug: gmail
  description: Deletes many messages by message ID. Provides no guarantees that messages
    were not already deleted or even existed at all.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/batchDelete
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesbatchdelete-post-openapi.md
- name: Gmail Update Label
  x-api-slug: gmail
  description: Modifies the labels on the specified messages.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/batchModify
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesbatchmodify-post-openapi.md
- name: Gmail Import Message
  x-api-slug: gmail
  description: Imports a message into only this user's mailbox, with standard email
    delivery scanning and classification similar to receiving via SMTP. Does not send
    a message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/import
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesimport-post-openapi.md
- name: Gmail Send Message
  x-api-slug: gmail
  description: Sends the specified message to the recipients in the To, Cc, and Bcc
    headers.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/send
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagessend-post-openapi.md
- name: Gmail Delete Message
  x-api-slug: gmail
  description: Immediately and permanently deletes the specified message. This operation
    cannot be undone. Prefer messages.trash instead.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/{id}
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesid-delete-openapi.md
- name: Gmail Get Message
  x-api-slug: gmail
  description: Gets the specified message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/{id}
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesid-get-openapi.md
- name: Gmail Modify message
  x-api-slug: gmail
  description: Modifies the labels on the specified message.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/{id}/modify
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesidmodify-post-openapi.md
- name: Gmail Trash Message
  x-api-slug: gmail
  description: Moves the specified message to the trash.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/{id}/trash
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesidtrash-post-openapi.md
- name: Gmail UnTrash Message
  x-api-slug: gmail
  description: Removes the specified message from the trash.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/{id}/untrash
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesiduntrash-post-openapi.md
- name: Gmail Get Attachments
  x-api-slug: gmail
  description: Gets the specified message attachment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/messages/{messageId}/attachments/{id}
  tags: Email
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridmessagesmessageidattachmentsid-get-openapi.md
- name: Gmail Get Profile
  x-api-slug: gmail
  description: Gets the current user's Gmail profile.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/profile
  tags: User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridprofile-get-openapi.md
- name: Gmail Get Auto-Forwarding Settings
  x-api-slug: gmail
  description: Gets the auto-forwarding setting for the specified account.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/autoForwarding
  tags: Settings
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsautoforwarding-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsautoforwarding-get-openapi.md
- name: Gmail Update Auto-Forwarding Settings
  x-api-slug: gmail
  description: |-
    Updates the auto-forwarding setting for the specified account. A verified forwarding address must be specified when auto-forwarding is enabled.

    This method is only available to service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/autoForwarding
  tags: Settings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsautoforwarding-put-openapi.md
- name: Gmail Get Message Filters
  x-api-slug: gmail
  description: Lists the message filters of a Gmail user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/filters
  tags: Filters
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsfilters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsfilters-get-openapi.md
- name: Gmail Create Message Filters
  x-api-slug: gmail
  description: Creates a filter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/filters
  tags: Filters
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsfilters-post-openapi.md
- name: Gmail Delete Message Filter
  x-api-slug: gmail
  description: Deletes a filter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/filters/{id}
  tags: Filters
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsfiltersid-delete-openapi.md
- name: Gmail Get Message Filter
  x-api-slug: gmail
  description: Gets a filter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/filters/{id}
  tags: Filters
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsfiltersid-get-openapi.md
- name: Gmail Get Forward Addresses
  x-api-slug: gmail
  description: Lists the forwarding addresses for the specified account.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/forwardingAddresses
  tags: Forwarding Address
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsforwardingaddresses-get-openapi.md
- name: Gmail Create Forward Addresse
  x-api-slug: gmail
  description: |-
    Creates a forwarding address. If ownership verification is required, a message will be sent to the recipient and the resource's verification status will be set to pending; otherwise, the resource will be created with verification status set to accepted.

    This method is only available to service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/forwardingAddresses
  tags: Forwarding Address
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsforwardingaddresses-post-openapi.md
- name: Gmail Delete Forward Address
  x-api-slug: gmail
  description: |-
    Deletes the specified forwarding address and revokes any verification that may have been required.

    This method is only available to service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/forwardingAddresses/{forwardingEmail}
  tags: Forwarding Address
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsforwardingaddressesforwardingemail-delete-openapi.md
- name: Gmail GGetet Forward Address
  x-api-slug: gmail
  description: Gets the specified forwarding address.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/forwardingAddresses/{forwardingEmail}
  tags: Forwarding Address
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsforwardingaddressesforwardingemail-get-openapi.md
- name: Gmail Gets IMAP Settings
  x-api-slug: gmail
  description: Gets IMAP settings.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/imap
  tags: IMAP Settings
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsimap-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsimap-get-openapi.md
- name: Gmail Update IMAP Setting
  x-api-slug: gmail
  description: Updates IMAP settings.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/imap
  tags: IMAP Settings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsimap-put-openapi.md
- name: Gmail Gets POP Settings
  x-api-slug: gmail
  description: Gets POP settings.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/pop
  tags: ~
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingspop-get-openapi.md
- name: Gmail Update IMAP Setting
  x-api-slug: gmail
  description: Updates POP settings.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/pop
  tags: POP Settings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingspop-put-openapi.md
- name: Gmail Send As Alias
  x-api-slug: gmail
  description: Lists the send-as aliases for the specified account. The result includes
    the primary send-as address associated with the account as well as any custom
    "from" aliases.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs
  tags: Alias
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendas-get-openapi.md
- name: Gmail Create Alias
  x-api-slug: gmail
  description: |-
    Creates a custom "from" send-as alias. If an SMTP MSA is specified, Gmail will attempt to connect to the SMTP service to validate the configuration before creating the alias. If ownership verification is required for the alias, a message will be sent to the email address and the resource's verification status will be set to pending; otherwise, the resource will be created with verification status set to accepted. If a signature is provided, Gmail will sanitize the HTML before saving it with the alias.

    This method is only available to service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs
  tags: Alias
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendas-post-openapi.md
- name: Gmail Delete Alias
  x-api-slug: gmail
  description: |-
    Deletes the specified send-as alias. Revokes any verification that may have been required for using it.

    This method is only available to service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}
  tags: Alias
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemail-delete-openapi.md
- name: Gmail Get Alias
  x-api-slug: gmail
  description: Gets the specified send-as alias. Fails with an HTTP 404 error if the
    specified address is not a member of the collection.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}
  tags: Alias
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemail-get-openapi.md
- name: Gmail Update Alias
  x-api-slug: gmail
  description: |-
    Updates a send-as alias. If a signature is provided, Gmail will sanitize the HTML before saving it with the alias.

    Addresses other than the primary address for the account can only be updated by service account clients that have been delegated domain-wide authority. This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}
  tags: Alias
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemail-patch-openapi.md
- name: Gmail Update Alias
  x-api-slug: gmail
  description: |-
    Updates a send-as alias. If a signature is provided, Gmail will sanitize the HTML before saving it with the alias.

    Addresses other than the primary address for the account can only be updated by service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}
  tags: Alias
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemail-put-openapi.md
- name: Gmail Get S/MIME Configurations
  x-api-slug: gmail
  description: Lists S/MIME configs for the specified send-as alias.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}/smimeInfo
  tags: S/MIME Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailsmimeinfo-get-openapi.md
- name: Gmail Create S/MIME Configurations
  x-api-slug: gmail
  description: Insert (upload) the given S/MIME config for the specified send-as alias.
    Note that pkcs12 format is required for the key.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}/smimeInfo
  tags: S/MIME Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailsmimeinfo-post-openapi.md
- name: Gmail Delete S/MIME Configurations
  x-api-slug: gmail
  description: Deletes the specified S/MIME config for the specified send-as alias.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}/smimeInfo/{id}
  tags: S/MIME Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailsmimeinfoid-delete-openapi.md
- name: Gmail Get S/MIME Configuration
  x-api-slug: gmail
  description: Gets the specified S/MIME config for the specified send-as alias.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}/smimeInfo/{id}
  tags: S/MIME Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailsmimeinfoid-get-openapi.md
- name: Gmail Create Default S/MIME Configurations
  x-api-slug: gmail
  description: Sets the default S/MIME config for the specified send-as alias.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}/smimeInfo/{id}/setDefault
  tags: S/MIME Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailsmimeinfoidsetdefault-post-openapi.md
- name: Gmail Send Verification Email
  x-api-slug: gmail
  description: |-
    Sends a verification email to the specified send-as alias address. The verification status must be pending.

    This method is only available to service account clients that have been delegated domain-wide authority.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/sendAs/{sendAsEmail}/verify
  tags: Verification
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailverify-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingssendassendasemailverify-post-openapi.md
- name: Gmail Get Vacation Settings
  x-api-slug: gmail
  description: Gets vacation responder settings.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/vacation
  tags: Vacation Settings
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsvacation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsvacation-get-openapi.md
- name: Gmail Update Vacation Settings
  x-api-slug: gmail
  description: Updates vacation responder settings.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/settings/vacation
  tags: Vacation Settings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridsettingsvacation-put-openapi.md
- name: Gmail Stop Push Notifications
  x-api-slug: gmail
  description: Stop receiving push notifications for the given user mailbox.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/stop
  tags: Push Notification
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridstop-post-openapi.md
- name: Gmail Get Threads
  x-api-slug: gmail
  description: Lists the threads in the user's mailbox.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/threads
  tags: Email Thread
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridthreads-get-openapi.md
- name: Gmail Delete Threads
  x-api-slug: gmail
  description: Immediately and permanently deletes the specified thread. This operation
    cannot be undone. Prefer threads.trash instead.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/threads/{id}
  tags: Email Thread
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridthreadsid-delete-openapi.md
- name: Gmail Get Threads
  x-api-slug: gmail
  description: Gets the specified thread.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/threads/{id}
  tags: Email Thread
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridthreadsid-get-openapi.md
- name: Gmail Modify Thread labels
  x-api-slug: gmail
  description: Modifies the labels applied to the thread. This applies to all messages
    in the thread.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/threads/{id}/modify
  tags: Email Thread
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridthreadsidmodify-post-openapi.md
- name: Gmail Trash Thread
  x-api-slug: gmail
  description: Moves the specified thread to the trash.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/threads/{id}/trash
  tags: Email Thread
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridthreadsidtrash-post-openapi.md
- name: Gmail UnTrash Threat
  x-api-slug: gmail
  description: Removes the specified thread from the trash.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/threads/{id}/untrash
  tags: Email Thread
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridthreadsiduntrash-post-openapi.md
- name: Gmail Send Push Notification
  x-api-slug: gmail
  description: Set up or update a push notification watch on the given user mailbox.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users//{userId}/watch
  tags: Push Notification
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/useridwatch-post-openapi.md
- name: Gmail
  x-api-slug: gmail
  description: The Gmail API is a RESTful API that can be used to access Gmail mailboxes
    and send mail. For most web applications (including mobile apps), the Gmail API
    is the best choice for authorized access to a users Gmail data.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/gmail-icon.png
  humanURL: https://www.google.com/gmail/
  baseURL: https://www.googleapis.com//gmail/v1/users
  tags: Gmail
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gmail/master/_listings/gmail/openapi.md
x-common:
- type: x-auth-scopes
  url: https://developers.google.com/gmail/api/auth/scopes
- type: x-authentication
  url: https://developers.google.com/gmail/api/auth/about-auth
- type: x-developer
  url: https://developers.google.com/gmail/api/
- type: x-documentation
  url: https://developers.google.com/gmail/api/v1/reference/
- type: x-twitter
  url: https://twitter.com/gmail
- type: x-website
  url: https://www.google.com/gmail/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---