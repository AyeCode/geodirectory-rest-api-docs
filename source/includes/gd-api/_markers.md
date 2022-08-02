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

This API lets you retrieve and view a specific marker by post type.

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
```

## Retrieve a Single Marker Data ##

This API lets you retrieve and view a specific marker by post id.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/markers/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl https://example.com//wp-json/geodir/v2/markers/<id> \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
    "html": "<div class=\"gd-bubble bsui\" style=\"\">\n\t<div class=\"gd-bubble-inside\">\n\t\t<div class=\"geodir-bubble_desc\">\n\t\t\t<div class=\"geodir-post-title bsui sdel-3ab4ade6\" >\t\t<h4 class=\"geodir-entry-title  h5 \">\n\t\t\t<a href=\"http://localhost:10005/places/united-states/pennsylvania/philadelphia/attractions/please-touch-museum/\" class=\"\" title=\"View: Please Touch Museum\">Please Touch Museum</a>\n\t\t</h4>\n\t\t</div>\n\t\t\t<div class=\"geodir-bubble_image pb-2\">\n\t\t\t\t<div class=\"geodir-post-slider bsui sdel-54815a97\" ><div class=\" geodir-image-container geodir-image-sizes-medium_large   \" >\n\t\n\t\t\t\t<div class=\"geodir-images geodir-images-n-1 geodir-images-image carousel-inner  \"><div class='carousel-item  active' ><a href='http://localhost:10005/places/united-states/pennsylvania/philadelphia/attractions/please-touch-museum/' class='geodir-link-image embed-has-action embed-responsive embed-responsive-16by9 d-block'><img src=\"http://localhost:10005/wp-content/uploads/2022/07/2.png\" alt=\"2\" width=\"600\" height=\"400\" class=\"align size-medium_large geodir-image-102 embed-responsive-item embed-item-cover-xy  w-100 p-0 m-0 mw-100 border-0\" srcset=\"http://localhost:10005/wp-content/uploads/2022/07/2.png 600w, http://localhost:10005/wp-content/uploads/2022/07/2-300x200.png 300w\" sizes=\"(max-width: 600px) 100vw, 600px\" /><i class=\"fas fa-link\" aria-hidden=\"true\"></i></a></div>\t\t</div>\n\n\n\t\t\n\t\t</div>\n</div>\n\t\t\t</div>\n\t\t\t<div class=\"geodir-bubble-meta-top clearfix\">\n\t\t\t\t<div class=\"geodir-post-rating bsui sdel-a61cd2d5\" ><div class=\"geodir_post_meta gd-rating-info-wrap  float-left mr-2  geodir-post-rating-value-0\" data-rating=\"0\">        <div class=\"gd-list-rating-stars d-inline-block\">\n           <div class=\"gd-rating-outer-wrap gd-rating-output-wrap d-flex d-flex justify-content-between flex-nowrap w-100\">\t\t\t<div class=\"gd-rating gd-rating-output gd-rating-type-font-awesome\">\n\t\t\t<span class=\"gd-rating-wrap d-inline-flex position-relative \" title=\"No rating yet!\">\n\t\t\t\t<span class=\"gd-rating-foreground position-absolute text-nowrap overflow-hidden\" style='width:0%;  color:#ff9900; '>\n\t\t\t\t<i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i>\t\t\t\t</span>\n\t\t\t\t<span class=\"gd-rating-background\" style='color:#afafaf;'>\n\t\t\t\t<i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i><i class=\"fas fa-star fa-fw\" aria-hidden=\"true\" ></i>\t\t\t\t</span>\n\t\t\t</span>\n\t\t\t\t\t\t\t</div>\n\t\t\t</div>        </div>\n        </div></div>\n\t\t\t\t<div class=\"geodir-post-fav bsui sdel-c4bb63e4\" ><div class=\"geodir_post_meta gd-fav-info-wrap  float-right ml-2  gd-fav-hide-text \" >\t\t<span class=\"gd-list-favorite\">\n\t\t\t<span class=\"geodir-addtofav favorite_property_197  h6\">\n\t<a href=\"javascript:void(0);\" title=\"Add to Favorites\"  class=\"geodir-addtofav-icon\"  data-color-on=\"#e84739\"  data-icon=\"fas fa-heart\"  data-color-off=\"grey\"  data-toggle=\"tooltip\"  onclick=\"javascript:window.location.href='http://localhost:10005/wp-login.php'\"  ><i class=\"fas fa-heart\"  style=\"color:grey;\" ></i> <span class=\"geodir-fav-text gv-secondary sr-only\" style=\"\">Favorite</span></a>\n</span>\n\t\t</span>\n\t\t</div></div>\n\t\t\t</div>\n\t\t\t<div class=\"geodir-bubble-meta-side\">\n\t\t\t\t<div class=\"geodir-output-location bsui sdel-deec5859\" ><div class='  d-block geodir-output-location geodir-output-location-mapbubble' style='' ><div class=\"geodir_post_meta  list-group-item list-group-item-action  geodir-field-post_title\"><span class=\"geodir_post_meta_icon geodir-i-text\" style=\"\"><i class=\"fas fa-minus fa-fw\" aria-hidden=\"true\"></i> <span class=\"geodir_post_meta_title \" >Place Title: </span></span>Please Touch Museum</div><div class=\"geodir_post_meta  list-group-item list-group-item-action  geodir-field-address\" itemscope itemtype=\"http://schema.org/PostalAddress\"><span class=\"geodir_post_meta_icon geodir-i-address\" style=\"\"><i class=\"fas fa-map-marker-alt fa-fw\" aria-hidden=\"true\"></i> <span class=\"geodir_post_meta_title \" >Address: </span></span><span itemprop=\"streetAddress\">1200 Sansom St</span><br>   <span itemprop=\"addressLocality\">Philadelphia</span><br> <span itemprop=\"addressRegion\">Pennsylvania</span><br> <span itemprop=\"postalCode\">19107</span><br> <span itemprop=\"addressCountry\">United States</span></div><div class=\"geodir_post_meta  list-group-item list-group-item-action  geodir-field-phone\"><span class=\"geodir_post_meta_icon geodir-i-phone\" style=\"\"><i class=\"fas fa-phone fa-fw\" aria-hidden=\"true\"></i> <span class=\"geodir_post_meta_title \" >Phone: </span></span><a href=\"tel:2227771111\">(222) 777-1111</a></div></div></div>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n</div>"
}
```