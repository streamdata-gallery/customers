---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Create a customer
  description: Create a customer
  termsOfService: https://www.rebilly.com/terms/
  contact:
    name: Rebilly API Support
    url: https://www.rebilly.com/contact/
    email: integrations@rebilly.com
  version: "2.1"
host: api.rebilly.com
basePath: /v2.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /customers:
    get:
      summary: Retrieve a list of customers
      description: Retrieve a list of customers
      operationId: customers.get
      x-api-path-slug: customers-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
      - in: query
        name: No Name
      - in: query
        name: sort
        description: The collection items sort field and order (prefix with - for
          descending sort)
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Customers
    post:
      summary: Create a customer
      description: Create a customer
      operationId: customers.post
      x-api-path-slug: customers-post
      parameters:
      - in: body
        name: body
        description: Customer resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customer
  /customers/{id}/lead-source:
    get:
      summary: Retrieve a customer's Lead Source
      description: Retrieve a Lead Source of given customer
      operationId: customers.id.lead_source.get
      x-api-path-slug: customersidleadsource-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Customers
      - Lead
      - Source
    delete:
      summary: Delete a Lead Source for a customer
      description: Delete a Lead Source that belongs to a certain customer
      operationId: customers.id.lead_source.delete
      x-api-path-slug: customersidleadsource-delete
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcea
      - Customer
    put:
      summary: Create a Lead Source for a customer
      description: Create a Lead Source for a customer
      operationId: customers.id.lead_source.put
      x-api-path-slug: customersidleadsource-put
      parameters:
      - in: body
        name: body
        description: Lead Source resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcea
      - Customer
  /customers/{id}:
    get:
      summary: Retrieve a customer
      description: Retrieve a customer with specified identifier string
      operationId: customers.id.get
      x-api-path-slug: customersid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Customer
    put:
      summary: Create a customer with predefined ID
      description: Create a customer with predefined identifier string
      operationId: customers.id.put
      x-api-path-slug: customersid-put
      parameters:
      - in: body
        name: body
        description: Customer resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customer
      - Predefined
      - ID
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---