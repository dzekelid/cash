---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Transfer funds between bank accounts (also Deposit Cash/Cheques from
    Cash Held)
  version: 1.0.0
  description: Transfer funds between bank accounts (also deposit cash/cheques from
    cash held).
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/accountingsystem/agentcash:
    get:
      summary: Gets overview of the agent cash account
      description: Gets overview of the agent cash account.
      operationId: AccountingSystem_GetAgentCash
      x-api-path-slug: apiaccountingsystemagentcash-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Overview
      - Of
      - Agent
      - Cash
      - Account
  /api/posting/cash:
    get:
      summary: Get all postings in the cash account for the agent
      description: Get all postings in the cash account for the agent.
      operationId: Posting_GetCashFunds
      x-api-path-slug: apipostingcash-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Postings
      - In
      - Cash
      - Accountthe
      - Agent
  /api/transfer/interaccount:
    post:
      summary: Transfer funds between bank accounts (also Deposit Cash/Cheques from
        Cash Held)
      description: Transfer funds between bank accounts (also deposit cash/cheques
        from cash held).
      operationId: Transfer_ProcessIatByiatDataContract
      x-api-path-slug: apitransferinteraccount-post
      parameters:
      - in: body
        name: iatDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Transfer
      - Funds
      - Between
      - Bank
      - Accounts
      - (also
      - Deposit
      - Cash
      - Cheques
      - From
      - Cash
      - Held)
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