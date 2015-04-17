This document contains a field-by-field description of the data structure for the Land Use Change Data standard. The canoncial list of fields is in [LUCD fields.txt](LUCD fields.txt), which also shows the hierarchical relationships among the fields described here.

field          | required?  | repeatable? | description
-------------- | ---------- | ----------- | -----------
application    | yes        | no          | A container for the fields associated with this application, as listed below.
id             | yes        | no          | The unique ID used internally by the municipality to identify the application.
short name     | yes        | no          | A short-form textual description of the application, preferably under 140 characters.
description    | yes        | no          | A textual description of the application, potentially including lists and other formatting, with no length limit.
URL            | yes        | no          | A link to the municipality's record of the application on the municipal website (or just a link to the most relevant page on the municipal website, if no application-specific page is available).
associated applications | no| no          | A container for any associated applications. E.g., if the application is a re-zoning application and there are related development and heritage designation applications being submitted in parallel.
associated application | yes| yes         | A container for the associated application information. Not required if there are no associated applications.
id             | yes        | no          | The unique ID used internally by the municipality to identify the associated application. Not required if there is no associated application.
URL            | no         | no          | A link to the municipality's record of the associated application on the municipal website.
addresses      | at least 1 address or 1 geo | no | A container for the address or addresses, in case there are multiple addresses. The application should include at least one address **or** one geo object, i.e. if at least one address is provided a geo object is not required, and vice a versa.
address        | see above  | yes         | A container for the address information.
street 1       | yes        | no          | The street address, or the first line of the address for multi-line addresses.
street 2       | no         | no          | The second line of the address for multi-line addresses.
street 3       | no         | no          | The third line of the address for multi-line addresses.
city           | yes        | no          | The city of the address.
province/state | yes        | no          | The province or state of the address.
postal/zip     | yes        | no          | The postal code or zip code of the address.
geos           | at least 1 address or 1 geo | no | A container for the geo object or geo objects, in case there are multiple geo objects. The application should include at least one address **or** one geo object, i.e. if at least one address is provided a geo object is not required, and vice a versa.
geo            | see above  | yes         | A container for the geo information.
geo name       | no         | no          | A short-form description of the location represented by the geo object.
geo object     | yes        | no          | An [OGC simple feature](http://www.opengeospatial.org/standards/sfa) object representing the location of the application, typically formatted as [Well Known Text](http://en.wikipedia.org/wiki/Well-known_text). Points, multi-points, polygons and multi-polygons are all acceptable.
applicant      | no         | no          | A container for the applicant information.
contact name   | no         | no          | The name of the primary contact person within the applying organization.
organization   | no         | no          | The name of the organization applying for the permit.
phone          | no         | no          | The phone number for the applying organization.
address        | no         | no          | A container for the applicant's address information.
street 1       | yes        | no          | The street address for the applicant, or the first line of the address for multi-line addresses.
street 2       | no         | no          | The second line of the address for multi-line addresses.
street 3       | no         | no          | The third line of the address for multi-line addresses.
city           | yes        | no          | The city of the applicant's address.
province/state | yes        | no          | The province or state of the applicant's address.
postal/zip     | yes        | no          | The postal code or zip code of the applicant's address.
municipal contacts | at least 1 | no      | A container for the municipal contact or contacts, in case there are multiple contacts.
contact        | see above  | yes         | A container for the for contact information for a point of contact within the municipality for this application.
name           | no         | no          | The name of the municipal contact.
title          | no         | no          | The municipal contact's professional title.
email          | yes        | no          | The municipal contact's email address.
phone          | no         | no          | The municipal contact's phone number.
address        | no         | no          | A container for the municipal contact's address information.
street 1       | yes        | no          | The street address, or the first line of the address for multi-line addresses.
street 2       | no         | no          | The second line of the address for multi-line addresses.
street 3       | no         | no          | The third line of the address for multi-line addresses.
city           | yes        | no          | The city of the address.
province/state | yes        | no          | The province or state of the address.
postal/zip     | yes        | no          | The postal code or zip code of the address.
statuses       | at least 1 | no          | A container for the application status or statuses, in case there are multiple statuses.
status         | see above  | yes         | A container for information about the/a procedural status of the application.
status name    | yes        | no          | The status of the application, e.g. submitted, pending, re-submitted, approved, etc.
status date    | yes        | no          | The [date](http://en.wikipedia.org/wiki/ISO_8601) at which the application was assigned the above status.
public meetings| no         | no          | A container for the public meeting or meetings, in case there are multiple meetings.
public meeting | no         | yes         | Information about public meetings held by the municipality or proponent regarding the application, e.g. open houses and consultations.
date           | no         | no          | The [date](http://en.wikipedia.org/wiki/ISO_8601) the public was or will be held.
location       | no         | no          | A container for address information about where the public meeting was or will be held, if applicable.
street 1       | yes        | no          | The street address, or the first line of the address for multi-line addresses.
street 2       | no         | no          | The second line of the address for multi-line addresses.
street 3       | no         | no          | The third line of the address for multi-line addresses.
city           | yes        | no          | The city of the address.
province/state | yes        | no          | The province or state of the address.
description    | no         | no          | A description of the nature of the public meeting.
URL            | no         | no          | A link to the online component of the public meeting, if applicable.
documents      | no         | no          | A container for information about the document or documents, in case there are multiple documents.
document       | no         | yes         | A container for information about the document. At least two of name/abstract/URL should be provided.
name           | no         | no          | The name of the document, e.g. "Streetscape Drawings".
URL            | no         | no          | A link a publicly-accessible online copy of the document. 
