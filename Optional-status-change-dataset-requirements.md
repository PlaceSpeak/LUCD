An optional application status change dataset is included in case there is detailed information available regarding the lifecycle of the permit. Fields included in the core dataset indicate current status, this dataset can be linked to provide a historical record.

[Required](#required), [recommended](#recommended) and [optional](#optional) fields are provided.

### Required

Field          | DataType          | Description
---------------|-------------------|------------
ApplicationId  | TEXT              | Provides data link back to core applications information by application ID.
Status         | TEXT              | Provides raw text for an application status.
StatusDate     | TEXT (YYYY-MM-DD) | Indicates the date at which this status was assigned in the jurisdiction's database.

### Recommended

Field          | DataType | Description
---------------|----------|------------
StatusMapped   | TEXT     | Status mapped to standardized values:  <ul><li>Application Accepted</li><li>Fees/Payment</li><li>In Review</li><li>Permit Issued</li><li>Inspection Phase</li><li>Permit Finaled</li><li>Permit Finaled with Conditions</li><li>Occupancy</li><li>Appeal</li><li>Permit Cancelled</li></ul>

### Optional

Field             | DataType | Description
------------------|----------|------------
StatusDescription | TEXT     | Longer description of current status.
