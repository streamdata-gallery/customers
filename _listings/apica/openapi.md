swagger: "2.0"
x-collection-name: Apica
x-complete: 1
info:
  title: Scenarios API
  version: 1.0.0
host: api.pingdom.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
basePath: /
paths:
  '/customers/{customerId} ':
    ' get ':
      summary: Customers
      description: Returns subcustomer by subcustomer's ID.
      operationId: -customers-customerid-
      x-api-path-slug: customerscustomerid-get
      responses:
        200:
          description: OK
      tags:
      - Customers
  '/customers ':
    ' post ':
      summary: Customers
      description: Creates customer.
      operationId: -customers-
      x-api-path-slug: customers-post
      responses:
        200:
          description: OK
      tags:
      - Customers
  '/customers/{customerId}/subscription ':
    ' put ':
      summary: Customers Subscription
      description: Updates customer's subscription.
      operationId: -customers-customerid-subscription-
      x-api-path-slug: customerscustomeridsubscription-put
      responses:
        200:
          description: OK
      tags:
      - Customers