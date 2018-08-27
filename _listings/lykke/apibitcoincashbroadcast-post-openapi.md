---
swagger: "2.0"
x-collection-name: Lykke
x-complete: 0
info:
  title: Lykke Add API Bitcoincash Broadcast
  version: 1.0.0
  description: Add api bitcoincash broadcast.
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/BcnTransactionByCashOperation/{id}:
    get:
      summary: Get API Bcntransactionbycashoperation
      description: Get api bcntransactionbycashoperation.
      operationId: ApiBcnTransactionByCashOperationByIdGet
      x-api-path-slug: apibcntransactionbycashoperationid-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Bcntransactionbycashoperation
  /api/BitcoinCash/broadcast:
    post:
      summary: Add API Bitcoincash Broadcast
      description: Add api bitcoincash broadcast.
      operationId: ApiBitcoinCashBroadcastPost
      x-api-path-slug: apibitcoincashbroadcast-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: model
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Broadcast
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