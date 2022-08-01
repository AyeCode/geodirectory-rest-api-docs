# Markers #
REST API End Points to access map markers data.

## Marker properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                          | integer   | Unique identifier for the object. <i class="label label-info">read-only</i>                                                          |
| `total`                        | int    | total marker founds.|
| `baseurl`                      | string    | upload directory url. |
| `content_url`                | string | content directory url.|
| `icons`                | array | markers icons array.|
| `items`                | array | markers data array.|

## Retrieve a Marker Data ##

This API lets you retrieve and view a specific field by name.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/markers?post_type=&lt;gd_place&gt;</h6>
	</div>
</div>

```shell
curl https://example.com//wp-json/geodir/v2/markers \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "total": 2,
        "baseurl": "http://localhost:10005/wp-content/uploads",
        "content_url": "http://localhost:10005/wp-content/",
        "icons": {
            "63": {
                "i": "2021/03/Attractions.png",
                "w": 36,
                "h": 45
            }
        },
        "items": [
            {
                "m": "195",
                "lt": "39.920996451631",
                "ln": "-75.016184453886",
                "t": "Franklin Square",
                "i": 63
            },
            {
                "m": "197",
                "lt": "39.949757529995836",
                "ln": "-75.1605083405838",
                "t": "Please Touch Museum",
                "i": 63
            }
        ]
    }
]
