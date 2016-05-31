---

title: "Create tenant"
weight: 40

menu:
  main:
    name: "Create"
    identifier: "rest-api-tenant-post-create"
    parent: "rest-api-tenant"
    pre: "POST `/tenant/create`"

---


Create a new tenant.


# Method

POST `/tenant/create`


# Parameters

This method takes no parameters.


## Request Body

A JSON object with the following properties:

<table class="table table-striped">
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>id</td>
    <td>String</td>
    <td>The id of the tenant.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>String</td>
    <td>The name of the tenant.</td>
  </tr>
</table>


# Result

This method returns no content.

# Response Codes

<table class="table table-striped">
  <tr>
    <th>Code</th>
    <th>Media type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>204</td>
    <td></td>
    <td>Request successful.</td>
  </tr>
  <tr>
    <td>403</td>
    <td>application/json</td>
    <td>Identity service is read-only.</td>
  </tr>
  <tr>
    <td>500</td>
    <td>application/json</td>
    <td>The tenant could not be created due to an internal server error. See the <a href="{{< relref "reference/rest/overview/index.md#error-handling" >}}">Introduction</a> for the error response format.</td>
  </tr>
</table>


# Example

## Request

POST `/tenant/create`

Request Body:

    {
      "id":"tenantOne",
      "name":"Tenant One"
    }

## Response

Status 204. No content.