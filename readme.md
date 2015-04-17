# The Land Use Change Data standard

The **LUCD standard** (optionally pronounced "lucid") is a proposed open standard for publishing municipal data related to land use change. The initially anticipated use cases are re-zoning applications and development permits.

If you have opinions about the standard please [submit an issue](https://github.com/PlaceSpeak/LUCD/issues) here, or get in touch at <hugh@placespeak.com>.

## What's here

**LUCD fields.txt**

This is a list of the required and optional fields for the LUCD standard. This schema is the core component of the standard. These fields can be published in a number of formats, including XML and JSON.

Required fields are marked with an asterisk. 

In cases where multiple instances of a data type can be present (e.g. a re-zoning affecting more than one street address or a development application that has been assigned more than one status during its assessment) square brackets are used to indicate where the fields for that data type can be repeated.

**LUCD fields description.md**

This is a table providing descriptions of the fields in `LUCD fields.txt`.

**example.json**

This is an example of a re-zoning and development application published using the LUCD schema in the **JSON** data format.

*More applications illustrating additional formatting will be added*.

**example.xml**

This is an example of a re-zoning and development application published using the LUCD schema in the **XML** data format.

**example.csv**

This is an example of a re-zoning and development application published using the LUCD schema in the **Comma Separated Values** data format. Note that some fields in the data standard are optionally repeated, which can be difficult to encode in CSV format. One option for doing so is presented here.

**readme.md**

This file.
