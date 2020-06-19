[title]: # (SCIM Connector APIs)
[tags]: # (api)
[priority]: # (110)
# SCIM Connector APIs

This section reviews the APIs that are used by the SCIM Connector application.

## Thycotic SCIM Connector API Commands

``` 
Application Users (GET)

Create Application User (POST)

(PATCH)

Delete Application User (DELETE)

SCIM Integrated Endpoints (GET)

SCIM Integrated Endpoint (use id) (GET)

Modify integrated Endpoint (PUT)

Create SCIM Integrated Endpoints (POST)

Delete SCIM Integrated Endpoints (Delete)

Settings (GET)

Update Settings (POST)

Non-Expiring Tokens (POST)

Non-Expiring Tokens (DELETE)

Logs (GET)

Ping (GET)
```

## Supported SCIM API Endpoints

``` 

Users (GET) <Base URL>/v2/users

User by ID (GET) <Base URL>/v2/users/<user id>

Create User (POST) <Base URL>/v2/users

Update User by ID (PUT) <Base URL>/v2/users/<user id>

Delete User by ID (DELETE) <Base URL>/v2/users/<user id>

Groups (GET) <Base URL>/v2/groups

Group by ID (GET) <Base URL>/v2/groups/<group id>

Create Group (POST) <Base URL>/v2/groups

Delete Group (DELETE) <Base URL>/v2/groups/<group id>

Service provider configuration (GET)

Schemas (GET)

Resource Types (GET)

Containers (GET)

Container Permissions (GET)

Privilege Data (GET)

Privilege Data Permissions (GET)
```

## Supported Filters

* __eq (equal):__ The attribute and operator values must be identical for a match.

* __ne (not equal):__ The attribute and operator values are not identical.

* __co (contains):__ The entire operator value must be a substring of the attribute value for a match.

* __sw (starts with):__ The entire operator value must be a substring of the attribute value, starting at the beginning of the attribute value. This criterion is satisfied if the two strings are identical.

* __ew (ends with):__ The entire operator value must be a substring of the attribute value, matching at the end of the attribute value. This criterion is satisfied if the two strings are identical.

* __pr (present):__ If the attribute has a non-empty or (has value) non-null value, or if it contains a non-empty node for complex attributes, there is a match.

* __gt (greater than):__ If the attribute value is greater than the operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison, and for DateTime types, it is a chronological comparison. For integer attributes, it is a comparison by numeric value. Boolean and binary attributes will cause a failed response (HTTP status code 400) with scimType of invalidFilter.

* __ge (greater than or equal to):__ If the attribute value is greater than to the operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison, and for DateTime types, it is a chronological comparison. For integer attributes, it is a comparison by numeric value. Boolean and binary attributes will cause a failed response (HTTP status code 400) with
scimType of invalidFilter.

* __lt (less than):__ If the attribute value is less than the operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison, and for DateTime types, it is a chronological comparison. For integer attributes, it is a comparison by numeric value. Boolean and binary attributes SHALL cause a failed response (HTTP status code 400) with “scimType” of “invalidFilter”.

* __le (less than or equal to):__ If the attribute value is less than or equal to the operator value, there is a match. The actual comparison is dependent on the attribute type. For string attribute types, this is a lexicographical comparison, and for DateTime types, it is a chronological comparison. For integer attributes, it is a comparison by numeric value. Boolean and binary attributes will cause a failed response (HTTP status scimType of invalidFilter.

* __and (Logical “and”):__ The filter is only a match if both expressions evaluate to true.

* __or (Logical “or”):__ The filter is a match if either expression evaluates to true.

* __Not (“Not” function):__ The filter is a match if the expression evaluates to false.

* __( ) (Precedence grouping):__ Boolean expressions grouped using parentheses to change the standard order of operations, that is, to evaluate logical “or” operators before logical “and” operators.

* __[ ] (Complex attribute filter grouping):__ Complex filters where
expressions must be applied to the same value of a parent attribute
specified immediately before the left square bracket [. The expression
within square brackets [ and ] must be a valid filter expression based
upon sub-attributes of the parent attribute. Nested expressions may be used.

## Filtering Examples

* Get the first 50 groups:

   `<Base URL>/v2/groups?StartIndex=1&Count=50`

* Get users where their email contains `“Thycotic.com”:`

   `<Base URL>/v2/users?filter=emails.value co "thycotic.com"`

* Include only specific attributes in the return (Return only user id attribute):

   `<Base URL>/v2/Users?attributes[0]=id`

* Exclude specific values from the return (Return all attributes except user name):

   `<Base URL>/v2/Users?excludedAttributes[0]=userName`