# zendesk-connector

The .authconfig file needs a "api_key" property

## Ticket
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
