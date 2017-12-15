# Patients

## Patients Collection

```shell
curl "HOST/api/v1/patients"
  -H "Authorization: Bearer token" -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{
    "success": true,
    "message": "",
    "data": [
        {
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
        },
        {
            "id": 2,
            "age": 28,
            "dob": null,
            "email": null,
            "emergency_contact_name": null,
            "emergency_contact_surname": null,
            "emergency_contact_phone": null,
            "emergency_contact_relationship": null,
            "gender": "Male",
            "given_names": "Juan",
            "height": 194,
            "history_significant": null,
            "history_significant_details": null,
            "history_has_allergies": null,
            "history_allergy_details": null,
            "history_resuscitation_plan": null,
            "history_resuscitation_details": null,
            "history_taking_meds": null,
            "history_meds_details": null,
            "incident_id": 2,
            "indigenous_status": "Non-Indigenous",
            "phone": null,
            "postcode": null,
            "presenting_condition": null,
            "severity": null,
            "state": null,
            "street_number": null,
            "street_address": null,
            "suburb": null,
            "surname": "Villegas",
            "unit_number": null,
            "weight": 84,
            "width": 80,
            "created_at": "2017-12-14 15:38:38",
            "updated_at": "2017-12-14 15:38:38",
            "formattedStreetAddress": ""
        }
    ]
}
```

Retrieves a collection of Patients

### HTTP Request

`GET HOST/api/v1/patients`

## Single Patient

```shell
curl "HOST/api/v1/patients/1"
  -H "Authorization: Bearer token" -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{
    "success": true,
    "message": "",
    "data": {
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
        "formattedStreetAddress": "1/14 ",
        "incident": {
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
            "updatedByUser": "Buckham Duffy"
        }
    }
}
```

Retrieves a particular Patient

### HTTP Request

`GET HOST/patients/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Patient to retrieve

## Delete Patient

```shell
curl "HOST/api/v1/patients/1"
  -X DELETE
  -H "Authorization: Bearer token"
```

> The above command returns JSON structured like this:

This endpoint deletes a specific Patient.

### HTTP Request

`DELETE HOST/patients/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Patient to delete