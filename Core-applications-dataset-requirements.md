The following provides the [required](#required), [recommended](#recommended) and [optional](#optional) fields for the core applicaions dataset.

# Core

### Required

Field                      | DataType | Description
---------------------------|----------|------------
ApplicationID              | TEXT     | The unique ID used internally by the municipality to identify the application.
Description                | TEXT     | A textual description of the application, potentially including lists and other formatting, with no length limit.
Address1 <sup>1</sup>      | TEXT     | The street address, or the first line of the address for multi-line addresses.
Address2 <sup>1</sup>                   | TEXT     | The second line of the address for multi-line addresses.
City <sup>1</sup>                       | TEXT     | The city of the address.
State <sup>1</sup>                      | TEXT     | The province or state of the address.
Zip <sup>1</sup>                        | TEXT     | The postal code or zip code of the address.
Geo <sup>1</sup>           | [GeoJSON](http://geojson.org/geojson-spec.html) | A GeoJSON object representing the location of the application. Points, multi-points, polygons and multi-polygons are all acceptable.
StatusCurrent <sup>2</sup> | TEXT     | Raw value indicating current status of the application.

### Recommended

Field                 | DataType | Description
----------------------|----------|------------
Link <sup>3</sup>     | TEXT     | A URL link to the municipality's record of the application on the municipal website.<sup>2</sup>
MunicipalContactName  | TEXT     | The name of the municipal contact.
MunicipalContactEmail | TEXT     | The municipal contact's email address.
StatusCurrentMapped   | TEXT     | StatusCurrent mapped to standardized values: <ul><li>Proposed</li><li>Approved</li><li>Withdrawn</li><li>Comment Period Begun</li><li>Comment Period Ended</li><li>On Hold</li><li>Completed</li><li>Review</li><li>Council Review</li><li>Issue Unresolved</li><li>Notice of Public Hearing</li><li>Cancelled</li></ul>
ApplicationType       | TEXT     | Raw values indicating type of application.
ApplicationTypeMapped | TEXT     | Application type mapped to standardized values: <ul><li>Development Permit</li><li>Development Variance Permit</li><li>Rezoning</li><li>Heritage Designation</li><li>Heritage Alteration Permit</li></ul>

### Optional

Field                    | DataType | Description
-------------------------|----------|------------
Abstract                 | TEXT     | A short-form textual description of the application, preferably under 140 characters.
MunicipalContactTitle    | TEXT     | The municipal contact's professional title.
MunicipalContactPhone    | TEXT     | The municipal contact's phone number.
ApplicantOrganization    | TEXT     | The name of the organization applying for the permit.
ApplicantContactName     | TEXT     | The name of the primary contact person within the applying organization.
ApplicantPhone           | TEXT     | The phone number for the applying organization.
ApplicantAddress1        | TEXT     | The street address, or the first line of the address for multi-line addresses.
ApplicantAddress2        | TEXT     | The second line of the address for multi-line addresses.
ApplicantCity            | TEXT     | The city of the address.
ApplicantState           | TEXT     | The province or state of the address.
ApplicantZip             | TEXT     | The postal code or zip code of the address.
StatusCurrentDescription | TEXT     | Longer description of current status.
ProjectName              | TEXT     | Name of the project related to the application.
ProjectID                | TEXT     | ID within the jurisdiction’s database of the project related to the application.

1. Either of `Address...` or `Geo` is required. If both are available, both should be provided. Neither `Address...` nor `Geo` is required if the optional Addresses dataset is provided.
2. StatusCurrent is not required if the optional Status change dataset is provided.
3. Ideally there should be no login. Users should be able to click on the link and be taken straight to all the online information regarding the permit.
