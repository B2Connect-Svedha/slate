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
  "message": "string",
  "body": {
    "statuses": [
      "string"
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
  "message": "string",
  "body": {
    "locations": [
      "string"
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
  "message": "string",
  "body": [
    "string"
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
  "message": "string",
  "body": [
    "string"
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
  "message": "string",
  "body": {
    "department": [
      {
        "fieldName": "string",
        "fieldCount": 0
      }
    ],
    "job_role": [
      {
        "fieldName": "string",
        "fieldCount": 0
      }
    ],
    "nationality": [
      {
        "fieldName": "string",
        "fieldCount": 0
      }
    ]
  }
}

```

Retrieves the chart count

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>


