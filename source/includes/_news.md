# News and Updates

## Updates Week June 28th 2018

### Designation Codes

**Breaking Changes** Fields that deal with designation codes have just received a major update. We switched from 
arbitrary text fields to only allowing a set of predefined designation codes. This means that clients must check the 
corresponding documentation (see Incident Model description) for supported designation codes. The Incident model now
also includes a readonly field with the presentation name for the designation code.

### New fields on Incident model

The incident model was upgraded with new fields:

- patient_transport_outcome: Arbitrary 255 max length string.
- risk_cabin_altitude_restriction: See patient model 
- handover_recipient: See incident model
- datetime_departed: See incident model

### Added section for Audit Logs management

Methods for GETting and POSTing Audit Logs are now described in the api docs.

## Updates Week 4 - May 2018

### Added first_contact_datetime and first_contact_site to Incident model

See Incident model description for more information.

## Updates Week 3 - May 2018

### handover_datetime attribute added to Incident model

See Incident model description for more information.

### Breaking changes on Incident Update response

Until today, the api responded with the string 'updated' in the data property of the returned JSON.
This has been removed to standardize the responses of the api in general.

### Diagnosis Codes removed from Patient, added to Incident

As of now, Diagnosis Codes are a property of the Incident model, not the Patient anymore.

Also, the database now supports having Incidents with many Diagnosis Codes. At the moment, the 
limit is capped to 2 codes per Incident.

To set the Diagnosis Codes for an Incident, use the new "diagnosis_codes" property of the Incident model
to provide the ids of the desired Diagnosis Codes. More information in the corresponding endpoint description.

### Camel Case attributes replaced with snake_case counterparts

In an effort to standardize the responses of the API, some of the attributes returned in some models
were changed from SnakeCase to their corresponding snake_case versions. So for example, the _updatedByUser_ attribute
in the Incident model is now _updated_by_user_. Check the corresponding API sections for more changes.   