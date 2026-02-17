Programmes endpoint
===================

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This endpoint lists programmes offered by the HEI.


Request method
--------------

 * Requests MUST be made with HTTP GET. Servers SHOULD reject all other request methods.


Request parameters
------------------

Parameters MUST be provided in a query string.
If no parameters are provided, then all programmes offered by the HEI are returned.
You MUST NOT provide more than one of the following filtering parameters:


### `ounit_id` (optional)

If given, then the server MUST limit the list of returned programmes IDs to only
such, which are tied to the Organisational Unit with the given ID.


### `programme_id` (optional)

Identifier of the programme to be returned.


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
