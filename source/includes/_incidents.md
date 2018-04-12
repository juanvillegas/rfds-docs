# Incidents

## Incidents Collection

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

| Parameter | Default | Description                                                        |
| --------- | ------- | -----------                                                        |
| search    | -       | If provided, a search will be performed using `search` as keyword. |
| per_page  | 10      | The maximum number of records to be returned on each request.      |

### Response Fields

| Field                        | Type    | Description |
| ---------                    | ------- | ----------- |
| id                           | integer | -           |
| coordinator_name             | string  | -           |
| coordinator_surname          | string  | -           |
| coordinator_phone            | string  | -           |
| coordinator_designation_code | string  | -           |
| coordinator_facility         | string  | -           |
| created_by                   | integer | -           |
| updated_by                   | integer | -           |


## Single Incident

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

| Parameter | Description                        |
| --------- | -----------                        |
| ID        | The ID of the Incident to retrieve |

## Delete Incident

```shell
curl "HOST/api/v1/incidents/1"
  -X DELETE
  -H "Authorization: Bearer token"
```

This endpoint deletes a specific Incident.

### HTTP Request

`DELETE HOST/incidents/<ID>`

### URL Parameters

| Parameter | Description                      |
| --------- | -----------                      |
| ID        | The ID of the Incident to delete |

# Incident Medication

## Retrieve Medication Chart

### HTTP Request

`GET HOST/incidents/{incident_id}/medication-chart`

### URL Parameters

| Parameter   | Description | Required   |
| ---------   | ----------- | ---------- |
| incident_id | Incident ID | Yes        |

### Response Fields

The response will be an array, where each member contains the following fields:

| Field           | Type         | Description |
| ---------       | -------      | ----------- |
| administered_at | datetime     | -           |
| administered_by | string(191)  | -           |
| dosage          | decimal(8,4) | -           |
| medication_name | string(191)  | -           |
| prescribed_by   | string(191)  | -           |
| route           | string(191)  | -           |
| unit            | string(191)  | -           |

## Create Medication

### HTTP Request

`POST HOST/incidents/{incident_id}/medication-chart`

### URL Parameters

| Parameter   | Description | Required   |
| ---------   | ----------- | ---------- |
| incident_id | Incident ID | Yes        |

### Response Fields

The response will be an array, where each member contains the following fields:

| Field           | Type         |
| ---------       | -------      |
| dosage          | decimal(8,4) |
| medication_name | string(191)  |
| administered_at | datetime     |
| administered_by | string(191)  |
| prescribed_by   | string(191)  |
| route           | string(191)  |
| unit            | string(191)  |

# Incident Vital Signs

## Retrieve Vital Signs

```shell
curl "HOST/api/v1/incidents/1/vital-signs/1"
  -H "Authorization: Bearer token"
```
Retrieves Vital Signs for the given Incident.

### HTTP Request

`GET HOST/incidents/{incident_id}/vital-signs/{vital_signs_id?}`

If _vital_signs_id_ is not provided, the latest Vital Signs records available for the Incident 
will be returned.

### URL Parameters

| Parameter      | Description    | Required   |
| ---------      | -----------    | ---------- |
| incident_id    | Incident ID    | Yes        |
| vital_signs_id | Vital Signs ID | No         |

> The above command returns JSON structured like this:

```json
{
    "incident_id": 1,
    "patient_id": 1,
    "blood_pressure_high": 100,
    "blood_pressure_low": 90,
    "temperature": 14,
    "fio2": 12,
    "respiratory_rate": null,
    "rhytm": null,
    "gcs": null,
    "gcs_e": null,
    "gcs_v": null,
    "gcs_m": null,
    "heart_rate": null,
    "blood_sugars": null,
    "cewt": null,
    "o2_saturation": null,
    "user": {
        "name": "Buckham Duffy"
    },
    "normal_sys_bp": null,
    "o2_flow_delivery": "None",
    "o2_flow_rate": null,
    "consciousness": null,
    "respiratory_distress": null,
    "capillary_refill_time": null,
    "observation_time": null,
    "pain_score": null,
    "created_at": "2017-12-03T14:42:30+00:00"
}
```

## Create Vital Signs

```shell
curl "HOST/api/v1/incidents/1/vital-signs"
  -X POST
  -H "Authorization: Bearer token"
```

> Example request

```json
{
    "patient_id": 1,
    "blood_pressure_high": 100,
    "blood_pressure_low": 90,
    "temperature": 14,
    "fio2": 12,
    "heart_rate": 1,
    "respiratory_rate": 1,
    "rhytm": 1,
    "gcs": 1,
    "blood_sugars": 1,
    "cewt": 1,
    "o2_saturation": 1,
    "pain_score": 1,
    "created_at": "2018-04-04 00:00:00"
}
```
Creates Vital Signs for the given Incident

### HTTP Request

`POST HOST/incidents/{incident_id}/vital-signs`

### URL Parameters

| Parameter   | Description | Required   |
| ---------   | ----------- | ---------- |
| incident_id | Incident ID | Yes        |

### Request Parameters

See [Vital Signs Model Description](#vital-signs-record)

## Retrieve History
//TODO

# Incident Obstetrics

## Retrieve Obstetrics

```shell
curl "HOST/api/v1/incidents/1/obstetrics/1"
  -H "Authorization: Bearer token"
```
Retrieves Obstetrics for the given Incident.

### HTTP Request

`GET HOST/incidents/{incident_id}/obstetrics/{obstetrics_id?}`

### URL Parameters

| Parameter     | Description                                                                                    |
| ---------     | -----------                                                                                    |
| incident_id   | Required.                                                                                      |
| obstetrics_id | Optional. If none is provided, the latest Obstetrics record for the Incident will be returned. |

> Example response:

```json
{
    "incident_id": 1,
    "patient_id": 1,
    "fhr": 1,
    "fm_high": 1,
    "fm_low": 1,
    "cont_frequency": 1,
    "pv_loss": 1,
    "mewts": 1,
    "cont_duration": 1,
    "user": {
        "name": "Buckham Duffy"
    },
    "created_at": "2017-12-12T00:00:00+00:00"
}
```

## Retrieve Obstetrics History

```shell
curl "HOST/api/v1/incidents/1/obstetrics/history"
  -H "Authorization: Bearer token"
```
Retrieves Obstetrics History for the given Incident.

### HTTP Request

`GET HOST/incidents/{incident_id}/obstetrics/history`

### URL Parameters

| Parameter   | Description |
| ---------   | ----------- |
| incident_id | Incident ID |

### Request Parameters

| Parameter | Values         | Default |
| --------- | -----------    | ------- |
| format    | full, compact  | compact |
| per_page  | integer [1, +] | 10      |
| page      | integer [1, +] | 1       |

### Response Fields

If format **compact** was specified, the response will be an array, where each member contains 
the following fields:

| Field      | Type     |
| ---------  | -------  |
| id         | integer  |
| created_at | datetime |

If format **full** was specified, the response will be an array, where each member contains 
the fields indicated in the [Obstetrics Model Description](#obstetrics-record) section.

**user** is an object containing the following fields:

| Field   | Type     |
|-- ----- | ------ --|
| name    | string   |

## Create Obstetrics

```shell
curl "HOST/api/v1/incidents/1/obstetrics"
  -X POST
  -H "Authorization: Bearer token"
```

> Example request:

```json
{
    "patient_id": 1,
    "fhr": 1,
    "fm_high": 1,
    "fm_low": 1,
    "cont_frequency": 1,
    "pv_loss": 1,
    "mewts": 1,
    "cont_duration": 1
}
```
Creates Vital Signs for the given Incident

### HTTP Request

`POST HOST/incidents/{incident_id}/vital-signs`

### URL Parameters

| Parameter   | Description |
| ---------   | ----------- |
| incident_id | Incident ID |

> Example Response 422:

```json
{
    "message": "The given data was invalid.",
    "errors": {
        "patient_id": [
            "The patient id field is required."
        ]
    }
}
```