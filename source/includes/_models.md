# Models

The following section describes the Models that are used through the API and their corresponding fields

## Incident

| Attribute                         | Type        | Description                                                                                   |
| ---------                         | ---------   | --------                                                                                      |
| atr_number                        | string(255) | -                                                                                             |
| id                                | integer     | Unique identifier for record                                                                  |
| contact_method                    | string(100) | -                                                                                             |
| coordinator_name                  | string(191) | -                                                                                             |
| coordinator_surname               | string(191) | -                                                                                             |
| coordinator_phone                 | string(191) | -                                                                                             |
| coordinator_designation_code      | string(255) | See valid designation codes below                                                             |
| coordinator_designation_code_nice | string      | Readonly. Formatted designation code. See designation codes below.                            |
| coordinator_facility              | string(191) | -                                                                                             |
| created_by                        | integer     | -                                                                                             |
| datetime_departed                 | datetime    | -                                                                                             |
| diagnosis_codes                   | array       | Readonly. The array will contain all the Diagnosis Code objects associated with this Incident |
| escort_weight                     | integer     | -                                                                                             |
| escort_given_name                 | string(191) | -                                                                                             |
| escort_surname                    | string(191) | -                                                                                             |
| evac_code                         | string(191) | -                                                                                             |
| evac_decision_datetime            | datetime    | -                                                                                             |
| first_contact_site                | string(255) | Nullable.                                                                                     |
| first_contact_datetime            | datetime    | Nullable.                                                                                     |
| flight_priority                   | integer     | -                                                                                             |
| handover_datetime                 | datetime    | -                                                                                             |
| handover_recipient                | string(255) | -                                                                                             |
| initiated_by                      | string(255) | -                                                                                             |
| incident_datetime                 | datetime    | -                                                                                             |
| patient_evacuated                 | boolean     | -                                                                                             |
| originating_facility              | string(255) | -                                                                                             |
| patient_escorted                  | boolean     | -                                                                                             |
| patient_transport_outcome         | string(255) | -                                                                                             |
| receiving_facility                | string(255) | -                                                                                             |
| reporter_name                     | string(191) | -                                                                                             |
| reporter_surname                  | string(191) | -                                                                                             |
| reporter_phone                    | string(191) | -                                                                                             |
| reporter_designation_code         | string(191) | See valid designation codes below                                                             |
| reporter_designation_code_nice    | string      | Readonly. Formatted designation code. See designation codes below.                            |
| reporter_facility                 | string(191) | -                                                                                             |
| rsq_number                        | string(191) | -                                                                                             |
| updated_by                        | integer     | -                                                                                             |
| tcr_number                        | string(255) | -                                                                                             |
| afr_number                        | string(255) | -                                                                                             |
| created_at                        | timestamp   | -                                                                                             |
| updated_at                        | timestamp   | -                                                                                             |

### Evacuation Codes

**Nice** value will be available in Incident model as **evac_code_nice**.

| Code | Nice                                            |
| ---- | ----                                            |
| T1   | T1 • Air, RFDS this base                        |
| T2   | T2 • Air, RFDS other base                       |
| T3   | T3 • Air, Charter                               |
| T4   | T4 • Air, Commercial                            |
| T5   | T5 • Air, Rotary Wing                           |
| T6   | T6 • Road, Queensland Ambulance Service         |
| T7   | T7 • Road, Other Ambulance Service              |
| T8   | T8 • Road, RFDS Vehicle                         |
| T9   | T9 • Road, Private Vehicle                      |
| T10  | T10 • Road, Commercial Vehicle                  |
| T11  | T11 • Boat                                      |
| T12  | T12 • Other                                     |
| T13  | T13 • Transport Cancelled                       |
| T14  | T14 • Transport of Non-RFDS Retrieval Team Only |

### Designation Codes

| Code | Nice                                   |
| ---- | ----                                   |
| m1.1 | M1.1 • Medical Officer, RFDS General   |
| m1.2 | M1.2 • Medical Officer, RFDS IPHCI     |
| m1.3 | M1.3 • Retrieval Registrar, RFDS       |
| m2.1 | M2.1 • Specialist, Emergency           |
| m2.2 | M2.2 • Specialist, Anaesthetic/ICU     |
| m2.3 | M2.3 • Specialist, O&G                 |
| m2.4 | M2.4 • Specialist, Paediatric/Neonatal |
| m2.5 | M2.5 • Specialist, Psychiatric         |
| m2.6 | M2.6 • Specialist, Other               |
| n1.1 | N1.1 • Registered Nurse, RFDS General  |
| n2   | N2 • Registered Nurse, Non-RFDS        |
| q1   | Q1 • QAS Officer                       |

## Patient

// TODO: help is required to add the patient model here :D

## Obstetrics Record

| Attribute           | Type          | Description                                          |
| ---------           | ---------     | --------                                             |
| id                  | integer       | Read only                                            |
| incident_id         | integer       | Read only                                            |
| patient_id          | integer       | Required                                             |
| cont_duration       | decima(5,1)   | Range: [0,9999]. eg: 1234.1, 1.1, 5 are valid values |
| cont_frequency_high | string(255)   | -                                                    |
| cont_frequency_low  | string(255)   | -                                                    |
| created_at          | datetime      | -                                                    |
| fhr                 | integer       | -                                                    |
| fm                  | string(255)   | -                                                    |
| mewts               | decimal(8,49) | Range: [0,9999]                                      |
| pv_loss             | string(255)   | -                                                    |
| observed_at         | datetime      | Required                                             |

## Vital Signs Record

| Attribute             | Type         | Description                                                                     |
| ---------             | ---------    | --------                                                                        |
| id                    | integer      | Read Only                                                                       |
| incident_id           | integer      | Read Only                                                                       |
| patient_id            | integer      | Required                                                                        |
| user_id               | integer      | Read Only                                                                       |
| blood_pressure_high   | integer      | -                                                                               |
| blood_pressure_low    | integer      | -                                                                               |
| blood_sugars          | decimal(8,4) | -                                                                               |
| fio2                  | string(255)  | -                                                                               |
| gcs                   | integer      | -                                                                               |
| gcs_e                 | integer      | -                                                                               |
| gcs_v                 | integer      | -                                                                               |
| gcs_m                 | integer      | -                                                                               |
| heart_rate            | decimal(8,4) | -                                                                               |
| o2_saturation         | decimal(8,4) | -                                                                               |
| pain_score            | integer      | Range: [0,10]                                                                   |
| respiratory_rate      | decimal(8,4) | -                                                                               |
| rhytm                 | string(191)  | -                                                                               |
| temperature           | decimal(8,4) | -                                                                               |
| normal_sys_bp         | integer      | -                                                                               |
| o2_flow_delivery      | string(255)  | -                                                                               |
| o2_flow_rate          | decimal(8,4) | -                                                                               |
| consciousness         | string(191)  | -                                                                               |
| respiratory_distress  | string(191)  | -                                                                               |
| capillary_refill_time | integer      | See [this](#capillary-refill-time-field-values) for a description of each value |
| observed_at           | datetime     | Required.                                                                       |                                                                            |

### Capillary Refill Time Field Values

| Value     | Description    |
|-- ------- | ------------ --|
| 10        | <= 2 seconds   |
| 20        | 3 seconds      |
| 30        | 4 seconds      |
| 40        | 5 seconds      |
| 50        | > 5 seconds    |

## CQI Record

// TODO: help would be appreciated

## Audit Log

| Attribute          | Type        | Description                                                                              |
| ---------          | ----------- | -----------                                                                              |
| device             | string(255) | Required. Its the name of the device reporting the audit log.                            |
| event              | enum        | Required. valid values: 'login', 'create_incident', 'edit_incident', 'view_incident'     |
| incident_id        | integer     | Optional. ID of the incident. Only required for certain event types.                     |
| user_id            | integer     | Optional. ID of the reporting user. If not provided, the logged in user id will be used. |
| location           | array       | Optional. If provided, it must include the following subfields:                          |
| location.latitude  | string      | Latitude of the intended location                                                        |
| location.longitude | string      | Longitude of the intended location.                                                      |

## Diagnosis Code Chapter

| Attribute | Type        | Description |
| --------- | ----------- | ----------- |
| id        | integer     | -           |
| name      | string(255) | -           |

## Diagnosis Code

| Attribute         | Type        | Description |
| ---------         | ---------   | --------    |
| id                | integer     | -           |
| chapter_id        | integer     | -           |
| code              | integer     | string(170) |
| short_description | string(255) | -           |
| long_description  | mediumtext  | -           |

## Risks List

| Name                       | Field                           | Accepted values                                    |
| ---                        | ----                            | ---                                                |
| Cabin Altitude Restriction | risk_cabin_altitude_restriction | 0: No restrictions, 5: < 4000 feet, 10 < Sea level |
| Positioning Requirement    | risk_positioning_requirement    | String, 191 chars                                  |
| Pressure Area device       | risk_pressure_area_device       | Boolean                                            |
| Pressure Injury            | risk_pressure_injury            | String, 30 chars                                   |
| Infectious                 | risk_infectious                 | String, 255 chars                                  |
| Agitated Patient Score     | risk_agitated_patient_score     | Number between 0 and 60, multiple of 5             |

# Datatypes

## Decimal

Whenever a _decimal_ field is described, the number of integer and decimal digits supported by the field are
also specified. A field described as decimal(x,y) will have X digits in total, of which X-Y correspond to the integer
part and Y digits to the decimal part.

For example, if a field is described as decimal(10,4), then the field supports up to 6 integer digits and 4 decimal digits.
For this field, the following examples represent valid values: **1, 1.1, 1.2345, 100000.1234, 123456**.

## Datetime Formats

| Identifier | Format         | Example             |
| ---        | ----           | ---                 |
| datetime   | Y-m-d H:i:s    | 2018-12-21 00:00:00 |
| ISO8601    | TBD            | TBD                 |
| timestamp  | Unix timestamp | -                   |