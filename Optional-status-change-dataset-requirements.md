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
StatusMapped   | TEXT     | Status mapped to standardized values:  StatusCurrent mapped to standardized values: <ul><li>Proposed</li><li>Approved</li><li>Withdrawn</li><li>Comment Period Begun</li><li>Comment Period Ended</li><li>On Hold</li><li>Completed</li><li>Review</li><li>Council Review</li><li>Issue Unresolved</li><li>Notice of Public Hearing</li><li>Cancelled</li></ul>

### Optional

Field             | DataType | Description
------------------|----------|------------
StatusDescription | TEXT     | Longer description of current status.
