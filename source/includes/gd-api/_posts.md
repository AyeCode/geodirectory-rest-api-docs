# Posts #
REST API End Points for managing and checking GD Posts.


## Posts properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                          | integer   | Unique identifier for the object. <i class="label label-info">read-only</i>                                                          |
| `id`                        | int    | post id.|
| `slug`                      | string    | post slug. |
| `link`                | string | post url.|
| `status`                | string | status of post.|
| `type`                | string | post type.|
| `author`                | int | post author id.|
| `date`                | string | post date.|
| `date_gmt`                | string | post date in GMT format.|
| `modified`                | string | post modified date.|
| `modified_gmt`                | string | post modified_gmt date.|
| `default_category`                | int | default category id.|
| `modified_gmt`                | string | post modified_gmt date.|
| `post_category`                | array | post category array.|
| `street`                | string | street name.|
| `country`                | string | post country.|
| `region`                | string | post region.|
| `city`                | string | post city.|
| `zip`                | string | post zip.|
| `latitude`                | string | post latitude.|
| `longitude`                | string | post longitude.|
| `mapview`                | string | mapview.|
| `mapzoom`                | string | mapzoom level.|
| `ping_status`                | string | ping_status.|
| `comment_status`                | string | comment_status.|
| `images`                | string | images.|
| `rating`                | string | rating.|
| `rating_count`                | string | rating_count.|

## Retrieve a Posts Data ##

This API lets you retrieve and view specific post type posts data.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/geodir/v2/&lt;post_type_rest_base&gt;</h6>
	</div>
</div>

```shell
curl https://example.com//wp-json/geodir/v2/<post_type_rest_base>\
	-u consumer_key:consumer_secret
```
> JSON response example:

```json
[
    {
        "id": 197,
        "title": {
            "raw": "Please Touch Museum",
            "rendered": "Please Touch Museum"
        },
        "slug": "please-touch-museum",
        "link": "http://localhost:10005/places/united-states/pennsylvania/philadelphia/attractions/please-touch-museum/",
        "status": "publish",
        "type": "gd_place",
        "author": 1,
        "date": "2021-03-03T06:37:36",
        "date_gmt": "2021-03-03T06:37:36",
        "modified": "2022-07-29T02:56:03",
        "modified_gmt": "2022-07-29T02:56:03",
        "content": {
            "raw": "<h3>New Location!</h3>\r\nWho doesn´t love the Please Touch Museum? And now, taking kids to the Museum is better than ever. The nation´s premier children´s museum - which has been a beloved landmark since it opened in 1976 - has a new home in Fairmount Park, opening its doors to a world of educational, hands-on fun.\r\n\r\nThe new location in Memorial Hall - a National Historic Landmark built in 1876 for the Centennial Exhibition celebrating the country´s 100th birthday - will boast three times more space for exhibitions and programs.\r\n\r\nJust outside the museum, kids and adults will also delight in riding the meticulously restored 1908 Woodside Park Dentzel Carousel, built in Philadelphia for a now-defunct amusement park 10 blocks from Memorial Hall.\r\n\r\nVisit The Please Touch Museum for more info!\r\n<h3>The Experience</h3>\r\nThe city´s award-winning children´s museum is fun-filled, totally hands-on, and so delightful that adults are entertained, too. Each nook and cranny has a different theme - from the fantastic to the practical. In Alice´s Adventures in Wonderland, kids can play croquet with the Queen and sip tea with the Mad Hatter; nearby, oversized props bring Maurice Sendak´s classics to life.\r\n\r\nKids can take the wheel of a real bus and sail a boat on a mini-Delaware River; in “Nature´s Pond,” the youngest visitors (age 3 and under) can discover animals nestled among high grass and a lily pond, or enjoy stories and nursery rhymes in “Fairytale Garden.” Please Touch is also a first live theater experience for young children - Please Touch Playhouse performances are original and interactive and take place daily!\r\n\r\nPlease Touch Museum tends to be busier on rainy days. You may want to schedule your visit on fair weather days. Mornings are also a busy time with most school groups visiting during this time. Afternoons are a great time to visit the museum as well as Mondays when groups are not scheduled.\r\n<h3>History</h3>\r\nOne of the lasting museums from the tourist upgrade of Philadelphia that coincided with the 1976 Bicentennial celebration, Please Touch Museum® filled a gap in the city´s cultural scene. Other museums in the area certainly have sections for children, but Please Touch Museum´s new home not only offers three toddler areas, but also exciting exhibit components for older siblings (for ages 7 and up).\r\n<h3>Visiting Tips</h3>\r\nPlease Touch Museum tends to be busier on rainy days. You may want to schedule your visit on fair weather days. Mornings are also a busy time with most school groups visiting during this time. Afternoons are a great time to visit the museum as well as Mondays when groups are not scheduled.\r\n<h3>Insider Tip</h3>\r\nThe museum has a full schedule of craft activities and music, dance and storytelling performances, which are entertaining for both kids and adults.\r\n<h3>Great Kids’ Stuff</h3>\r\nIn The Supermarket, kids take control: They can stock the shelves, load their cart and ring up the order.\r\nBuy Tickets Online In Advance\r\n\r\nYou can buy admission tickets to the Please Touch Museum online through our partners at the Independence Visitor Center. Just click the button below.",
            "rendered": "<h3>New Location!</h3>\n<p>Who doesn´t love the Please Touch Museum? And now, taking kids to the Museum is better than ever. The nation´s premier children´s museum &#8211; which has been a beloved landmark since it opened in 1976 &#8211; has a new home in Fairmount Park, opening its doors to a world of educational, hands-on fun.</p>\n<p>The new location in Memorial Hall &#8211; a National Historic Landmark built in 1876 for the Centennial Exhibition celebrating the country´s 100th birthday &#8211; will boast three times more space for exhibitions and programs.</p>\n<p>Just outside the museum, kids and adults will also delight in riding the meticulously restored 1908 Woodside Park Dentzel Carousel, built in Philadelphia for a now-defunct amusement park 10 blocks from Memorial Hall.</p>\n<p>Visit The Please Touch Museum for more info!</p>\n<h3>The Experience</h3>\n<p>The city´s award-winning children´s museum is fun-filled, totally hands-on, and so delightful that adults are entertained, too. Each nook and cranny has a different theme &#8211; from the fantastic to the practical. In Alice´s Adventures in Wonderland, kids can play croquet with the Queen and sip tea with the Mad Hatter; nearby, oversized props bring Maurice Sendak´s classics to life.</p>\n<p>Kids can take the wheel of a real bus and sail a boat on a mini-Delaware River; in “Nature´s Pond,” the youngest visitors (age 3 and under) can discover animals nestled among high grass and a lily pond, or enjoy stories and nursery rhymes in “Fairytale Garden.” Please Touch is also a first live theater experience for young children &#8211; Please Touch Playhouse performances are original and interactive and take place daily!</p>\n<p>Please Touch Museum tends to be busier on rainy days. You may want to schedule your visit on fair weather days. Mornings are also a busy time with most school groups visiting during this time. Afternoons are a great time to visit the museum as well as Mondays when groups are not scheduled.</p>\n<h3>History</h3>\n<p>One of the lasting museums from the tourist upgrade of Philadelphia that coincided with the 1976 Bicentennial celebration, Please Touch Museum® filled a gap in the city´s cultural scene. Other museums in the area certainly have sections for children, but Please Touch Museum´s new home not only offers three toddler areas, but also exciting exhibit components for older siblings (for ages 7 and up).</p>\n<h3>Visiting Tips</h3>\n<p>Please Touch Museum tends to be busier on rainy days. You may want to schedule your visit on fair weather days. Mornings are also a busy time with most school groups visiting during this time. Afternoons are a great time to visit the museum as well as Mondays when groups are not scheduled.</p>\n<h3>Insider Tip</h3>\n<p>The museum has a full schedule of craft activities and music, dance and storytelling performances, which are entertaining for both kids and adults.</p>\n<h3>Great Kids’ Stuff</h3>\n<p>In The Supermarket, kids take control: They can stock the shelves, load their cart and ring up the order.<br />\nBuy Tickets Online In Advance</p>\n<p>You can buy admission tickets to the Please Touch Museum online through our partners at the Independence Visitor Center. Just click the button below.</p>\n",
            "protected": false
        },
        "default_category": "63",
        "post_category": [
            {
                "id": 63,
                "name": "Attractions",
                "slug": "attractions"
            },
            {
                "id": 69,
                "name": "Feature",
                "slug": "feature"
            }
        ],
        "post_tags": [
            {
                "id": 71,
                "name": "Sample Tags",
                "slug": "sample-tags"
            },
            {
                "id": 70,
                "name": "Tags",
                "slug": "tags"
            }
        ],
        "step_one": null,
        "step_two": null,
        "special_offers": "",
        "business_hours": {
            "raw": "[\"Mo 09:00-17:00\",\"Tu 09:00-17:00\",\"We 09:00-17:00\",\"Th 09:00-17:00\",\"Fr 09:00-17:00\"],[\"UTC\":\"-5\",\"Timezone\":\"America/New_York\"]",
            "rendered": {
                "days": {
                    "Mo": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Monday",
                        "day_short": "Mon",
                        "day_no": 1,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    540,
                                    1020
                                ],
                                "utc_minutes": [
                                    840,
                                    1320
                                ],
                                "utc_minutes_dst": [
                                    780,
                                    1260
                                ]
                            }
                        ]
                    },
                    "Tu": {
                        "today": 1,
                        "closed": 0,
                        "open": 0,
                        "day": "Tuesday",
                        "day_short": "Tue",
                        "day_no": 2,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    1980,
                                    2460
                                ],
                                "utc_minutes": [
                                    2280,
                                    2760
                                ],
                                "utc_minutes_dst": [
                                    2220,
                                    2700
                                ]
                            }
                        ]
                    },
                    "We": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Wednesday",
                        "day_short": "Wed",
                        "day_no": 3,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    3420,
                                    3900
                                ],
                                "utc_minutes": [
                                    3720,
                                    4200
                                ],
                                "utc_minutes_dst": [
                                    3660,
                                    4140
                                ]
                            }
                        ]
                    },
                    "Th": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Thursday",
                        "day_short": "Thu",
                        "day_no": 4,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    4860,
                                    5340
                                ],
                                "utc_minutes": [
                                    5160,
                                    5640
                                ],
                                "utc_minutes_dst": [
                                    5100,
                                    5580
                                ]
                            }
                        ]
                    },
                    "Fr": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Friday",
                        "day_short": "Fri",
                        "day_no": 5,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    6300,
                                    6780
                                ],
                                "utc_minutes": [
                                    6600,
                                    7080
                                ],
                                "utc_minutes_dst": [
                                    6540,
                                    7020
                                ]
                            }
                        ]
                    },
                    "Sa": {
                        "today": 0,
                        "closed": 1,
                        "open": 0,
                        "day": "Saturday",
                        "day_short": "Sat",
                        "day_no": 6,
                        "slots": [
                            {
                                "slot": null,
                                "range": "Closed",
                                "open": 0,
                                "time": [],
                                "minutes": []
                            }
                        ]
                    },
                    "Su": {
                        "today": 0,
                        "closed": 1,
                        "open": 0,
                        "day": "Sunday",
                        "day_short": "Sun",
                        "day_no": 7,
                        "slots": [
                            {
                                "slot": null,
                                "range": "Closed",
                                "open": 0,
                                "time": [],
                                "minutes": []
                            }
                        ]
                    }
                },
                "extra": {
                    "has_open": 0,
                    "has_closed": 0,
                    "today_range": "9:00 am - 5:00 pm",
                    "current_label": "Closed now",
                    "open_now_label": "Open now",
                    "closed_now_label": "Closed now",
                    "date": "2022-08-02",
                    "time": "06:38:57",
                    "full_date": "2022-08-02 06:38:57",
                    "date_format": "August 2, 2022",
                    "time_format": "6:38 am",
                    "full_date_format": "August 2, 2022 6:38 am",
                    "timezone_string": "America/New_York",
                    "offset": -18000,
                    "utc_offset": "-5",
                    "offset_dst": -14400,
                    "utc_offset_dst": "-4",
                    "has_dst": 1,
                    "is_dst": 1
                }
            }
        },
        "contact_information": null,
        "street": "1200 Sansom St",
        "country": "United States",
        "region": "Pennsylvania",
        "city": "Philadelphia",
        "zip": "19107",
        "latitude": "39.949757529995836",
        "longitude": "-75.1605083405838",
        "mapview": "ROADMAP",
        "mapzoom": "",
        "phone": "(222) 777-1111",
        "email": "info@pleasetouchmuseum.com",
        "website": "http://pleasetouchmuseum.com",
        "twitter": "http://twitter.com/pleasetouchmuseum",
        "facebook": "http://facebook.com/pleasetouchmuseum",
        "video": "",
        "price": "0.00",
        "property_status": {
            "raw": "For Sale",
            "rendered": "For Sale"
        },
        "property_furnishing": {
            "raw": "Unfurnished",
            "rendered": "Unfurnished"
        },
        "property_type": {
            "raw": "Detached house",
            "rendered": "Detached house"
        },
        "property_bedrooms": {
            "raw": "2",
            "rendered": "2"
        },
        "property_bathrooms": {
            "raw": "2",
            "rendered": "2"
        },
        "property_area": null,
        "property_features": {
            "raw": "",
            "rendered": []
        },
        "sale_status": {
            "raw": null,
            "rendered": "Select Status"
        },
        "asasas": "",
        "featured": false,
        "rating": "0",
        "rating_count": 0,
        "featured_media": 414,
        "featured_image": {
            "id": "102",
            "title": "",
            "src": "http://localhost:10005/wp-content/uploads/2022/07/2.png",
            "thumbnail": "http://localhost:10005/wp-content/uploads/2022/07/2-150x150.png",
            "width": 600,
            "height": 400
        },
        "images": [
            {
                "id": "102",
                "title": "",
                "src": "http://localhost:10005/wp-content/uploads/2022/07/2.png",
                "thumbnail": "http://localhost:10005/wp-content/uploads/2022/07/2-150x150.png",
                "featured": true,
                "position": "0"
            },
            {
                "id": "103",
                "title": "",
                "src": "http://localhost:10005/wp-content/uploads/2022/07/3.png",
                "thumbnail": "http://localhost:10005/wp-content/uploads/2022/07/3-150x150.png",
                "featured": false,
                "position": "1"
            },
            {
                "id": "104",
                "title": "",
                "src": "http://localhost:10005/wp-content/uploads/2022/07/4.png",
                "thumbnail": "http://localhost:10005/wp-content/uploads/2022/07/4-150x150.png",
                "featured": false,
                "position": "2"
            }
        ],
        "comment_status": "open",
        "ping_status": "closed",
        "meta": [],
        "guid": {
            "rendered": "http://localhost:10005/places/please-touch-museum/"
        },
        "_links": {
            "self": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/197"
                }
            ],
            "collection": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/places"
                }
            ],
            "about": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/types/gd_place"
                }
            ],
            "author": [
                {
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/wp/v2/users/1"
                }
            ],
            "replies": [
                {
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/geodir/v2/reviews?post=197"
                }
            ],
            "version-history": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/197/revisions"
                }
            ],
            "wp:featuredmedia": [
                {
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/wp/v2/media/414"
                }
            ],
            "wp:attachment": [
                {
                    "href": "http://localhost:10005/wp-json/wp/v2/media?parent=197"
                }
            ],
            "wp:term": [
                {
                    "taxonomy": "gd_place_tags",
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/tags?post=197"
                },
                {
                    "taxonomy": "gd_placecategory",
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/categories?post=197"
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
    },
    {
        "id": 195,
        "title": {
            "raw": "Franklin Square",
            "rendered": "Franklin Square"
        },
        "slug": "franklin-square",
        "link": "http://localhost:10005/places/united-states/pennsylvania/philadelphia/attractions/franklin-square/",
        "status": "publish",
        "type": "gd_place",
        "author": 1,
        "date": "2021-03-03T06:32:35",
        "date_gmt": "2021-03-03T06:32:35",
        "modified": "2021-03-03T06:32:35",
        "modified_gmt": "2021-03-03T06:32:35",
        "content": {
            "raw": " <h3> Location </h3>\n\t\t\n\t\t6th and Race Streets in Historic Philadelphia\n\t\t<h3>The Experience</h3>\n\t\t\n\t\tOne of Philadelphia&acute;s newest historic attractions is also one of its oldest.\n\t\t\n\t\tFranklin Square, one of the five public squares that William Penn laid out in his original plan for the city, has undergone a dramatic renovation.\n\t\t\n\t\tThe park now boasts several all new, family-friendly attractions, including a miniature golf course, a classic carousel, storytelling benches, a picnic area and more.\n\t\t\n\t\t<h3>Mini Golf </h3>\n\t\t\n\t\tAt Philly Mini Golf, an 18-hole miniature golf course decorated with some of Philadelphia&acute;s favorite icons, play a round of putt-putt and learn a little history at the same time.\n\t\t<h3>Carousel </h3>\n\t\t\n\t\tClose your eyes and take a nostalgic ride on the Philadelphia Park Liberty Carousel, a classic tribute to Philadelphia&acute;s great heritage of carousel-making. It&acute;s sure to be a instant kid favorite.\n\t\tStorytelling Benches\n\t\t\n\t\tThen catch up on your history at one of the storytelling benches located throughout the park, where you can hear tales of Franklin Square&acute;s past, or learn about the many communities touched by the Square, courtesy of the friendly storytellers of Once Upon a Nation.\n\t\t<h3>Fountain</h3>\n\t\t\n\t\tAnd emanating from the corners of the historic park, four new herringbone brick walking paths with nighttime lighting bring even more charm to the Square after dark. The paths lead to the centerpiece of the Square, the Franklin Square Fountain, a marble masterpiece built in 1838 surrounded by wrought iron fences, which is currently still going under cosmetic restoration.\n\t\t<h3>The History </h3>\n\t\t\n\t\tOriginally named “North East Publick Square,” the 7.5-acre green is one of five original squares that William Penn laid out in his original plan of the city in 1682. The Square was renamed in honor of Benjamin Franklin in 1825.\n\t\t\n\t\tOver the years, the area has been used as a cattle pasture, a horse and cattle market, a burial ground, a drill and parade ground for the American military during the War of 1812 and, finally, a city park.\n\t\t\n\t\tIn 1837, the city made Franklin Square into a public park and an elegant fountain was constructed in its center, a fountain thought to be the oldest surviving fountain in William Penn&acute;s five historic squares. The others are Rittenhouse, Washington, Logan and Center Square, where City Hall is now located.\n\t\t<h3>SquareBurger </h3>\n\t\t\n\t\tJust in time for summer, Franklin Square has opened SquareBurger, a Stephen Starr-run “burger shack” selling summer staples: hot dogs, fries, milkshakes (made with Tasty Kakes) and, of course, hamburgers and cheeseburgers.\n\t\t\n\t\tSquareBurger is open until October - perfect for a couple bites between rounds of miniature golf!",
            "rendered": "<br />\n<h3> Location </h3>\n<p>\t\t6th and Race Streets in Historic Philadelphia</p>\n<h3>The Experience</h3>\n<p>\t\tOne of Philadelphia&acute;s newest historic attractions is also one of its oldest.</p>\n<p>\t\tFranklin Square, one of the five public squares that William Penn laid out in his original plan for the city, has undergone a dramatic renovation.</p>\n<p>\t\tThe park now boasts several all new, family-friendly attractions, including a miniature golf course, a classic carousel, storytelling benches, a picnic area and more.</p>\n<h3>Mini Golf </h3>\n<p>\t\tAt Philly Mini Golf, an 18-hole miniature golf course decorated with some of Philadelphia&acute;s favorite icons, play a round of putt-putt and learn a little history at the same time.</p>\n<h3>Carousel </h3>\n<p>\t\tClose your eyes and take a nostalgic ride on the Philadelphia Park Liberty Carousel, a classic tribute to Philadelphia&acute;s great heritage of carousel-making. It&acute;s sure to be a instant kid favorite.<br />\n\t\tStorytelling Benches</p>\n<p>\t\tThen catch up on your history at one of the storytelling benches located throughout the park, where you can hear tales of Franklin Square&acute;s past, or learn about the many communities touched by the Square, courtesy of the friendly storytellers of Once Upon a Nation.</p>\n<h3>Fountain</h3>\n<p>\t\tAnd emanating from the corners of the historic park, four new herringbone brick walking paths with nighttime lighting bring even more charm to the Square after dark. The paths lead to the centerpiece of the Square, the Franklin Square Fountain, a marble masterpiece built in 1838 surrounded by wrought iron fences, which is currently still going under cosmetic restoration.</p>\n<h3>The History </h3>\n<p>\t\tOriginally named “North East Publick Square,” the 7.5-acre green is one of five original squares that William Penn laid out in his original plan of the city in 1682. The Square was renamed in honor of Benjamin Franklin in 1825.</p>\n<p>\t\tOver the years, the area has been used as a cattle pasture, a horse and cattle market, a burial ground, a drill and parade ground for the American military during the War of 1812 and, finally, a city park.</p>\n<p>\t\tIn 1837, the city made Franklin Square into a public park and an elegant fountain was constructed in its center, a fountain thought to be the oldest surviving fountain in William Penn&acute;s five historic squares. The others are Rittenhouse, Washington, Logan and Center Square, where City Hall is now located.</p>\n<h3>SquareBurger </h3>\n<p>\t\tJust in time for summer, Franklin Square has opened SquareBurger, a Stephen Starr-run “burger shack” selling summer staples: hot dogs, fries, milkshakes (made with Tasty Kakes) and, of course, hamburgers and cheeseburgers.</p>\n<p>\t\tSquareBurger is open until October &#8211; perfect for a couple bites between rounds of miniature golf!</p>\n",
            "protected": false
        },
        "default_category": "63",
        "post_category": [
            {
                "id": 63,
                "name": "Attractions",
                "slug": "attractions"
            },
            {
                "id": 69,
                "name": "Feature",
                "slug": "feature"
            }
        ],
        "post_tags": [
            {
                "id": 71,
                "name": "Sample Tags",
                "slug": "sample-tags"
            },
            {
                "id": 70,
                "name": "Tags",
                "slug": "tags"
            }
        ],
        "step_one": null,
        "step_two": null,
        "special_offers": null,
        "business_hours": {
            "raw": "[\"Mo 09:00-17:00\",\"Tu 09:00-17:00\",\"We 09:00-17:00\",\"Th 09:00-17:00\",\"Fr 09:00-17:00\"],[\"UTC\":\"+0\",\"Timezone\":\"UTC\"]",
            "rendered": {
                "days": {
                    "Mo": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Monday",
                        "day_short": "Mon",
                        "day_no": 1,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    540,
                                    1020
                                ]
                            }
                        ]
                    },
                    "Tu": {
                        "today": 1,
                        "closed": 0,
                        "open": 0,
                        "day": "Tuesday",
                        "day_short": "Tue",
                        "day_no": 2,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    1980,
                                    2460
                                ]
                            }
                        ]
                    },
                    "We": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Wednesday",
                        "day_short": "Wed",
                        "day_no": 3,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    3420,
                                    3900
                                ]
                            }
                        ]
                    },
                    "Th": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Thursday",
                        "day_short": "Thu",
                        "day_no": 4,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    4860,
                                    5340
                                ]
                            }
                        ]
                    },
                    "Fr": {
                        "today": 0,
                        "closed": 0,
                        "open": 0,
                        "day": "Friday",
                        "day_short": "Fri",
                        "day_no": 5,
                        "slots": [
                            {
                                "slot": "09:00-17:00",
                                "range": "9:00 am - 5:00 pm",
                                "open": 0,
                                "time": [
                                    "0900",
                                    "1700"
                                ],
                                "minutes": [
                                    6300,
                                    6780
                                ]
                            }
                        ]
                    },
                    "Sa": {
                        "today": 0,
                        "closed": 1,
                        "open": 0,
                        "day": "Saturday",
                        "day_short": "Sat",
                        "day_no": 6,
                        "slots": [
                            {
                                "slot": null,
                                "range": "Closed",
                                "open": 0,
                                "time": [],
                                "minutes": []
                            }
                        ]
                    },
                    "Su": {
                        "today": 0,
                        "closed": 1,
                        "open": 0,
                        "day": "Sunday",
                        "day_short": "Sun",
                        "day_no": 7,
                        "slots": [
                            {
                                "slot": null,
                                "range": "Closed",
                                "open": 0,
                                "time": [],
                                "minutes": []
                            }
                        ]
                    }
                },
                "extra": {
                    "has_open": 0,
                    "has_closed": 0,
                    "today_range": "9:00 am - 5:00 pm",
                    "current_label": "Closed now",
                    "open_now_label": "Open now",
                    "closed_now_label": "Closed now",
                    "date": "2022-08-02",
                    "time": "06:38:57",
                    "full_date": "2022-08-02 06:38:57",
                    "date_format": "August 2, 2022",
                    "time_format": "6:38 am",
                    "full_date_format": "August 2, 2022 6:38 am",
                    "timezone_string": "UTC",
                    "offset": 0,
                    "utc_offset": "+0",
                    "offset_dst": 0,
                    "utc_offset_dst": "+0",
                    "has_dst": 0,
                    "is_dst": 0
                }
            }
        },
        "contact_information": null,
        "street": "210, Massachusetts Avenue, Erlton-Ellisburg",
        "country": "United States",
        "region": "Pennsylvania",
        "city": "Philadelphia",
        "zip": "08002",
        "latitude": "39.920996451631",
        "longitude": "-75.016184453886",
        "mapview": null,
        "mapzoom": null,
        "phone": "(111) 677-4444",
        "email": "info@franklinsq.com",
        "website": "http://franklinsquare.com",
        "twitter": "http://twitter.com/franklinsquare",
        "facebook": "http://facebook.com/franklinsquare",
        "video": "",
        "price": null,
        "property_status": {
            "raw": null,
            "rendered": "Select Status"
        },
        "property_furnishing": {
            "raw": null,
            "rendered": "Select Status"
        },
        "property_type": {
            "raw": null,
            "rendered": "Select Type"
        },
        "property_bedrooms": {
            "raw": null,
            "rendered": "Select Bedrooms"
        },
        "property_bathrooms": {
            "raw": null,
            "rendered": "Select Bathrooms"
        },
        "property_area": null,
        "property_features": {
            "raw": null,
            "rendered": []
        },
        "sale_status": {
            "raw": null,
            "rendered": "Select Status"
        },
        "asasas": null,
        "featured": false,
        "rating": "0",
        "rating_count": 0,
        "featured_media": 0,
        "featured_image": {
            "id": 0,
            "title": "website screenshot",
            "src": "https://s.wordpress.com/mshots/v1/http%3A%2F%2Ffranklinsquare.com?w=825&h=430",
            "thumbnail": "https://s.wordpress.com/mshots/v1/http%3A%2F%2Ffranklinsquare.com?w=825&h=430",
            "width": "",
            "height": ""
        },
        "images": [
            {
                "id": 0,
                "title": "website screenshot",
                "src": "https://s.wordpress.com/mshots/v1/http%3A%2F%2Ffranklinsquare.com?w=825&h=430",
                "thumbnail": "https://s.wordpress.com/mshots/v1/http%3A%2F%2Ffranklinsquare.com?w=825&h=430",
                "featured": false,
                "position": 0
            }
        ],
        "comment_status": "open",
        "ping_status": "closed",
        "meta": [],
        "guid": {
            "rendered": "http://localhost:10005/places/franklin-square/"
        },
        "_links": {
            "self": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/195"
                }
            ],
            "collection": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/places"
                }
            ],
            "about": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/types/gd_place"
                }
            ],
            "author": [
                {
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/wp/v2/users/1"
                }
            ],
            "replies": [
                {
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/geodir/v2/reviews?post=195"
                }
            ],
            "version-history": [
                {
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/195/revisions"
                }
            ],
            "wp:attachment": [
                {
                    "href": "http://localhost:10005/wp-json/wp/v2/media?parent=195"
                }
            ],
            "wp:term": [
                {
                    "taxonomy": "gd_place_tags",
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/tags?post=195"
                },
                {
                    "taxonomy": "gd_placecategory",
                    "embeddable": true,
                    "href": "http://localhost:10005/wp-json/geodir/v2/places/categories?post=195"
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
]
```

## Create Post ##

## Update Post ##