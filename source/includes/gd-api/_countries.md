# Countries #
REST API End Points for managing and checking GD Countries.

## Countries properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                          | integer   | Unique identifier for the object. <i class="label label-info">read-only</i>                                                          |
| `name`                        | string    | Name of country.|
| `title`                      | string    | Title for country. |
| `iso2`                | string | iso2 code for country|
| `iso3`                | string | iso3 code for country|

## Retrieve a country ##

This API lets you retrieve and view a specific country by name.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/countries/&lt;name&gt;</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/geodir/v2/countries/Afghanistan \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
    "id": null,
    "name": "Afghanistan",
    "title": "Afghanistan",
    "iso2": null,
    "iso3": null,
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/geodir/v2/countries/0"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/geodir/v2/countries"
            }
        ]
    }
}
```

## List all countries ##

This API helps you to list all the countries that have been created.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/countries</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/geodir/v2/countries \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "id": null,
        "name": "Afghanistan",
        "title": "Afghanistan",
        "iso2": null,
        "iso3": null,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/geodir/v2/countries/0"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/geodir/v2/countries"
                }
            ]
        }
    },
    {
        "id": null,
        "name": "Åland Islands",
        "title": "Åland Islands",
        "iso2": null,
        "iso3": null,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/geodir/v2/countries/0"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/geodir/v2/countries"
                }
            ]
        }
    }
]
```
