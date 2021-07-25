
# SCIM WG Re-charter Proposal - First Draft
This Charter is work in progress. To submit feedback,
please use the [scim mailing list](https://www.ietf.org/mailman/listinfo/scim).

-   This Charter: 
    -   [Collaborative version (hackmd)](https://hackmd.io/gj0Du6xHRBq5wAwqFMueFg)
    -   [Reviewed Drafts (versions pushed periodically from hackmd)](https://github.com/SCIM-Interest-Group/wiki/blob/main/WGcharter-firstdraft.md)
-   Previous Charters
    -   [Original SCIM 2.0 Charter, June 2012](https://datatracker.ietf.org/doc/charter-ietf-scim/)
-   Start Date: Unknown
---
# Charter 

The System for Cross-domain Identity Management (SCIM) specification
is an HTTP-based protocol that makes managing identities in multi-domain scenarios easier. SCIM was last published in 2015 and has seen growing adoption.

One goal for this working group is to shepherd SCIM, currently RFC series [7642](https://datatracker.ietf.org/doc/html/rfc7642), [7643](https://datatracker.ietf.org/doc/html/rfc7643), [7644](https://datatracker.ietf.org/doc/html/rfc7644), through the Internet Standard process. The group will deliver revised specifications for the SCIM requirements as Informational, and for the SCIM protocol and base schema suitable for consideration as a Standard. This work will be based upon the existing RFCs, errata and interoperabilty feedback, and incorporate current security and privacy best practices.

In addition to revising the requirements, protocol and base schema RFCs, the group will also consider additional specifications as extensions to SCIM that have found broad adoption and are ready for standards track.  This includes profiles and schemas for interoperability in additional scenarios.  The working group will develop additional Proposed Standard RFCs based on outcomes of the following work:

* Handling returning large result sets through paging, based on [draft-hunt-scim-mv-paging-00](https://tools.ietf.org/id/draft-hunt-scim-mv-paging-00.html)	and [draft-peterson-scim-cursor-pagination-00](https://tools.ietf.org/html/draft-peterson-scim-cursor-pagination-00)
* Profiling SCIM for common implementations patterns, based on [https://datatracker.ietf.org/doc/html/draft-wahl-scim-profile-00](https://datatracker.ietf.org/doc/html/draft-wahl-scim-profile-00) 
* Profiling SCIM relationships with other identity-centric protocols such as OAuth 2.0, OpenID Connect, Shared Signals, and Fastfed
* Support for synchronization-related goals between domains
* Evolution of the externalid usage
* Handling Deletes in SCIM Servers that don't allow Deletes (Soft Deletes) - based on [draft-ansari-scim-soft-delete-00](https://tools.ietf.org/html/draft-ansari-scim-soft-delete-00)
* Proposals for new Schema definitions
    * Schema for exchanging HR information
    * Schema for exchanging Enterprise group information
    * Schema for Privileged Access Management, based on [draft-grizzle-scim-pam-ext-01](https://tools.ietf.org/html/draft-grizzle-scim-pam-ext-01)



