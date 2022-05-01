# Fields #
REST API End Points for managing and checking GD Fields.

## Fields properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                          | integer   | Unique identifier for the object. <i class="label label-info">read-only</i>                                                          |
| `type`                        | string    | Post type slug.|
| `name`                      | string    | unique field key. |
| `title`                | string | field title.|
| `admin_title`                | string | field title for admin view.|
| `description`                | string | field description.|
| `data_type`                | string | field datatype.( TEXT, NUMBER, VARCHAR )|
| `field_type`                | string | field type it could be ( text, select, checkbox, radio, textarea, address, category, url, email, phone, datepicker)|
| `field_type_key`                | string | field type key.|
| `decimal_point`                | string | Decimal point.|
| `default_value`                | string | Default value of field.|
| `placeholder`                | string | Placeholder of field.|
| `required`                | string | Required field.|
| `required_msg`                | string | Required message.|
| `validation_pattern`                | string | Validation pattern for field.|
| `validation_msg`                | string | Validation message for field.|
| `option_values`                | string | Optional value for optional fields like select, checkbox lists, list.|
| `location`                | string | display location for field.|
| `order`                | string | order of field.|
| `icon`                | string | field icon.|
| `class`                | string | field class.|
| `status`                | string | 1 for active and 0 for inactive.|
| `packages`                | string | comma separated package ids for the field, for which field is available |
| `tab_parent`                | string | Field parent tab. |
| `tab_level`                | string | Field tab level. |
| `sorting`                | string | Show field in post sorting? |
| `searching`                | string | Show field in post search? |
| `extra_fields`                | string | Field extra setting |

## Retrieve a field ##

This API lets you retrieve and view a specific field by name.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/&lt;fields&gt;</h6>
	</div>
</div>

```shell
curl https://example.com//wp-json/geodir/v2/fields \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "id": "41",
        "type": "gd_event",
        "name": "package_id",
        "title": "Package",
        "admin_title": "Package",
        "description": "Select your package.",
        "data_type": "INT",
        "field_type": "text",
        "field_type_key": "package_id",
        "decimal_point": "",
        "default_value": "",
        "placeholder": "",
        "required": false,
        "required_msg": "",
        "validation_pattern": "",
        "validation_msg": "",
        "option_values": "",
        "location": "",
        "order": 2,
        "icon": "fas fa-dollar-sign",
        "class": "",
        "default": true,
        "private": false,
        "status": 1,
        "packages": "",
        "tab_parent": "0",
        "tab_level": 0,
        "sorting": false,
        "searching": false,
        "extra_fields": "",
        "_links": {
            "self": [
                {
                    "href": "https://ppldb.com/v2/wp-json/geodir/v2/fields/41"
                }
            ],
            "collection": [
                {
                    "href": "https://ppldb.com/v2/wp-json/geodir/v2/fields"
                }
            ]
        }
    },
    {
        "id": "42",
        "type": "gd_event",
        "name": "expire_date",
        "title": "Expire Date",
        "admin_title": "Expire Date",
        "description": "Post expire date, usually set automatically. Leave blank to set expire date &quot;Never&quot;.",
        "data_type": "DATE",
        "field_type": "datepicker",
        "field_type_key": "expire_date",
        "decimal_point": "",
        "default_value": "",
        "placeholder": "",
        "required": false,
        "required_msg": "",
        "validation_pattern": "",
        "validation_msg": "",
        "option_values": "",
        "location": "",
        "order": 1,
        "icon": "fas fa-clock",
        "class": "",
        "default": true,
        "private": true,
        "status": 1,
        "packages": "",
        "tab_parent": "0",
        "tab_level": 0,
        "sorting": false,
        "searching": false,
        "extra_fields": "",
        "_links": {
            "self": [
                {
                    "href": "https://ppldb.com/v2/wp-json/geodir/v2/fields/42"
                }
            ],
            "collection": [
                {
                    "href": "https://ppldb.com/v2/wp-json/geodir/v2/fields"
                }
            ]
        }
    },
]
