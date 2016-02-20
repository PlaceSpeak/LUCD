An optional public meetings dataset is included in case there is more detailed information available about public engagement with respect to a given application. This can include past or scheduled meetings.

### Required

Field                       | DataType          | Description
----------------------------|-------------------|------------
PublicMeetingDate           | TEXT (YYYY-MM-DD) | The date the public meeting was or will be held.
PublicMeetingDescription    | TEXT              | A description of the nature of the public meeting.

### Optional

Field                  | DataType     | Description
-----------------------|--------------|------------
PublicMeetingAddress1  | TEXT         | The street address of the public meeting, or the first line of the address for multi-line addresses.
PublicMeetingAddress2  | TEXT         | The second line of the address for multi-line addresses.
PublicMeetingCity      | TEXT         | The city of the address.
PublicMeetingState     | TEXT         | The province or state of the address.
PublicMeetingLink      | TEXT         | A link to the online component of the public meeting, if applicable.
PublicMeetingStartTime | TEXT (HH:MM) | The start time of the public meeting. Use local time zone, or local time with [UTC offset](https://en.wikipedia.org/wiki/ISO_8601#Time_offsets_from_UTC) (hh:mmZ±hh:mm).
PublicMeetingEndTime   | TEXT         | The end time of the public meeting.
