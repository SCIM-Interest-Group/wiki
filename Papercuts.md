# Papercuts

This page lists items related to the spec that implementers have had difficulty with.

## Amazon Web Services list

1.	Anti-entropy is currently solved by the client periodically doing full scans over all Users and Group memberships in the service.
      a.	This is especially expensive due to lack of support for token-based pagination. Spec requires index-based pagination.
2.	No asynchronous bulk operations
      a.	Makes it slower and/or chatty to execute the initial upload of a large directory.
      b.	Identity Providers struggle to find the right balance of high throughput without accidentally saturating the endpoint, without actually knowing the limits of the endpoint.
3.	Spec contains multiple ways to implement some behaviors (e.g. deleting a user attribute) and is ambiguous in the interpretation of some operations (such as understanding when to deactivate vs. delete a user).
      a.	This led to interoperability.
      b.	Or worse, it led to data corruption. For example, some IdPs used PUT for writing users, but this had the side-effect of wiping all data on the User object. Most switched to PATCH.
      c.	FastFed defined a profile to formalize known best practices.
4.	Mutability of the externalId attribute
      a.	How should services interpret a change to the externalId?
      b.	Can services leverage the externalId to detect dangerous bugs that have security ramifications. For example, an IdP accidentally re-using the same username for multiple users (spec violation), causing the IdP to accidentally merge the attributes of multiple users into a single record when provisioning to the app. This can be detected by seeing multiple PATCH operations with the same username but different externalId.
      c.	How should services handle a tenant who switches IdPs, and hence the externalId may legitimately change.
5.	Validations beyond basic datatype validations. String length constraints, regex, numerical range constraints, enums?
6.	How to extend pre-defined core attributes? For example, adding a validation flag to the email or phone.
7.	Other ambiguities:
      a.	Unclear how to represent the value of ‘manager’ in the EnterpriseUser. This is a specific example of a general question about representing attributes that are references to other Users/Groups/Resources.
      b.	If a user can login with either their email or phone number (or both), what value should go into the username field?





## SailPoint list

1.	Should r/o attributes be included in a PUT when updating (replacing) a User record? RFC7644 3.1 says:
      > For example, in a SCIM PUT request, "readOnly" attributes are ignored, while "readWrite" attributes are updated.

      RFC 7643 4.1.2 notes that User "groups" attribute is readOnly. We have experienced implementations
      omitting the "groups" attribute on a User PUT results in the User being removed from their Groups.
      And other implementations that preserve the Groups in such a case.


2.	RFC 7643 3.1 says "id", "externalId", and "meta" attributes are common attributes, and need to returned from the endpoints,
      but may not be present in the schemas. This section can be interpreted both ways - that they must be included
      in schemas, and that the definition of these in the spec overrides whatever may be returned in schemas anyhow.
      To add insult to injury, they may be present in the schema but null, as shown in this real-world example:

```JSON
{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "id": null,
  "externalId": null,
  "meta": null
}
```


3.	Payload structure for updating complex attribute from extended Schema of any resource type is missing in the specification.

