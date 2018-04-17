# Models

The following section describes some Models that are used through the API and their corresponding fields

## Incident

| Attribute                    | Type        | Description                  |
| ---------                    | ---------   | --------                     |
| id                           | integer     | Unique identifier for record |
| contact_method               | string(100) | -                            |
| coordinator_name             | string(191) | -                            |
| coordinator_surname          | string(191) | -                            |
| coordinator_phone            | string(191) | -                            |
| coordinator_designation_code | string(191) | -                            |
| coordinator_facility         | string(191) | -                            |
| created_by                   | integer     | -                            |
| updated_by                   | integer     | -                            |
| escort_weight                | integer     | -                            |
| evac_code                    | string(191) | -                            |
| evac_decision_datetime       | datetime    | -                            |
| flight_priority              | integer     | -                            |
| initiated_by                 | string(255) | -                            |
| incident_datetime            | datetime    | -                            |
| patient_evacuated            | boolean     | -                            |
| originating_facility         | string(255) | -                            |
| patient_escorted             | boolean     | -                            |
| receiving_facility           | string(255) | -                            |
| reporter_name                | string(191) | -                            |
| reporter_surname             | string(191) | -                            |
| reporter_phone               | string(191) | -                            |
| reporter_designation_code    | string(191) | -                            |
| reporter_facility            | string(191) | -                            |
| rsq_number                   | string(191) | -                            |
| escort_given_name            | string(191) | -                            |
| escort_surname               | string(191) | -                            |
| atr_number                   | string(255) | -                            |
| tcr_number                   | string(255) | -                            |
| afr_number                   | string(255) | -                            |
| created_at                   | timestamp   | -                            |
| updated_at                   | timestamp   | -                            |

## Incident

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

| Value    | Description   |
|--------- | --------------|
| 10       | <= 2 seconds  |
| 20       | 3 seconds     |
| 30       | 4 seconds     |
| 40       | 5 seconds     |
| 50       | > 5 seconds   |

## CQI Record

// TODO

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