# The Land Use Change Data standard

## Current Version

The current version is `0.9`.

## Overview

The **LUCD standard** (optionally pronounced "lucid") is a proposed open standard for publishing municipal data related to land use change. The initially anticipated use cases are re-zoning applications and development permits.

If you have opinions about the standard please [submit an issue](https://github.com/PlaceSpeak/LUCD/issues) here, or get in touch at <hugh@placespeak.com>.

The standard is organized into **core** and **optional** datasets.

The core **applications** dataset provides basic information about individual land use change applications.

The optional **status change**, **public meetings** and **documents** datasets connect to the core applications dataset and provide supporting information about applications.

Within each of these datasets there are *required*, *recommended*, and *optional* fields:

* Required: Essential data field. The fields are absolutely necessary to have the basic level of data necessary to make this a useful dataset.
* Recommended: These fields are highly recommended in order to make the data useful. If these data are available, then they should be submitted.
* Optional: "Nice to have" fields. These fields also provide additional information, and if the data exists, they should be submitted.

This approach to data organization follows the [Building & Land Development Specification](http://permitdata.org/). Field naming conventions established in the BLDS have also been followed where appropriate.

## Requirements

The required fields for the data standard are described in the following documents, available in this code repository:

* [Core-applications-dataset-requirements.md](Core-applications-dataset-requirements.md)
* [Optional-status-change-dataset-requirements.md](Optional-status-change-dataset-requirements.md)
* [Optional-public-meeting-dataset-requirements.md](Optional-public-meeting-dataset-requirements.md)
* [Optional-document-dataset-requirements.md](Optional-document-dataset-requirements.md)
