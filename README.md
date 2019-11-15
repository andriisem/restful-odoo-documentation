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
<p>{'xmlrpc.client.Fault: &lt;Fault 1: \'Traceback (most recent call last):\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/service/model.py&quot;, line 93, in wrapper\\n    return f(dbname, *args, **kwargs)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/service/model.py&quot;, line 175, in execute\\n    res = execute_cr(cr, uid, obj, method, *args, **kw)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/service/model.py&quot;, line 164, in execute_cr\\n    return odoo.api.call_kw(recs, method, args, kw)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 393, in call_kw\\n    result = _call_kw_model_create(method, model, args, kwargs)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 373, in _call_kw_model_create\\n    result = method(recs, *args, **kwargs)\\n  File &quot;&lt;decorator-gen-108&gt;&quot;, line 2, in create\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 343, in _model_create_multi\\n    return create(self, [arg])\\n  File &quot;/home/odoo/src/odoo/13.0/addons/account/models/partner.py&quot;, line 504, in create\\n    return super().create(vals_list)\\n  File &quot;&lt;decorator-gen-126&gt;&quot;, line 2, in create\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 344, in _model_create_multi\\n    return create(self, arg)\\n  File &quot;/home/odoo/src/odoo/13.0/addons/partner_autocomplete/models/res_partner.py&quot;, line 183, in create\\n    partners = super(ResPartner, self).create(vals_list)\\n  File &quot;&lt;decorator-gen-79&gt;&quot;, line 2, in create\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 344, in _model_create_multi\\n    return create(self, arg)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/addons/base/models/res_partner.py&quot;, line 536, in create\\n    partners = super(Partner, self).create(vals_list)\\n  File &quot;&lt;decorator-gen-102&gt;&quot;, line 2, in create\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 344, in _model_create_multi\\n    return create(self, arg)\\n  File &quot;/home/odoo/src/odoo/13.0/addons/mail/models/mail_thread.py&quot;, line 269, in create\\n    threads = super(MailThread, self).create(vals_list)\\n  File &quot;&lt;decorator-gen-3&gt;&quot;, line 2, in create\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/api.py&quot;, line 344, in _model_create_multi\\n    return create(self, arg)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/models.py&quot;, line 3707, in create\\n    records = self._create(data_list)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/models.py&quot;, line 3793, in _create\\n    cr.execute(query, params)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/sql_db.py&quot;, line 163, in wrapper\\n    return f(self, *args, **kwargs)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/sql_db.py&quot;, line 240, in execute\\n    res = self._obj.execute(query, params)\\npsycopg2.IntegrityError: insert or update on table &quot;res_partner&quot; violates foreign key constraint &quot;res_partner_parent_id_fkey&quot;\\nDETAIL:  Key (parent_id)=(32) is not present in table &quot;res_partner&quot;.\\n\\n\\nDuring handling of the above exception, another exception occurred:\\n\\nTraceback (most recent call last):\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/addons/base/controllers/rpc.py&quot;, line 63, in xmlrpc_2\\n    response = self._xmlrpc(service)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/addons/base/controllers/rpc.py&quot;, line 43, in _xmlrpc\\n    result = dispatch_rpc(service, method, params)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/http.py&quot;, line 138, in dispatch_rpc\\n    result = dispatch(method, params)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/service/model.py&quot;, line 40, in dispatch\\n    res = fn(db, uid, *params)\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/service/model.py&quot;, line 168, in execute_kw\\n    return execute(db, uid, obj, method, *args, **kw or {})\\n  File &quot;/home/odoo/src/odoo/13.0/odoo/service/model.py&quot;, line 153, in wrapper\\n    raise ValidationError(msg)\\nodoo.exceptions.ValidationError: (\\\'The operation cannot be completed: another model requires the record being deleted. If possible, archive it instead.\\\\n\\\\nModel: Contact (res.partner), Constraint: res_partner_parent_id_fkey\\\', None)\\n\'&gt;'}</p>

```
