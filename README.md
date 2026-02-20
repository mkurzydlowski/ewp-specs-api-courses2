Courses API
===========

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This document describes the **Courses API**. This API is not directly related
to EWP mobility APIs, but it might help with building user-friendly mobility
client software. It allows other HEIs to access information on courses.


Learning Opportunities
----------------------

`Course` is just one of types of Learning Opportunities. This model
has been adopted from the [EMREX][emrex] and ELMO projects (you will see many
similarities to EMREX in the XSDs too).


### Specification vs instance

Learning opportunities are models with two entities: LO specifications and LO
instances.

 * LO specification (LOS) is an abstract specification of a course. A
   template of sorts. It has no students, no grades, no starting nor ending
   dates.

 * LO instance (LOI) describes a "real" instance of an LO. It is conducted in
 a specific time, it has its students, etc.

This API allows accessing both - LOSes and LOIs – but all LOIs are accessible
via LOS parents. If a LOS doesn't have a LOI child, then it means that this LOS
has not been conducted in the searched time span.


Endpoints and functionality to be implemented
---------------------------------------------

Server implementers MUST:

* Implement the [`courses` endpoint](endpoints/courses.md).
* Implement the [`instances` endpoint](endpoints/instances.md).
* Put the URLs of these endpoints in their [manifest file][discovery-api], as
  described in [manifest-entry.xsd](manifest-entry.xsd).

The details on each of these endpoints are described on separate pages of this
API specification (use the links above).


[develhub]: http://developers.erasmuswithoutpaper.eu/
[statuses]: https://github.com/erasmus-without-paper/ewp-specs-management#statuses
[discovery-api]: https://github.com/erasmus-without-paper/ewp-specs-api-discovery
[emrex]: http://emrex.eu/