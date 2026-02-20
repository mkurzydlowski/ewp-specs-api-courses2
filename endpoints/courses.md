Courses endpoint
================

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This endpoint lists courses (LOS).


Request method
--------------

 * Requests MUST be made with HTTP GET. Servers SHOULD reject all other request methods.


Request parameters
------------------

Parameters MUST be provided in a query string.
If no parameters are provided, then all courses offered by the HEI are returned.
You MUST NOT provide more than one of the following filtering parameters:


### `ounit_id` (optional)

If given, then the server MUST limit the list of returned courses to only
such, which are tied to the organisational unit with the given ID.


### `programme_id` (optional)

If given, then the server MUST limit the list of returned courses to only
such, which are tied to the programme with the given ID.

See EWP Programmes API for more details.


### `los_id` (optional)

Identifier of the course (LOS) to be returned.


You MAY also add this parameter:


### `include_deprecated` (optional)

If given, then the server MUST include deprecated courses in the list of returned courses.


Handling of invalid parameters
------------------------------

 * General [error handling rules][error-handling] apply.


Response
--------

Servers MUST respond with a valid XML document described by the
[courses-response.xsd](courses-response.xsd) schema. See the schema annotations
for further information.


[develhub]: http://developers.erasmuswithoutpaper.eu/
[statuses]: https://github.com/erasmus-without-paper/ewp-specs-management#statuses
[error-handling]: https://github.com/erasmus-without-paper/ewp-specs-architecture#error-handling
