# Orders

## Get order details

> GET /orders/{orderId}

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/orders/{orderId}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response for Status code: 200

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "orderId": 0,
    "salesOrderId": 0,
    "salesOrderNo": "string",
    "invoiceId": 0,
    "invoiceNo": "string",
    "source": "APP",
    "total": 0,
    "subtotal": 0,
    "installment": 0,
    "installmentInfo": [
      {
        "stepNumber": 0,
        "price": 0,
        "dueDate": "2022-07-21T06:43:17.067Z",
        "status": "string"
      }
    ],
    "fees": [
      {
        "type": "PROCESSING",
        "value": 0
      }
    ],
    "paymentMethod": "string",
    "userComment": "string",
    "status": "string",
    "time": 0,
    "userEmail": "string",
    "userPhone": "string",
    "userZoneState": "string",
    "userZone": "string",
    "userAddress": "string",
    "salesAgentCode": "string",
    "currency": "string",
    "items": [
      {
        "offerId": 0,
        "sku": "string",
        "amount": 0,
        "price": 0,
        "name": "string",
        "images": [
          "string"
        ],
        "currency": "string",
        "serviceName": "string",
        "serviceUUID": "string",
        "account": "string",
        "serviceStatus": "string"
      }
    ],
    "cardNumber": "string",
    "cardPin": "string",
    "tenure": 0,
    "appPlatform": "string",
    "appVersion": "string"
  }
}

```

> Response for Status code: 401

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "orderId": 0,
    "salesOrderId": 0,
    "salesOrderNo": "string",
    "invoiceId": 0,
    "invoiceNo": "string",
    "source": "APP",
    "total": 0,
    "subtotal": 0,
    "installment": 0,
    "installmentInfo": [
      {
        "stepNumber": 0,
        "price": 0,
        "dueDate": "2022-07-21T06:43:17.092Z",
        "status": "string"
      }
    ],
    "fees": [
      {
        "type": "PROCESSING",
        "value": 0
      }
    ],
    "paymentMethod": "string",
    "userComment": "string",
    "status": "string",
    "time": 0,
    "userEmail": "string",
    "userPhone": "string",
    "userZoneState": "string",
    "userZone": "string",
    "userAddress": "string",
    "salesAgentCode": "string",
    "currency": "string",
    "items": [
      {
        "offerId": 0,
        "sku": "string",
        "amount": 0,
        "price": 0,
        "name": "string",
        "images": [
          "string"
        ],
        "currency": "string",
        "serviceName": "string",
        "serviceUUID": "string",
        "account": "string",
        "serviceStatus": "string"
      }
    ],
    "cardNumber": "string",
    "cardPin": "string",
    "tenure": 0,
    "appPlatform": "string",
    "appVersion": "string"
  }
}

```

> Response for Status code: 200

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "orderId": 0,
    "salesOrderId": 0,
    "salesOrderNo": "string",
    "invoiceId": 0,
    "invoiceNo": "string",
    "source": "APP",
    "total": 0,
    "subtotal": 0,
    "installment": 0,
    "installmentInfo": [
      {
        "stepNumber": 0,
        "price": 0,
        "dueDate": "2022-07-21T06:43:17.111Z",
        "status": "string"
      }
    ],
    "fees": [
      {
        "type": "PROCESSING",
        "value": 0
      }
    ],
    "paymentMethod": "string",
    "userComment": "string",
    "status": "string",
    "time": 0,
    "userEmail": "string",
    "userPhone": "string",
    "userZoneState": "string",
    "userZone": "string",
    "userAddress": "string",
    "salesAgentCode": "string",
    "currency": "string",
    "items": [
      {
        "offerId": 0,
        "sku": "string",
        "amount": 0,
        "price": 0,
        "name": "string",
        "images": [
          "string"
        ],
        "currency": "string",
        "serviceName": "string",
        "serviceUUID": "string",
        "account": "string",
        "serviceStatus": "string"
      }
    ],
    "cardNumber": "string",
    "cardPin": "string",
    "tenure": 0,
    "appPlatform": "string",
    "appVersion": "string"
  }
}

```



Retrieves details of the offer order associated with the given id

### Parameters

Name | Description
--------- | ------- 
orderId (integer($int64)) | order id

### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="warning">
Status Code 401 : User has not yet been authenticated
</aside>

<aside class="warning">
Status Code 404 : Order with specified id was not found
</aside>





## Update order details

> PATCH /orders/{orderId}

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.patch("/orders/{orderId}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> The above command requires a JSON structured like this:

```json


{
  "salesAgentCode": "string",
  "status": "string"
}

```

> Response

```json
{
  "success": true,
  "code": 0,
  "message": "string",
  "body": "string"
}

```

Updates the details of the offer order associated with the 

### Parameters

Name | Description
--------- | ------- 
orderId (integer($int64)) | order id

### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="warning">
Status Code 401: User has not yet been authenticated
</aside>

<aside class="warning">
Status Code 404: Order with specified id was not found
</aside>





## Find all orders

> GET /orders

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/orders").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "total": 0,
    "items": [
      {
        "orderId": 0,
        "salesOrderId": 0,
        "salesOrderNo": "string",
        "invoiceId": 0,
        "invoiceNo": "string",
        "source": "APP",
        "total": 0,
        "status": "string",
        "time": 0,
        "userZoneState": "string",
        "userZone": "string",
        "userAddress": "string",
        "userPhone": "string",
        "salesAgentCode": "string",
        "paymentMethod": "string",
        "currency": "string",
        "appPlatform": "string",
        "appVersion": "string"
      }
    ]
  }
}

```

Retrieves all offer orders

### Parameters

Name | Description
--------- | ------- 
page (integer($int32)) | the page number to start with (Default value: 1)
per-page (integer($int32)) | number of items to return per page (Default value: 30)
filter-by (array(string))| Field to filter by attribute.   Format (filter-by = attributeId: option1; option2 )  Example (filter-by=STATUS:CREATED;APPROVED)  List of supported filters (ORDER_NO, INVOICE_NO, STATUS, LOCATION, SALES_AGENT, MOBILE_NUMBER)   Default value : List []
sort-by | field to sort by.  Available values  (DATE_LOW_TO_HIGH, DATE_HIGH_TO_LOW)  Default value  (DATE_HIGH_TO_LOW)

### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="warning">
Status Code 401 : User has not yet been authenticated
</aside>




## Get offer order user

> GET /orders/{orderId}/user

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/orders/{orderId}/user").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "id": 0,
    "contactPhone": "string",
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "emiratesProfile": {
      "name": "string",
      "sex": "string",
      "dateOfBirth": 0,
      "nationality": "string",
      "emiratesId": "string",
      "expiryDate": 0
    }
  }
}

```

Retrieve the offer order user

### Parameters

Name | Description
--------- | ------- 
orderId (integer($int64)) | order id

### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="warning">
Status Code 401: User has not yet been authenticated
</aside>

<aside class="warning">
Status Code 404: Order with specified id was not found
</aside>



## Get offer order payments

> GET /orders/{orderId}/payments

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/orders/{orderId/payments}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": [
    {
      "id": "string",
      "invoiceNumber": "string",
      "paymentMode": "string",
      "stamp": 0,
      "paidAmount": 0,
      "transactionId": "string",
      "paymentNumber": "string",
      "currency": "string"
    }
  ]
}

```

Retrieves the offer order payments

### Parameters

Name | Description
--------- | ------- 
orderId (integer($int64)) | order id

### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="warning">
Status Code 401 : User has not yet been authenticated
</aside>

<aside class="warning">
Status Code 404 : Order wit specified id was not found
</aside>






## Get offer order invoice

> GET /orders/{orderId}/invoice

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/orders/{orderId}/invoice").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "invoiceId": 0,
    "invoiceNumber": "string",
    "date": "string",
    "status": "string",
    "customerName": "string",
    "customerPhone": "string",
    "price": 0,
    "balance": 0,
    "installment": 0,
    "currency": "string"
  }
}

```

Retrieves the offer orde invoice

### Parameters

Name | Description
--------- | ------- 
orderId (integer($int64)) | order id

### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="warning">
Status Code 401: User has not yet been authenticated
</aside>

<aside class="warning">
Status Code 404: Order with specified id was not found
</aside>





## Get offer order history

> GET /orders/{orderId}/history

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/orders/{orderId}/history").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response: 

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": [
    {
      "id": 0,
      "orderId": 0,
      "stamp": 0,
      "status": "string",
      "comment": "string"
    }
  ]
}

```

Retrieves the history of the offer order associated with the given id

### Parameters

Name | Description
--------- | ------- 
orderId (integer($int64)) | order id
### Response

<aside class="success">
Status Code 200 : OK
</aside>

<aside class="success">
Status Code 401 : User has not yet been authenticated
</aside>

<aside class="success">
Status Code 404 : Order with specified id was not found
</aside>