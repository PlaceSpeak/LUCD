An optional documents dataset is included in the case there is information available regarding documentation supporting a given application.

### Required

Field          | DataType | Description
---------------|----------|------------
ApplicationId  | TEXT     | Provides data link back to core applications information by application ID.
DocumentName   | TEXT     | The name of the document, e.g. "Streetscape Drawings".

### Recommended

Field          | DataType | Description
---------------|----------|------------
DocumentLink   | TEXT     | A URL link to a publicly-accessible online copy of the document.

### Optional

Field                    | DataType | Description
-------------------------|----------|------------
DocumentDescription      | TEXT     | A detailed description of the document.
Status                   | TEXT     | For documents associated with a particular stage in the application process, the status name of that stage, e.g. "Approval by council". Links document to the status change dataset.
StatusMapped             | TEXT     | For documents associated with a particular stage in the application process, the standardized status name of that stage, e.g. "Approved". Links document to the status change dataset.
PublicMeetingDescription | TEXT     | For documents associated with a particular public meeting, the description of that meeting, e.g. "Second open house". Links document to the public meetings dataset.
Language                 | TEXT     | The language used by the document, in [ISO 639-2](http://www.loc.gov/standards/iso639-2/php/code_list.php) two letter code format. Use a comma separated list for multiple languages.  E.g. "en" for English, "fr" for French, "en,fr" for English and French.