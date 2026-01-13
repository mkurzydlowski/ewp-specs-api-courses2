Course Index endpoint
===================

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This endpoint allows clients to see the list of all courses known to
a particular HEI.


Request method
--------------

 * Requests MUST be made with either HTTP GET or HTTP POST method. Servers MUST
   support both these methods. Servers SHOULD reject all other request methods.

 * Clients are advised to use POST when passing a large number of parameters
   (servers MAY set a limit on their GET query string length).


Request parameters
------------------

Parameters MUST be provided either in a query string (for GET requests), or in
the `application/x-www-form-urlencoded` format (for POST requests).


### `ounit_id` (optional)

If given, then the server MUST limit the list of returned course IDs to only
such, which are tied to the Organizational Unit with the given ID.


### `programme_id` (optional)

If given, then the server MUST limit the list of returned course IDs to only
such, which are tied to the Programme with the given ID.


Handling of invalid parameters
------------------------------

 * General [error handling rules][error-handling] apply.


Response
--------

Servers MUST respond with a valid XML document described by the
[index-response.xsd](index-response.xsd) schema. See the schema annotations
for further information.


[develhub]: http://developers.erasmuswithoutpaper.eu/
[statuses]: https://github.com/erasmus-without-paper/ewp-specs-management#statuses
[registry-spec]: https://github.com/erasmus-without-paper/ewp-specs-api-registry
[discovery-api]: https://github.com/erasmus-without-paper/ewp-specs-api-discovery
[echo]: https://github.com/erasmus-without-paper/ewp-specs-api-echo
[error-handling]: https://github.com/erasmus-without-paper/ewp-specs-architecture#error-handling
