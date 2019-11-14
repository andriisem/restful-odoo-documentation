# Show All Customers

Get the details of the currently customers.

**URL** : `api/v1/res_partner`

**Method** : `GET`

**Auth required** : YES

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
     -d host='andriisem.odoo.com' \
     -d dbname='andriisem'
```

## Success Response

**Code** : `200 OK`

**Content examples**

```json
HTTP/1.0 200 OK
Content-Type: application/json
Content-Length: 742
Server: Werkzeug/0.16.0 Python/3.6.9
Date: Thu, 14 Nov 2019 17:08:51 GMT
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
  
# Create Customer

Create new customer

**URL** : `api/v1/res_partner`

**Method** : `POST`

**Auth required** : YES

**Avaliabl fields**

- name
- email
- street
- street2
- zip

I'll add the rest soon...

Python

```py

import requests

 data = {
   'host': 'andriisem.odoo.com',
   'dbname': 'andriisem',
   'name': 'Andrii Sem',
   'email': 'andrii@sem.com',
   'street': 'Antonovycha str.',

 }
 response = requests.post('/api/v1/res_partner',  data=data, auth=('username', 'password'))
```

cURL
```bash
curl -X POST /api/v1/res_partner \
     -i --user username:password \
     -d host='andriisem.odoo.com' \
     -d dbname='andriisem' \
     -d name='Andrii Sem' \
     -d email='andrii@sem.com' \
     -d street='Antonovycha str.'
```

## Success Response

**Code** : `200 OK`

**Content examples**

```json
HTTP/1.0 200 OK
Content-Type: application/json
Content-Length: 63
Server: Werkzeug/0.16.0 Python/3.6.9
Date: Thu, 14 Nov 2019 17:05:38 GMT

[
    {
        "id": 22,
        "name": "Andrii Sem"
    }
]
```