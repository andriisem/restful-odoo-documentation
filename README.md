# Show Current Customer

Get the details of the currently customers.

**URL** : `api/v1/res_partner`

**Method** : `GET`

**Auth required** : YES

**Data constraints**

Python

```py

import requests

 data = {
   'host': 'andriisem.odoo.com',
   'dbname': 'andriisem'
 }

 response = requests.get('/api/v1/res_partner',  data=data, auth=('username', 'password'))


```
cURL
```bash

curl -X GET /api/v1/res_partner \
     -i --user username:password \
     -d host=andriisem.odoo.com \
     -d dbname=andriisem
```

## Success Response

**Code** : `200 OK`

**Content examples**

```json
[
    {
        "id": 3,
        "name": "Andrey Semko"
    },
    {
        "id": 7,
        "name": "Odoo"
    },
    {
        "id": 1,
        "name": "andriisem"
    }
]
```
  