# Survey

## List all Surverys

> GET /survey​/

```dart

var request = http.Request('GET', Uri.parse('http://api-qa2.b2connect.me/management/survey/?page=1&per_page=10'));


http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}

```

```shell

curl --location --request GET 'http://api-qa2.b2connect.me/management/survey/?page=1&per_page=10'

```

```javascript

const axios = require("axios");

axios.get("/survey/").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```
> Response if STATUS CODE 200:

```json

{
  "id": 0,
  "title": "string",
  "category": "string",
  "surveyLink": "string",
  "created": "2022-07-20T08:07:26.466Z",
  "expiry": "2022-07-20T08:07:26.466Z",
  "status": "ACTIVE",
  "siteId": 0
}

```

> Example Response for STATUS CODE 404:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "total": 0,
    "surveys": [
      {
        "id": 0,
        "title": "string",
        "category": "string",
        "surveyLink": "string",
        "created": "2022-07-20T08:07:26.474Z",
        "expiry": "2022-07-20T08:07:26.474Z",
        "status": "ACTIVE",
        "siteId": 0
      }
    ]
  }
}

```

Retrieves the list of all surveys

### Parameters

Name | Description
--------- | ------- 
page (integer($int32)) | Default value: 1
per_page (integer($int32)) | Default value: 10

### Response

<aside class="success">
Status Code 200 : All surverys were fetched
</aside>

<aside class="warning">
Status Code 404 : Survey was not found
</aside>



## Retreive a specific survey

> GET /survey/{id}


```dart
var request = http.Request('GET', Uri.parse('http://api-qa2.b2connect.me/management/survey/92818518'));


http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}

```

```shell

curl --location --request GET 'http://api-qa2.b2connect.me/management/survey/92818518'

```

```javascript

const axios = require("axios");

axios.get("/survey/{id}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response if STATUS CODE 200:

```json

{
  "id": 0,
  "title": "string",
  "category": "string",
  "surveyLink": "string",
  "created": "2022-07-20T08:18:20.280Z",
  "expiry": "2022-07-20T08:18:20.280Z",
  "status": "ACTIVE",
  "siteId": 0
}

```

> Example Response for STATUS CODE 404:

```json

{
  "id": 0,
  "title": "string",
  "category": "string",
  "surveyLink": "string",
  "created": "2022-07-20T08:18:20.286Z",
  "expiry": "2022-07-20T08:18:20.286Z",
  "status": "ACTIVE",
  "siteId": 0
}

```

Retrieves the survey associated with the specific ID given

### Parameters

Name | Description
--------- | ------- 
id (integer($int64)) | Id of the survey you want to retrieve

### Response

<aside class="success">
Status Code 200 : Survey was fetched
</aside>

<aside class="warning">
Status Code 404 : Survey was not found
</aside>


## Create a new survey

> POST /survey


```dart
var request = http.Request('POST', Uri.parse('http://api-qa2.b2connect.me/management/survey/'));
request.body = {
  id: 47995082,
  title: "dolor magna sunt in",
  category: "nostrud laborum",
  surveyLink: "ad dolor aute",
  created: "2008-05-09T10:29:57.776Z",
  expiry: "2018-07-30T02:11:10.287Z",
  status: "ACTIVE",
  siteId: -88931221
}

http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}


```

```shell

curl --location --request POST 'http://api-qa2.b2connect.me/management/survey/' \

```

```javascript

const axios = require("axios");

axios.post("/survey").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> The above command requests a JSON structured like this:

```json
{
  "id": 0,
  "title": "string",
  "category": "string",
  "surveyLink": "string",
  "created": "2022-07-20T08:22:42.614Z",
  "expiry": "2022-07-20T08:22:42.614Z",
  "status": "ACTIVE",
  "siteId": 0
}
```

Creates a new survey

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : Survey was created
</aside>



## Update an existing survey

> PUT /survey/{id}


```dart

var request = http.Request('PUT', Uri.parse('http://api-qa2.b2connect.me/management/survey/92818518'));
request.body = {
  id: 47995082,
  title: "dolor magna sunt in",
  category: "nostrud laborum",
  surveyLink: "ad dolor aute",
  created: "2008-05-09T10:29:57.776Z",
  expiry: "2018-07-30T02:11:10.287Z",
  status: "ACTIVE",
  siteId: -88931221
}

http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}


```

```shell

curl --location --request PUT 'http://api-qa2.b2connect.me/management/survey/92818518' \

```

```javascript

const axios = require("axios");

axios.put("/survey/{id}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> The above command requires a JSON structured like this:

```json

{
  "id": 0,
  "title": "string",
  "category": "string",
  "surveyLink": "string",
  "created": "2022-07-20T08:32:47.603Z",
  "expiry": "2022-07-20T08:32:47.603Z",
  "status": "ACTIVE",
  "siteId": 0
}

```

Updates an existing survey associated with the given ID

### Parameters

Name | Description
--------- | ------- 
id (integer($int64)) | Id of the survey you want to update

### Response

<aside class="success">
Status Code 200 : Survey was updated
</aside>



