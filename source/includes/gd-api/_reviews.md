# Reviews #
REST API End Points for managing and checking GD Reviews.

## Reviews properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                          | integer   | Review id. <i class="label label-info">read-only</i>                                                          |
| `post`                        | integer    | Post id.|
| `parent`                      | integer    | review parent id. |
| `author`                | string | review author id.|
| `author_name`                | array | review author name.|
| `author_url`                | string | review author url.|
| `date`                | string | review date.|
| `date_gmt`                | string | review date in GMT.|
| `content`                | array | review content.|
| `link`                | string | review link.|
| `status`                | string | review status.|
| `type`                | string | review type.|
| `post_type`                | string | review post post type.|
| `rating`                | string | rating of review.|
| `country`                | string | country of reviewed post.|
| `region`                | string | region of reviewed post.|
| `city`                | string | city of reviewed post.|
| `latitude`                | string | latitude of reviewed post.|
| `longitude`                | string | longitude of reviewed post.|
| `author_avatar_urls`                | array | review author avatar urls.|
| `meta`                | array | review meta.|

## Retrieve the Reviews Data ##

This API lets you retrieve all the review data.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/reviews</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/geodir/v2/reviews\
	-u consumer_key:consumer_secret
```
> JSON response example:

```json
[
    {
        "id": 25,
        "post": 871,
        "parent": 0,
        "author": 1,
        "author_name": "admin",
        "author_url": "",
        "date": "2019-05-09T15:13:05",
        "date_gmt": "2019-05-09T15:13:05",
        "content": {
            "rendered": "Some text"
        },
        "link": "http://local.newwp.test/places/canada/ontario/king/houses/richmore-apartments-test123-food2#comment-25",
        "status": "approved",
        "type": "comment",
        "post_type": "gd_place",
        "rating": 5,
        "country": "Canada",
        "region": "Ontario",
        "city": "King",
        "latitude": "-79.58547458052635",
        "longitude": "44.012415575653726",
        "author_avatar_urls": {
            "24": "http://1.gravatar.com/avatar/ad5dd285560221a7302608c74c690035?s=24&d=mm&r=g",
            "48": "http://1.gravatar.com/avatar/ad5dd285560221a7302608c74c690035?s=48&d=mm&r=g",
            "96": "http://1.gravatar.com/avatar/ad5dd285560221a7302608c74c690035?s=96&d=mm&r=g"
        },
        "meta": [],
        "_links": {
            "self": [
                {
                    "href": "http://local.newwp.test/wp-json/geodir/v2/reviews/25"
                }
            ],
            "collection": [
                {
                    "href": "http://local.newwp.test/wp-json/geodir/v2/reviews"
                }
            ],
            "author": [
                {
                    "embeddable": true,
                    "href": "http://local.newwp.test/wp-json/wp/v2/users/1"
                }
            ],
            "up": [
                {
                    "embeddable": true,
                    "post_type": "gd_place",
                    "href": "http://local.newwp.test/wp-json/geodir/v2/places/871"
                }
            ]
        }
    }
]
```

## Retrieve Single Reviews Data by ID ##

This API lets you retrieve all the review data by review id.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/reviews/&lt;review_id&gt;</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/geodir/v2/reviews/<review_id>
	-u consumer_key:consumer_secret
```
> JSON response example:

```json
{
    "id": 11,
    "post": 197,
    "parent": 0,
    "author": 1,
    "author_name": "admin",
    "author_url": "http://localhost:10005",
    "date": "2022-08-02T08:07:03",
    "date_gmt": "2022-08-02T08:07:03",
    "content": {
        "rendered": "<div class=\"description\"><p>dasdsad asdsad</p>\n</div>"
    },
    "link": "http://localhost:10005/places/united-states/pennsylvania/philadelphia/attractions/please-touch-museum/#comment-11",
    "status": "approved",
    "type": "comment",
    "post_type": "gd_place",
    "country": "United States",
    "region": "Pennsylvania",
    "city": "Philadelphia",
    "latitude": "-75.1605083405838",
    "longitude": "39.949757529995836",
    "rating": {
        "id": "overall",
        "label": "Overall",
        "rating": "5",
        "html": "<div class=\"gd-rating-outer-wrap gd-rating-output-wrap d-flex d-flex justify-content-between flex-nowrap w-100\">\t\t\t<div class=\"gd-rating gd-rating-output gd-rating-type-font-awesome\">\n\t\t\t<span class=\"gd-rating-wrap d-inline-flex position-relative \" title=\"5 star rating\">\n\t\t\t\t<span class=\"gd-rating-foreground position-absolute text-nowrap overflow-hidden\" style='width:100%;  color:#ff9900; '>\n\t\t\t\t<i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i>\t\t\t\t</span>\n\t\t\t\t<span class=\"gd-rating-background\" style='color:#afafaf;'>\n\t\t\t\t<i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i>\t\t\t\t</span>\n\t\t\t</span>\n\t\t\t\t\t\t\t</div>\n\t\t\t</div>"
    },
    "author_avatar_urls": {
        "24": "http://0.gravatar.com/avatar/c2b06ae950033b392998ada50767b50e?s=24&d=mm&r=g",
        "48": "http://0.gravatar.com/avatar/c2b06ae950033b392998ada50767b50e?s=48&d=mm&r=g",
        "96": "http://0.gravatar.com/avatar/c2b06ae950033b392998ada50767b50e?s=96&d=mm&r=g"
    },
    "meta": [],
    "_links": {
        "self": [
            {
                "href": "http://localhost:10005/wp-json/geodir/v2/reviews/11"
            }
        ],
        "collection": [
            {
                "href": "http://localhost:10005/wp-json/geodir/v2/reviews"
            }
        ],
        "author": [
            {
                "embeddable": true,
                "href": "http://localhost:10005/wp-json/wp/v2/users/1"
            }
        ],
        "up": [
            {
                "embeddable": true,
                "post_type": "gd_place",
                "href": "http://localhost:10005/wp-json/geodir/v2/places/197"
            }
        ]
    }
}{
    "id": 11,
    "post": 197,
    "parent": 0,
    "author": 1,
    "author_name": "admin",
    "author_url": "http://localhost:10005",
    "date": "2022-08-02T08:07:03",
    "date_gmt": "2022-08-02T08:07:03",
    "content": {
        "rendered": "<div class=\"description\"><p>dasdsad asdsad</p>\n</div>"
    },
    "link": "http://localhost:10005/places/united-states/pennsylvania/philadelphia/attractions/please-touch-museum/#comment-11",
    "status": "approved",
    "type": "comment",
    "post_type": "gd_place",
    "country": "United States",
    "region": "Pennsylvania",
    "city": "Philadelphia",
    "latitude": "-75.1605083405838",
    "longitude": "39.949757529995836",
    "rating": {
        "id": "overall",
        "label": "Overall",
        "rating": "5",
        "html": "<div class=\"gd-rating-outer-wrap gd-rating-output-wrap d-flex d-flex justify-content-between flex-nowrap w-100\">\t\t\t<div class=\"gd-rating gd-rating-output gd-rating-type-font-awesome\">\n\t\t\t<span class=\"gd-rating-wrap d-inline-flex position-relative \" title=\"5 star rating\">\n\t\t\t\t<span class=\"gd-rating-foreground position-absolute text-nowrap overflow-hidden\" style='width:100%;  color:#ff9900; '>\n\t\t\t\t<i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i>\t\t\t\t</span>\n\t\t\t\t<span class=\"gd-rating-background\" style='color:#afafaf;'>\n\t\t\t\t<i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i>\t\t\t\t</span>\n\t\t\t</span>\n\t\t\t\t\t\t\t</div>\n\t\t\t</div>"
    },
    "author_avatar_urls": {
        "24": "http://0.gravatar.com/avatar/c2b06ae950033b392998ada50767b50e?s=24&d=mm&r=g",
        "48": "http://0.gravatar.com/avatar/c2b06ae950033b392998ada50767b50e?s=48&d=mm&r=g",
        "96": "http://0.gravatar.com/avatar/c2b06ae950033b392998ada50767b50e?s=96&d=mm&r=g"
    },
    "meta": [],
    "_links": {
        "self": [
            {
                "href": "http://localhost:10005/wp-json/geodir/v2/reviews/11"
            }
        ],
        "collection": [
            {
                "href": "http://localhost:10005/wp-json/geodir/v2/reviews"
            }
        ],
        "author": [
            {
                "embeddable": true,
                "href": "http://localhost:10005/wp-json/wp/v2/users/1"
            }
        ],
        "up": [
            {
                "embeddable": true,
                "post_type": "gd_place",
                "href": "http://localhost:10005/wp-json/geodir/v2/places/197"
            }
        ]
    }
}
```