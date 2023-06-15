# zendesk-connector

The .authconfig file needs a "api_key" property

## Tickets
Insert:

Minimal object:
```
{
  "_id": "1",
  "$origin": "1",
  "description": "Foo",
  "priority": "urgent",
  "subject": "My printer is on fire"
}
```

Updated:
```
    "$based_on_properties": [
        "description",
        "allow_attachments",
        "allow_channelback",
        "brand_id",
        "collaborator_ids",
        "created_at",
        "custom_fields",
        "custom_status_id",
        "email_cc_ids",
        "follower_ids",
        "followup_ids",
        "from_messaging_channel",
        "group_id",
        "has_incidents",
        "id",
        "is_public",
        "organization_id",
        "priority",
        "raw_subject",
        "requester_id",
        "sharing_agreement_ids",
        "status",
        "subject",
        "submitter_id",
        "tags",
        "ticket_form_id",
        "updated_at",
        "url"
        ],
```

Notes:
* ``description`` can only be set on the initial insert, after that it cannot be updated
* ``raw_subject`` will override ``subject`` if present in an update


## Ticketcomments
Share is not implemented yet. Create and update must be done through the Ticket endpoint: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_comments/


## Organizations
Insert:

Minimal object:
```
{
    "name": "An organization"
}
```

Update:
```
    "$based_on_properties": [
        "name",
        "created_at",
        "details",
        "domain_names",
        "external_id",
        "group_id",
        "id",
        "notes",
        "organization_fields",
        "shared_comments",
        "shared_tickets",
        "tags",
        "updated_at",
        "url"
        ],
```

## Users
Insert:

Minimal object:
```
{
  "email": "testme@example.com",
  "name": "Test Testesen",
  "skip_verify_email": true
}
```

Updated:
```
    "$based_on_properties": [
      "phone",
      "name",
      "active",
      "created_at",
      "custom_role_id",
      "default_group_id",
      "email",
      "iana_time_zone",
      "id",
      "last_login_at",
      "locale",
      "locale_id",
      "moderator",
      "only_private_comments",
      "report_csv",
      "restricted_agent",
      "role",
      "role_type",
      "shared",
      "shared_agent",
      "suspended",
      "time_zone",
      "updated_at",
      "url",
      "verified",
      "phone"
    ]
```

## Identities
Insert:

Minimal object:
```
{
{
  "skip_verify_email": true,
  "type": "email",
  "user_id": 16161714724369,
  "value": "hm@bar.com"
}
```

Updated:
```
    "$based_on_properties": [
      "type",
      "created_at",
      "deliverable_state",
      "id",
      "primary",
      "updated_at",
      "url",
      "user_id",
      "value",
      "verified"
    ]
```
