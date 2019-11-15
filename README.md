# Show All Customers

Get the details of the currently customers.

**URL** : `/api/v1/res_partner`

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

**URL** : `/api/v1/res_partner`

**Method** : `POST`

**Auth required** : YES

**Avaliabl fields**

- String
    - name
    - ref
    - vat
    - website
    - comment
    - function
    - street
    - street2
    - zip
    - city
    - type
    - email
    - phone
    - mobile
- Integer
    - color
- Boolean (true/false)
    - is_company
    - employee
- Float
    - credit_limit
    - partner_latitude
    - partner_longitude
- Many2one
    - title (```res.partner.title```)
    - parent_id (```res.partner```)
    - state_id (```res.country.state```)
    - country_id (```res.country```)
    - industry_id (```res.partner.industry```)
    - company_id (```res.company```)
- One2many
    - bank_ids (```res.partner.bank```)
    - child_ids (```res.partner.category```)
    - user_ids (```res.users```)

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
Content-Length: 4975
Server: Werkzeug/0.16.0 Python/3.6.9
Date: Fri, 15 Nov 2019 15:24:55 GMT

[
    {
        "id": 26,
        "signup_token": false,
        "signup_type": false,
        "signup_expiration": false,
        "signup_valid": false,
        "signup_url": false,
        "name": "Alex",
        "display_name": "Alex",
        "date": false,
        "title": false,
        "parent_id": false,
        "parent_name": false,
        "child_ids": [],
        "ref": false,
        "lang": "en_US",
        "active_lang_count": 1,
        "tz": false,
        "tz_offset": "+0000",
        "vat": false,
        "same_vat_partner_id": false,
        "bank_ids": [],
        "website": false,
        "comment": false,
        "category_id": [],
        "credit_limit": 0.0,
        "active": true,
        "employee": false,
        "function": false,
        "type": "contact",
        "street": "Antonovycha str.",
        "street2": false,
        "zip": false,
        "city": false,
        "state_id": false,
        "country_id": false,
        "partner_latitude": 0.0,
        "partner_longitude": 0.0,
        "email": "alex@com",
        "email_formatted": "Alex <alex@com>",
        "phone": false,
        "mobile": false,
        "is_company": false,
        "industry_id": false,
        "company_type": "person",
        "company_id": false,
        "color": 0,
        "user_ids": [],
        "partner_share": true,
        "contact_address": "Antonovycha str.\n\n  \n",
        "commercial_partner_id": [
            26,
            "Alex"
        ],
        "commercial_company_name": false,
        "company_name": false,
        "self": [
            26,
            "Alex"
        ],
        "activity_ids": [],
        "activity_state": false,
        "activity_user_id": false,
        "activity_type_id": false,
        "activity_date_deadline": false,
        "activity_summary": false,
        "activity_exception_decoration": false,
        "activity_exception_icon": false,
        "message_is_follower": true,
        "message_follower_ids": [
            89
        ],
        "message_partner_ids": [
            3
        ],
        "message_channel_ids": [],
        "message_ids": [
            84
        ],
        "message_unread": false,
        "message_unread_counter": 0,
        "message_needaction": false,
        "message_needaction_counter": 0,
        "message_has_error": false,
        "message_has_error_counter": 0,
        "message_attachment_count": 0,
        "message_main_attachment_id": false,
        "email_normalized": "alex@com",
        "is_blacklisted": false,
        "message_bounce": 0,
        "im_status": "im_partner",
        "channel_ids": [],
        "user_id": false,
        "website_message_ids": [],
        "credit": 0.0,
        "debit": 0.0,
        "debit_limit": 0.0,
        "total_invoiced": 0.0,
        "currency_id": [
            22,
            "UAH"
        ],
        "journal_item_count": 0,
        "property_account_payable_id": [],
        "property_account_receivable_id": [],
        "property_account_position_id": false,
        "property_payment_term_id": false,
        "property_supplier_payment_term_id": false,
        "ref_company_ids": [],
        "has_unreconciled_entries": false,
        "last_time_entries_checked": false,
        "invoice_ids": [],
        "contract_ids": [],
        "bank_account_count": 0,
        "trust": "normal",
        "invoice_warn": "no-message",
        "invoice_warn_msg": false,
        "supplier_rank": 0,
        "customer_rank": 0,
        "contact_address_complete": "Antonovycha str.,",
        "image_medium": false,
        "partner_gid": 0,
        "additional_info": false,
        "phone_sanitized": false,
        "phone_blacklisted": false,
        "property_product_pricelist": [
            1,
            "Public Pricelist (UAH)"
        ],
        "message_has_sms_error": false,
        "online_partner_vendor_name": false,
        "online_partner_bank_account": false,
        "payment_token_ids": [],
        "payment_token_count": 0,
        "image_1920": false,
        "image_1024": false,
        "image_512": false,
        "image_256": false,
        "image_128": false,
        "create_uid": [
            2,
            "Andrey Semko"
        ],
        "create_date": "2019-11-15 15:25:56",
        "write_uid": [
            2,
            "Andrey Semko"
        ],
        "write_date": "2019-11-15 15:25:56",
        "__last_update": "2019-11-15 15:25:56"
    }
]
```

## Bad Response

**Code** : `400 OK`

**Content examples**

```html

HTTP/1.0 400 BAD REQUEST
Content-Type: text/html
Content-Length: 4393
Server: Werkzeug/0.16.0 Python/3.6.9
Date: Fri, 15 Nov 2019 20:40:49 GMT

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>400 Bad Request</title>
<h1>Bad Request</h1>
<p>{'xmlrpc.client.Fault: Model: Contact (res.partner), Constraint: res_partner_parent_id_fkey', None)'}</p>

```
