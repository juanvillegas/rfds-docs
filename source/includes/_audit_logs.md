# Audit Logs

**Admin Only** This endpoints are only to be used by users of type Admin.

## Audit Logs Collection

```shell
curl "HOST/api/v1/audit-logs"
  -H "Authorization: Bearer token" -H "Accept: application/json"
```

> The above command returns JSON structured as a typical paginated response, where each member of the data array is structured like follows:

```json
{
    "action":"viewed Patient #1",
    "action_html":"viewed <a href=\"/incidents/1\">Patient #1</a>",
    "created_at":"2018-06-27 13:04:23",
    "device":"HALO Portal",
    "event":"view_incident",
    "latitude":null,
    "location":"Unknown location",
    "longitude":null,
    "text":"2018-06-27 13:04:23 admin viewed Patient #1 HALO Portal from Unknown location",
    "text_html":"<span class=\"date\">2018-06-27 13:04:23</span> <span class=\"username\">admin</span> <span class=\"action\">viewed Patient #1</span> <span class=\"device\">on HALO Portal</span> from <span class=\"location\">Unknown location</span>",
    "user_id":1,
    "username":"admin"
}
```

### HTTP Request

`GET HOST/api/v1/audit-logs`

Get a collection of audit logs. See below supported query parameters to filter the results. 

### Query Parameters

| Parameter | Default | Description                                                                                                        |
| --------- | ------- | -----------                                                                                                        |
| user_id   | -       | The user_id who triggered the Audit log                                                                            |
| event_key | -       | The type of action to be returned. Valid actions are: 'login', 'create_incident', 'edit_incident', 'view_incident' |
| date_from | -       | -                                                                                                                  |
| date_to   | -       | -                                                                                                                  |

## Create Audit Log

### HTTP Request

Create a new Audit log. See Audit Log model for supported fields.


