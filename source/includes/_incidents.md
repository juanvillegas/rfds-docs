# Incidents

## Collection

```shell
curl "HOST/api/v1/incidents"
  -H "Authorization: Bearer token" -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{
    "success": true,
    "message": "",
    "data": {
        "current_page": 1,
        "data": [
            {
                "id": 1,
                "contact_method": "Phone",
                "coordinator_name": "coord name",
                "coordinator_surname": "coord surname",
                "coordinator_phone": 123123123,
                "coordinator_designation_code": "code123",
                "coordinator_facility": "san juan del sur",
                "created_by": 1,
                "updated_by": 1,
                "escort_weight": 60,
                "evac_code": "code123",
                "evac_decision_datetime": null,
                "flight_priority": 2,
                "initiated_by": "RFDS",
                "incident_datetime": null,
                "patient_evacuated": 1,
                "originating_facility": "san juan del sur",
                "patient_escorted": null,
                "receiving_facility": null,
                "reporter_name": null,
                "reporter_surname": null,
                "reporter_phone": null,
                "reporter_designation_code": null,
                "reporter_facility": null,
                "rsq_number": 123,
                "created_at": "2017-12-03 14:38:09",
                "updated_at": "2017-12-03 14:38:09",
                "createdByUser": "Buckham Duffy",
                "updatedByUser": "Buckham Duffy",
                "patient": {
                    "id": 1,
                    "age": 28,
                    "dob": "2016-11-30",
                    "email": "patient-contact@email.com",
                    "emergency_contact_name": "mario",
                    "emergency_contact_surname": "villegas",
                    "emergency_contact_phone": 123123123,
                    "emergency_contact_relationship": "parent",
                    "gender": "Male",
                    "given_names": "juan manuel",
                    "height": 194,
                    "history_significant": 1,
                    "history_significant_details": "history",
                    "history_has_allergies": 1,
                    "history_allergy_details": "allergy details",
                    "history_resuscitation_plan": 1,
                    "history_resuscitation_details": "resuscitation",
                    "history_taking_meds": 1,
                    "history_meds_details": "extra meds",
                    "incident_id": 1,
                    "indigenous_status": "Non-Indigenous",
                    "phone": 123123123,
                    "postcode": 1414,
                    "presenting_condition": "presenting condition here",
                    "severity": 2,
                    "state": "QLD",
                    "street_number": 14,
                    "street_address": null,
                    "suburb": "Brisbane",
                    "surname": "villegas",
                    "unit_number": 1,
                    "weight": 87,
                    "width": 60,
                    "created_at": "2017-12-03 14:38:10",
                    "updated_at": "2017-12-03 14:38:10",
                    "formattedStreetAddress": "1/14 "
                }
            }
        ],
        "from": 1,
        "last_page": 1,
        "per_page": 10,
        "to": 1,
        "total": 1
    }
}
```

Get a collection of Incidents, optionally filtered by a search value.

### HTTP Request

`GET HOST/api/v1/incidents?search=keyword&per_page=20`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
search | - | If provided, a search will be performed using `search` as keyword.
per_page | 10 | The maximum number of records to be returned on each request.

## Single

```shell
curl "HOST/api/v1/incidents/1"
  -H "Authorization: Bearer token" -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{
    "success": true,
    "message": "",
    "data": {
        "id": 1,
        "coordinator_name": "coord name",
        "coordinator_surname": "coord surname",
        "coordinator_phone": 123123123,
        "coordinator_designation_code": "code123",
        "coordinator_facility": "san juan del sur",
        "created_by": 1,
        "updated_by": 1,
        "escort_weight": 60,
        "evac_code": "code123",
        "evac_decision_datetime": null,
        "flight_priority": 2,
        "initiated_by": "RFDS",
        "incident_datetime": null,
        "patient_evacuated": 1,
        "originating_facility": "san juan del sur",
        "patient_escorted": null,
        "receiving_facility": null,
        "reporter_name": null,
        "reporter_surname": null,
        "reporter_phone": null,
        "reporter_designation_code": null,
        "reporter_facility": null,
        "rsq_number": 123,
        "created_at": "2017-12-03 14:38:09",
        "updated_at": "2017-12-03 14:38:09",
        "createdByUser": "Buckham Duffy",
        "updatedByUser": "Buckham Duffy",
        "patient": {
            "id": 1,
            "age": 28,
            "dob": "2016-11-30",
            "email": "patient-contact@email.com",
            "emergency_contact_name": "mario",
            "emergency_contact_surname": "villegas",
            "emergency_contact_phone": 123123123,
            "emergency_contact_relationship": "parent",
            "gender": "Male",
            "given_names": "juan manuel",
            "height": 194,
            "history_significant": 1,
            "history_significant_details": "history",
            "history_has_allergies": 1,
            "history_allergy_details": "allergy details",
            "history_resuscitation_plan": 1,
            "history_resuscitation_details": "resuscitation",
            "history_taking_meds": 1,
            "history_meds_details": "extra meds",
            "incident_id": 1,
            "indigenous_status": "Non-Indigenous",
            "phone": 123123123,
            "postcode": 1414,
            "presenting_condition": "presenting condition here",
            "severity": 2,
            "state": "QLD",
            "street_number": 14,
            "street_address": null,
            "suburb": "Brisbane",
            "surname": "villegas",
            "unit_number": 1,
            "weight": 87,
            "width": 60,
            "created_at": "2017-12-03 14:38:10",
            "updated_at": "2017-12-03 14:38:10",
            "formattedStreetAddress": "1/14 "
        }
    }
}
```

Retrieves a particular Incident

### HTTP Request

`GET HOST/incidents/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Incident to retrieve

## Delete

```shell
curl "HOST/api/v1/incidents/1"
  -X DELETE
  -H "Authorization: Bearer token"
```

> The above command returns JSON structured like this:

This endpoint deletes a specific Incident.

### HTTP Request

`DELETE HOST/incidents/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Incident to delete