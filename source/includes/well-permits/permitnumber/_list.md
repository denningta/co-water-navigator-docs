## List Well Permits

```shell
curl "https://cowaternavigator/api/well-permits?permit=FP-63209"
```

```javascript
const kittn = require("kittn");

let api = kittn.authorize("meowmeowmeow");
let kittens = api.kittens.get();
```

> Successful deletion will return the deleted records in JSON:

```json
[
  {
    "permit": "FP-63209",
    "contactName": "FP-63209"
    // ...etc
  },
  {
    "permit": "2021-02",
    "contactName": "FP-63209"
    // ...etc
  },
  {
    "permit": "2022-01",
    "contactName": "FP-63209"
    // ...etc
  }
  //...etc
]
```

This endpoint retrieves a list of well permit records matching the query parameters.

### HTTP Request

`GET /api/well-permits`

### Query Parameters

| Parameter   | Required | Description                                                  |
| ----------- | -------- | ------------------------------------------------------------ |
| permit      | false    | Query by one or more well permit numbers.                    |
| reciept     | false    | Query by the reciept number associated with the well permit. |
| contactName | false    | Query by one or more contact names.                          |
