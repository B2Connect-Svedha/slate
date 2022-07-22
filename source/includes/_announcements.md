
# Announcements

## List all announcements

> GET /announcement/

```dart
var request = http.Request('GET', Uri.parse('http://api-qa2.b2connect.me/management/announcement/?page=1&per_page=10'));


http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}

```

```shell

curl --location --request GET 'http://api-qa2.b2connect.me/management/announcement/?page=1&per_page=10'

```

```javascript

const axios = require("axios");

axios.get("/announcement/").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> Response if STATUS CODE 200:

```json

{
    "success": true,
    "code": 0,
    "message": "",
    "body": {
        "total": 100,
        "announcements": [
            {
                "id": 18,
                "title": "adawd",
                "category": "Maintenance & Support",
                "description": "adad",
                "image": "683a41df-85ed-430a-a81c-286cf3196ba2.png",
                "created": 1650853737.002060000,
                "start": null,
                "expiry": 1652889600.000000000,
                "status": "ACTIVE",
                "siteId": null
            },
            {
                "id": 109,
                "title": "asdasdasd",
                "category": "Health & Safety",
                "description": "asdasdasd",
                "image": "ad0ce186-df68-4e53-9292-db0a200aa911.gif",
                "created": 1655364055.906176000,
                "start": null,
                "expiry": 1643556.055000000,
                "status": "INACTIVE",
                "siteId": 36
            }
        ]
    }
}

```

> Example Response for STATUS CODE 404:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Retrieves the list of all announcements

### Parameters

Name | Description
--------- | ------- 
page (integer($int32)) | Default value: 1
per_page (integer($int32)) | Default value: 10

### Response

<aside class="success">
Status Code 200 : All announcements were fetched
</aside>

<aside class="warning">
Status Code 404 : Announcement was not found
</aside>


## Retrieve a specific announcement

> GET /announcement/{id}


```dart

curl --location --request GET 'http://api-qa2.b2connect.me/management/announcement/92818518'

```

```shell
curl --location --request GET 'http://api-qa2.b2connect.me/management/announcement/92818518'
```

```javascript

const axios = require("axios");

axios.get("/announcement/{id}").then((res) => {
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
  "description": "string",
  "image": "string",
  "created": "2022-07-20T08:54:59.512Z",
  "start": "2022-07-20T08:54:59.512Z",
  "expiry": "2022-07-20T08:54:59.512Z",
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
  "description": "string",
  "image": "string",
  "created": "2022-07-20T08:54:59.518Z",
  "start": "2022-07-20T08:54:59.518Z",
  "expiry": "2022-07-20T08:54:59.518Z",
  "status": "ACTIVE",
  "siteId": 0
}

```

Retrieves the announcement assisociated with the specific ID given

### Parameters

Name | Description
--------- | ------- 
id (integer($int64)) | Id of the announcement you want to retrieve

### Response

<aside class="success">
Status Code 200 : Announcement was fetched
</aside>

<aside class="warning">
Status Code 404 : Announcement was not found
</aside>


## Create a new announcement 

> POST /announcement


```dart

var request = http.MultipartRequest('POST', Uri.parse('http://api-qa2.b2connect.me/management/announcement/?title=fugiat pariatur&category=fugiat pariatur&description=fugiat pariatur&start=1977-10-28&expiry=1977-10-28'));
request.files.add(await http.MultipartFile.fromPath('file', '/path/to/file'));

http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}


```

```shell

curl --location --request POST 'http://api-qa2.b2connect.me/management/announcement/?title=fugiat pariatur&category=fugiat pariatur&description=fugiat pariatur&start=1977-10-28&expiry=1977-10-28' \
--form 'file=@"/path/to/file"'

```

```javascript

const axios = require("axios");

axios.post("/announcement").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

Creates a new announcement 


### Parameters

Name | Description
--------- | ------- 
title (string) | title of the announcement
category (string) | the category the announcement belongs to
description (string) | announcement description
start (string ($date)) | start date of the announcement
expiry (string ($date)) | end date of the announcement

### Response

<aside class="success">
Status Code 200 : Announcement was created
</aside>



## Update exisiting announcement

> PUT /announcement/{id}


```dart

var request = http.Request('PUT', Uri.parse('http://api-qa2.b2connect.me/management/announcement/92818518?title=fugiat pariatur&category=fugiat pariatur&description=fugiat pariatur&status=fugiat pariatur&start=1977-10-28&expiry=1977-10-28'));


http.StreamedResponse response = await request.send();

if (response.statusCode == 200) {
  print(await response.stream.bytesToString());
}
else {
  print(response.reasonPhrase);
}


```

```shell

curl --location --request PUT 'http://api-qa2.b2connect.me/management/announcement/92818518?title=fugiat pariatur&category=fugiat pariatur&description=fugiat pariatur&status=fugiat pariatur&start=1977-10-28&expiry=1977-10-28'

```

```javascript

const axios = require("axios");

axios.put("/announcement/{id}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

> The above command requires a JSON structured like this:

Updates an existing announcement associated with the given ID

### Parameters

Name | Description
--------- | ------- 
title (string) | title of the announcement
category (string) | the category the announcement belongs to
description (string) | announcement description
start (string ($date)) | start date of the announcement
expiry (string ($date)) | end date of the announcement

### Response

<aside class="success">
Status Code 200 : Announcement was updated
</aside>


