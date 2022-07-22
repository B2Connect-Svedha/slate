# Users

## Add Emirates ID

> PUT /users​/{userId}​/emirates-id

```dart
var request = http.Request('PUT', Uri.parse('http://api-qa2.b2connect.me/management/users/92818518/emirates-id'));
request.body = {
  name: "John Doe",
  sex: "Male",
  dateOfBirth: 23061999,
  nationality: "EA",
  emiratesId: "78420036810972",
  expiryDate: 22052027
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

curl 'http://api-qa2.b2connect.me/management/users/:userId/emirates-id' /


```

```javascript

const axios = require("axios");

axios.put("/users/{userId}/emirates-id").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```


Saves the Emirates ID details of the user by either updating an exisiting ID or creating a new one if it's the first time.

### Parameters

Name | Description
--------- | ------- 
userId (integer($int64)) | This associates the emirates ID with a specific user ID to link the details to the user's account

### Response 

<aside class="success">
Status Code 200 : OK
</aside>


## Filter through users

> POST ​/users​/count

```dart
var request = http.Request('POST', Uri.parse('http://api-qa2.b2connect.me/management/users/count'));
request.body = {
    {
      filterField: "CHANNEL",
      filterType: "INACTIVE_DURING_DAYS",
      text: "consequat anim do ea"
    },

    {
      filterField: "JOB_ROLE",
      filterType: "ENDS_WITH",
      text: "cillum aliqua pariatur nulla"
    }
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

curl --location --request POST 'http://api-qa2.b2connect.me/management/users/count' \


```

```javascript
const axios = require("axios");

axios.post("/users/count").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})

```

Returns the user count by using specific filters

### Parameters

No parameters

### Response

<aside class="success">
Status Code 200 : OK
</aside>
