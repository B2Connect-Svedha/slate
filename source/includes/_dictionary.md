# Dictionary

## All Order Status

> GET /dictionaries/order-statuses

```dart 

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/dictionaries/order-statuses").then((res) => {
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
    "message": "",
    "body": {
        "statuses": [
            "initiated",
            "created",
            "approved",
            "rejected",
            "pending payment",
            "ready for delivery",
            "delivered",
            "delivered (await next payment)",
            "completed",
            "cancelled (refund claimed)"
        ]
    }
}

```

Retrieves all the order statuses

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>

## All locations

> GET /dictionaries/locations

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/dictionaries/locations").then((res) => {
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
    "message": "",
    "body": {
        "locations": [
            "ADMG",
            "ALDAR",
            "Progressive_WiFi"
        ]
    }
}

```

Retrieves all the locations

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>


## Retrieve all job roles

> GET /dictionaries/job-roles

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/dictionaries/job-roles").then((res) => {
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
    "message": "",
    "body": [
        "ACCOUNTANTS PAYABLE",
        "Accounts Payable Supervisor",
        "W/O Agent"
    ]
}

```

Retrieves all the job roles

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>


## Retrieve all departments

> GET /dictionaries/departments

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/dictionaries/departments").then((res) => {
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
    "message": "",
    "body": [
        "Accommodation in charge",
        "ACCOUNTS",
        "Style",
        "Welcome Office"
    ]
}

```

Retrieves all the departments

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>



## Retrieve chart count

> GET /dictionaries/chart-count

```dart

```

```shell

```

```javascript

const axios = require("axios");

axios.get("/dictionaries/chart-count").then((res) => {
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
    "message": "",
    "body": {
        "department": [
            {
                "fieldName": "F & B Service",
                "fieldCount": 130
            },
            {
                "fieldName": "Housekeeping",
                "fieldCount": 120
            }
        ],
        "job_role": [
            {
                "fieldName": "Housekeeping Attendant",
                "fieldCount": 50
            },
            {
                "fieldName": "Waiter/Waitress",
                "fieldCount": 30
            }
        ],
        "nationality": [
            {
                "fieldName": "INDIA",
                "fieldCount": 12345
            {
                "fieldName": "PAKISTAN",
                "fieldCount": 10005
            }
        ]
    }
}

```

Retrieves the chart count details for departments, job roles and nationalities

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>


