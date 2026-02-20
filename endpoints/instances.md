Instances endpoint
==================

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This endpoint lists instances (LOI) of a given course (LOS).


Request method
--------------

 * Requests MUST be made with HTTP GET. Servers SHOULD reject all other request methods.


Request parameters
------------------

Parameters MUST be provided in a query string. Exactly one of the following
parameters MUST be present:


### `los_id` (optional)

Identifier of the course (LOS) which instances are to be returned.


### `loi_id` (optional)

Identifier of the course instance (LOI) to be returned.


Handling of invalid parameters
------------------------------

 * General [error handling rules][error-handling] apply.


Response
--------

Servers MUST respond with a valid XML document described by the
[instances-response.xsd](instances-response.xsd) schema. See the schema annotations
for further information.


[develhub]: http://developers.erasmuswithoutpaper.eu/
[statuses]: https://github.com/erasmus-without-paper/ewp-specs-management#statuses
[error-handling]: https://github.com/erasmus-without-paper/ewp-specs-architecture#error-handling
