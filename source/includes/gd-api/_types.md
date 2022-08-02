# Types #
REST API End Points for managing and checking GD Post Types.

## Types properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `description`                          | string   | post typ description.                        |
| `hierarchical`                        | boolean    | false|
| `name`                      | string    | post type name. |
| `slug`                | string | post type slug.|
| `taxonomies`                | array | taxonomies array.|
| `rest_base`                | string | cpt slug.|

## Retrieve post types Data ##

This API lets you retrieve and view specific post type data.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/types</h6>
	</div>
</div>


```shell
curl https://example.com/wp-json/geodir/v2/types\
	-u consumer_key:consumer_secret
```
> JSON response example:

```json

{
    "gd_place": {
        "description": "Place post type.",
        "hierarchical": false,
        "name": "Places",
        "slug": "gd_place",
        "taxonomies": [
            "gd_place_tags",
            "gd_placecategory"
        ],
        "rest_base": "places",
        "_links": {
            "collection": [
                {
                    "href": "http://local.newwp.test/wp-json/geodir/v2/types"
                }
            ],
            "fields": [
                {
                    "href": "http://local.newwp.test/wp-json/geodir/v2/places/fields"
                }
            ],
            "wp:items": [
                {
                    "href": "http://local.newwp.test/wp-json/geodir/v2/places"
                }
            ],
            "curies": [
                {
                    "name": "wp",
                    "href": "https://api.w.org/{rel}",
                    "templated": true
                }
            ]
        }
    }
}
```

## Retrieve single post types Data ##

This API lets you retrieve and view specific single post type data.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/types/&lt;post_type_rest_base&gt;</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/geodir/v2/types/<post_type_rest_base>
	-u consumer_key:consumer_secret
```
> JSON response example:

```json
{
    "description": "Place post type.",
    "hierarchical": false,
    "name": "Places",
    "slug": "gd_place",
    "taxonomies": [
        "gd_place_tags",
        "gd_placecategory"
    ],
    "rest_base": "places",
    "_links": {
        "collection": [
            {
                "href": "http://local.newwp.test/wp-json/geodir/v2/types"
            }
        ],
        "fields": [
            {
                "href": "http://local.newwp.test/wp-json/geodir/v2/places/fields"
            }
        ],
        "wp:items": [
            {
                "href": "http://local.newwp.test/wp-json/geodir/v2/places"
            }
        ],
        "curies": [
            {
                "name": "wp",
                "href": "https://api.w.org/{rel}",
                "templated": true
            }
        ]
    }
}
```
## Create Comment ##

## Update Comment ##