If more than one address is sometimes associated with a given application this additional dataset can be used to provide multiple addresses, linked to their associated application via the `ApplicationId`.

Field                 | DataType | Description
----------------------|----------|------------
ApplicationID         | TEXT     | The unique ID used internally by the municipality to identify the application.
Address1 <sup>1</sup> | TEXT     | The street address, or the first line of the address for multi-line addresses.
Address2 <sup>1</sup> | TEXT     | The second line of the address for multi-line addresses.
City <sup>1</sup>     | TEXT     | The city of the address.
State <sup>1</sup>    | TEXT     | The province or state of the address.
Zip <sup>1</sup>      | TEXT     | The postal code or zip code of the address.
Geo <sup>1</sup>      | [GeoJSON](http://geojson.org/geojson-spec.html) | A GeoJSON object representing the location of the application. Points, multi-points, polygons and multi-polygons are all acceptable.

1. Either of `Address...` or `Geo` is required. If both are available, both should be provided. Neither `Address...` nor `Geo` is required if the optional Addresses dataset is provided.
