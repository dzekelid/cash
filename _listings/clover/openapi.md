swagger: "2.0"
x-collection-name: Clover
x-complete: 1
info:
  title: ""
  version: 1.0.0
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/cash_events:
    get:
      summary: Get all cash events
      description: Retrieve all cash events for this merchant. Cash events can also
        be consumed by registering a Webhook callback. See https://docs.clover.com/build/webhooks/
      operationId: GetAllCashEvents
      x-api-path-slug: v3merchantsmidcash-events-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [employee, device]'
      - in: query
        name: filter
        description: 'Filter fields: [employee'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Cash
      - Events
  /v3/merchants/{mId}/employees/{empId}/cash_events:
    get:
      summary: Get all cash events for an employee
      description: Retrieve cash events filtered by employee ID. Cash events can also
        be consumed by registering a Webhook callback. See https://docs.clover.com/build/webhooks/
      operationId: GetEmployeeCashEvents
      x-api-path-slug: v3merchantsmidemployeesempidcash-events-get
      parameters:
      - in: path
        name: empId
        description: Employee Id
      - in: query
        name: expand
        description: 'Expandable fields: [employee, device]'
      - in: query
        name: filter
        description: 'Filter fields: [employee'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Employees
      - EmpId
      - Cash
      - Events
  /v3/merchants/{mId}/devices/{deviceId}/cash_events:
    get:
      summary: Get all cash events for a device
      description: Retrieve cash events filtered by device ID. Cash events can also
        be consumed by registering a Webhook callback. See https://docs.clover.com/build/webhooks/
      operationId: GetDeviceCashEvents
      x-api-path-slug: v3merchantsmiddevicesdeviceidcash-events-get
      parameters:
      - in: path
        name: deviceId
        description: Device Id
      - in: query
        name: expand
        description: 'Expandable fields: [employee, device]'
      - in: query
        name: filter
        description: 'Filter fields: [employee'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Devices
      - DeviceId
      - Cash
      - Events