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
    ]
```

Notes:
* ``description`` can only be set on the initial insert, after that it cannot be updated
* ``raw_subject`` will override ``subject`` if present in an update
