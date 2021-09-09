# SCIM WG Re-charter Proposal - Second Draft
This Charter is work in progress. To submit feedback,
please use the [scim mailing list](https://www.ietf.org/mailman/listinfo/scim).

-   This Charter: 
    -   [Collaborative version (hackmd)](https://hackmd.io/fbDRsy8HThOXoMNjxu3-Og)
    -   [First draft (hackmd)](https://hackmd.io/gj0Du6xHRBq5wAwqFMueFg)
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



* Revision of the informational RFC 7642 will:
    * Focus on Use cases and implementation patterns
        * Pull vs. Push based use cases 
        * Events and signals use cases
        * Deletion use cases
    * New use cases may be added to the revised RFC
    
* Revision of RFC 7643/44 will include:
    * Profiling SCIM relationships with other identity-centric protocols such as OAuth 2.0, OpenID Connect, Shared Signals, and Fastfed
    * Updates to the evolution of the externalid usage
    
* Document SCIM support for synchronization-related goals between domains focused on:
  * Handling returning large result sets through paging, based on [draft-hunt-scim-mv-paging-00]
  * Incremental approaches to synchronization
   
 * Support for deletion-related goals including:
     * Handling Deletes in SCIM Servers that don't allow Deletes (Soft Deletes) - based on [draft-ansari-scim-soft-delete-00]
     
* Support for advanced automation scenarios such as:
    * Discovery and negotiation of client credentials
    * Attribute mapping
    * Per-attribute schema negotiation


* Enhance the existing schema to support exchanging of HR, Enterprise group  and privileged access management (using [draft-grizzle-scim-pam](https://tools.ietf.org/id/draft-grizzle-scim-pam-ext-00.html) as a base)

