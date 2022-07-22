# Notifications


## Send notification to phones

> POST /notification/phones

```dart

```

```shell
POST  https://api-qa2.b2connect.me/management/name=
-H Authorization Bearer {{token}}
-D file="String($binary)"
```

```javascript
const axios = require("axios");

axios.post("/notification/phones").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```
> The above command requires a JSON structured like this:

```json

{
  "notificationBody": {
    "name": "string",
    "channels": [
      "IN_APP"
    ],
    "message": "string",
    "title": "string",
    "level": "DONE"
  },
  "phones": [
    "string"
  ]
}

```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "message": "string"
  }
}

```

Sends notification to the specified list of phones

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : Notifications added to queue
</aside>

<aside class="warning">
Status Code 400 : Message or recipient field is empty
</aside>

<aside class="warning">
Status Code 404 : No user matches given parameters
</aside>


## Send notification to groups
> POST /notification/groups


```dart

```

```shell
POST  https://api-qa2.b2connect.me/management/name=
-H Authorization Bearer {{token}}
-D file="String($binary)"
```

```javascript
const axios = require("axios");


axios.post("/notification/groups").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```
> The above command requires a JSON structured like this:

```json

{
  "notificationBody": {
    "name": "string",
    "channels": [
      "IN_APP"
    ],
    "message": "string",
    "title": "string",
    "level": "DONE"
  },
  "groups": [
    0
  ]
}

```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "message": "string"
  }
}

```


Sends notification to the specified list of groups

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : Notifications added to queue
</aside>

<aside class="warning">
Status Code 400 : Message or recipient field is empty
</aside>

<aside class="warning">
Status Code 404 : No user matches given parameters
</aside>


## Send notifications by filter
> POST /notification/filter


```dart

```

```shell
POST  https://api-qa2.b2connect.me/management/name=
-H Authorization Bearer {{token}}
-D file="String($binary)"
```

```javascript
const axios = require("axios");


axios.post("/notification/filter").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```
> The above command requires a JSON structured like this:

```json

{
  "notificationBody": {
    "name": "string",
    "channels": [
      "IN_APP"
    ],
    "message": "string",
    "title": "string",
    "level": "DONE"
  },
  "userFilter": {
    "userFilterItems": [
      {
        "text": "string",
        "filterField": "PROPERTY",
        "filterType": "EQUALS"
      }
    ]
  }
}

```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "message": "string"
  }
}

```

Sends notification to the specified list made by using the filter

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : Notifications added to queue
</aside>

<aside class="warning">
Status Code 400 : Message or recipient field is empty
</aside>

<aside class="warning">
Status Code 404 : No user matches given parameters
</aside>



## Resend notification for events

> POST /notification/resend/{eventId}


```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.post("/notification/resend/{eventId}").then((res) => {
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
    "message": "string"
  }
}

```

Resends the notification dedicated for specific events

### Parameters

Name | Description
--------- | ------- 
eventId ($int64) | user phone number

### Response

<aside class="success">
Status Code 200 : Notifications added to queue
</aside>

<aside class="warning">
Status Code 400 : Message or recipient field is empty
</aside>

<aside class="warning">
Status Code 403 : Was resent for this group.
</aside>


<aside class="warning">
Status Code 404 : No user matches given parameters
</aside>




## Notification stats

> GET /notification/stats


```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.get("/notification/stats").then((res) => {
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
    "totalSMS": 0,
    "totalSuccessSMS": 0,
    "totalFailureSMS": 0,
    "totalPush": 0,
    "totalSuccessPush": 0,
    "totalFailurePush": 0,
    "totalAnnouncement": 0,
    "totalActiveAnnouncement": 0,
    "totalInactiveAnnouncement": 0,
    "totalSurvey": 0,
    "totalActiveSurvey": 0,
    "totalInactiveSurvey": 0,
    "recentNotifications": [
      {
        "id": 0,
        "name": "string",
        "totalCount": 0,
        "channels": [
          "IN_APP"
        ],
        "successCount": 0,
        "failedCount": 0,
        "date": "string",
        "owner": "string",
        "parentId": 0,
        "childIds": [
          0
        ]
      }
    ]
  }
}

```

Gives all the statistics for the notification

### Parameters

Name | Description
--------- | ------- 
eventId ($int64) | user phone number

### Response

<aside class="success">
Status Code 200 : OK
</aside>




## Notification Menu Access

> GET /notification/menu


```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.get("/notification/menu").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response for Status Code 200:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "message": "string"
  }
}
```

> Response for Status Code 404:

```json

{
  "dashboard": true,
  "notifications": true,
  "surveys": true,
  "announcements": true,
  "reports": true,
  "productSales": true,
  "support": true
}
```

Gives access to the menu for users


### Response


<aside class="success">
Status Code 200 : Menu access found
</aside>

<aside class="warning">
Status Code 404 : No user matches given parameters
</aside>



## Notification History

> GET /notification/history


```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.get("/notification/history").then((res) => {
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
    "total": 0,
    "notifications": [
      {
        "id": 0,
        "name": "string",
        "totalCount": 0,
        "channels": [
          "IN_APP"
        ],
        "successCount": 0,
        "failedCount": 0,
        "date": "string",
        "owner": "string",
        "parentId": 0,
        "childIds": [
          0
        ]
      }
    ]
  }
}

```


(Not sure) Retrieves the notification history

### Parameters

Name | Description
--------- | ------- 
page (integer ($int32)) | Page number to start with (Default value: 1)
per_page (integer ($int32)) | Number of records to return in one request (Default value: 25)

### Response

<aside class="success">
Status Code 200 : Menu access found
</aside>

<aside class="warning">
Status Code 404 : No user matches given parameters
</aside>

