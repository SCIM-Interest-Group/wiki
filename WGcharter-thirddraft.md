# SCIM WG Re-charter Proposal - Third Draft

The System for Cross-domain Identity Management (SCIM) specifications provide an HTTP-based protocol (RFC7643) and schema (RFC76744) that makes managing identities in multi-domain scenarios easier.  Since its publication in 2015, SCIM has seen growing adoption.

The first goal of this working group is to incorporate implementation experience; errata and interoperability feedback; and current security and best practices into a revised version of RFC7643 (protocol) and RFC7644 (base schema) suitability for consideration as the Internet Standard level of maturity.

Additionally, implementation experience with SCIM has surfaced new use cases and requirements.  The WG will document them in a revision of RFC7642. The WG will also consider publishing extensions to SCIM that have found broad adoption. These extensions may include profiles and schemas for interoperability in additional use cases.

* Revision of the informational RFC 7642 will:
    * Focus on Use cases and implementation patterns
        * Pull vs. Push based use cases
        * Events and signals use cases
        * Deletion use cases
    * New use cases may be added to the revised RFC
* Revision of RFC 7643/44 will include:
    * Profiling SCIM relationships with other identity-centric protocols such as OAuth 2.0, OpenID Connect, Shared Signals, and Fastfed
    * Updates to the evolution of the externalid usage
        * Updates to account state for capturing context of the state or change in state of the users account

* Multi-Value Query Filtering and Paging - based on [draft-hunt-scim-mv-paging-00]
* Define a method for co-ordinating resources between domains:
    * Incremental approach to synchronization
    * Consider building off of RFC8417 and draft-hunt-idevent-scim
* Support for deletion-related goals including:
    * Handling Deletes in SCIM Servers that don’t allow Deletes (Soft Deletes) - based on [draft-ansari-scim-soft-delete-00]
* Support for advanced automation scenarios such as:
    * Discovery and negotiation of client credentials
    * Attribute mapping
    * Per-attribute schema negotiation
* Enhance the existing schema to support exchanging of HR, Enterprise group and privileged access management (using draft-grizzle-scim-pam as a base)

# Milestones
**2021-Dec**: Working group adoption of I-Ds for Soft Delete 

**2021-Dec**: Working group adoption of I-Ds for Multi-valued paging 

**2022-Mar**: Working group adoption of I-Ds (either new or existing) for privileged access mgmt

**2022-Jun**: (Informational) Revision of RFC7642 to WGLC

**2022-Jun**: Working Group adoption of I-Ds for coordination/synchronization between domains

**2023-Dec**: Individual drafts for coordination/synchronization between domains 

**2023-Jun**: Revision of RFC7643/44 to WGLC
