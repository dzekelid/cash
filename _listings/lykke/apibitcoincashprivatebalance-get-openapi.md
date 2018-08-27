---
swagger: "2.0"
x-collection-name: Lykke
x-complete: 0
info:
  title: Lykke Get API Bitcoincash Private Balance
  version: 1.0.0
  description: Get api bitcoincash private balance.
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
  /api/BitcoinCash/multisig/balance:
    get:
      summary: Get API Bitcoincash Multisig Balance
      description: Get api bitcoincash multisig balance.
      operationId: ApiBitcoinCashMultisigBalanceGet
      x-api-path-slug: apibitcoincashmultisigbalance-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Multisig
      - Balance
  /api/BitcoinCash/multisig/transaction:
    get:
      summary: Get API Bitcoincash Multisig Transaction
      description: Get api bitcoincash multisig transaction.
      operationId: ApiBitcoinCashMultisigTransactionGet
      x-api-path-slug: apibitcoincashmultisigtransaction-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: query
        name: destinationAddress
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Multisig
      - Transaction
  /api/BitcoinCash/private/balance:
    get:
      summary: Get API Bitcoincash Private Balance
      description: Get api bitcoincash private balance.
      operationId: ApiBitcoinCashPrivateBalanceGet
      x-api-path-slug: apibitcoincashprivatebalance-get
      parameters:
      - in: query
        name: address
      - in: header
        name: Authorization
        description: access token
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Private
      - Balance
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