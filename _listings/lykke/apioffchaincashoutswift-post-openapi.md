---
swagger: "2.0"
x-collection-name: Lykke
x-complete: 0
info:
  title: Lykke Add API Offchain Cashout Swift
  version: 1.0.0
  description: Add api offchain cashout swift.
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
  /api/BitcoinCash/private/transaction:
    get:
      summary: Get API Bitcoincash Private Transaction
      description: Get api bitcoincash private transaction.
      operationId: ApiBitcoinCashPrivateTransactionGet
      x-api-path-slug: apibitcoincashprivatetransaction-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: query
        name: destinationAddress
      - in: query
        name: fee
      - in: query
        name: sourceAddress
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Private
      - Transaction
  /api/CashOut:
    post:
      summary: Add API Cashout
      description: Add api cashout.
      operationId: ApiCashOutPost
      x-api-path-slug: apicashout-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Cashout
  /api/CashOutSwiftRequest:
    post:
      summary: Add API Cashout Swift Request
      description: Add api cashout swift request.
      operationId: ApiCashOutSwiftRequestPost
      x-api-path-slug: apicashoutswiftrequest-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Cashout
      - Swift
      - Request
  /api/Ethereum/cashout:
    post:
      summary: Add API Ethereum Cashout
      description: Add api ethereum cashout.
      operationId: ApiEthereumCashoutPost
      x-api-path-slug: apiethereumcashout-post
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
      - Ethereum
      - Cashout
  /api/HotWallet/cashout:
    post:
      summary: Add API Hotwallet Cashout
      description: Add api hotwallet cashout.
      operationId: Cashout
      x-api-path-slug: apihotwalletcashout-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: model
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: SignatureVerificationToken
        description: signature verification token
      responses:
        200:
          description: OK
      tags:
      - Hotwallet
      - Cashout
  /api/MarginTrading/cashOutSwift:
    post:
      summary: Add API Margintrading Cashoutswift
      description: Add api margintrading cashoutswift.
      operationId: ApiMarginTradingCashOutSwiftPost
      x-api-path-slug: apimargintradingcashoutswift-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Margintrading
      - Cashoutswift
  /api/MyLykkeCashInEmail:
    post:
      summary: Add API Mylykkecashinemail
      description: Add api mylykkecashinemail.
      operationId: ApiMyLykkeCashInEmailPost
      x-api-path-slug: apimylykkecashinemail-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: reqModel
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Mylykkecashinemail
  /api/offchain/cashout:
    post:
      summary: Add API Offchain Cashout
      description: Add api offchain cashout.
      operationId: ApiOffchainCashoutPost
      x-api-path-slug: apioffchaincashout-post
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
      - Offchain
      - Cashout
  /api/offchain/cashout/forward:
    post:
      summary: Add API Offchain Cashout Forward
      description: Add api offchain cashout forward.
      operationId: ApiOffchainCashoutForwardPost
      x-api-path-slug: apioffchaincashoutforward-post
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
      - Offchain
      - Cashout
      - Forward
  /api/offchain/cashout/swift:
    get:
      summary: Get API Offchain Cashout Swift
      description: Get api offchain cashout swift.
      operationId: ApiOffchainCashoutSwiftGet
      x-api-path-slug: apioffchaincashoutswift-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      responses:
        200:
          description: OK
      tags:
      - Offchain
      - Cashout
      - Swift
    post:
      summary: Add API Offchain Cashout Swift
      description: Add api offchain cashout swift.
      operationId: ApiOffchainCashoutSwiftPost
      x-api-path-slug: apioffchaincashoutswift-post
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
      - Offchain
      - Cashout
      - Swift
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