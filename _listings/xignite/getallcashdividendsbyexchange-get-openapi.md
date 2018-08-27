---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Global Historical Get All Cash Dividends By Exchange
  description: Get all cash dividends for a date range in the specified exchange.
  version: 1.0.0
host: www.xignite.com
basePath: xGlobalHistorical.json/XigniteGlobalHistorical
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetAllCashDividendsByExchange:
    get:
      summary: Get All Cash Dividends By Exchange
      description: Get all cash dividends for a date range in the specified exchange.
      operationId: postGetallcashdivendsbyexchange
      x-api-path-slug: getallcashdividendsbyexchange-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Cash
      - Dividends
      - By
      - Exchange
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