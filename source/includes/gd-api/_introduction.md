# Introduction #

Geodirectory is fully integrated with the WordPress [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer) API. This allows Geodirectory data to be created, read, updated, and deleted using requests in JSON format and using WordPress REST API Authentication methods and standard HTTP verbs which are understood by most HTTP clients.

## Requirements ##

To use the Geodirectory REST API you must be using:

* Geodirectory V2.
* WordPress 4.4+.
* You may access the API over either HTTP or HTTPS, but *HTTPS is recommended where possible*.

<aside class="notice">
	Please note that you are <strong>not</strong> required to install the <a href="https://wordpress.org/plugins/rest-api/" target="_blank">WP REST API (WP API)</a> plugin.
</aside>

## Request/Response Format ##

The default response format is JSON. Requests with a message-body use plain JSON to set or update resource attributes. Successful requests will return a `200 OK` HTTP status.

Some general information about responses:

* Dates are returned in ISO8601 format: `YYYY-MM-DDTHH:MM:SS`
* Resource IDs are returned as integers.
* Any decimal monetary amount, such as prices or totals, will be returned as strings with two decimal places.
* Other amounts, such as item counts, are returned as integers.
* Blank fields are generally included as `null` or emtpy string instead of being omitted.


## Errors ##

Occasionally you might encounter errors when accessing the REST API. There are four possible types:

| Error Code                  | Error Type                                                  |
|-----------------------------|-------------------------------------------------------------|
| `400 Bad Request`           | Invalid request, e.g. using an unsupported HTTP method      |
| `401 Unauthorized`          | Authentication or permission error, e.g. incorrect API keys |
| `404 Not Found`             | Requests to resources that don't exist or are missing       |
| `500 Internal Server Error` | Server error                                                |

> Geodirectory error example:

```json
{
  "code": "rest_no_route",
  "message": "No route was found matching the URL and request method",
  "data": {
    "status": 404
  }
}
```

Errors return both an appropriate HTTP status code and response object which contains a `code`, `message` and `data` attribute.

## Parameters ##

Almost all endpoints accept optional parameters which can be passed as a HTTP query string parameter, e.g. `GET /wp-json/geodir/v2/markers/?post_type=gd_place`. All parameters are documented along each endpoint.

## Pagination ##

Requests that return multiple items will be paginated to 10 items by default. This default can be changed by the site administrator by changing the `posts_per_page` option. Alternatively the items per page can be specified with the `?per_page` parameter:

`GET /geodir/v2/places?per_page=15`

You can specify further pages with the `?page` parameter:

`GET /geodir/v2/places?page=2`

You may also specify the offset from the first resource using the `?offset` parameter:

`GET /geodir/v2/places?offset=5`

Page number is 1-based and omitting the `?page` parameter will return the first page.

The total number of resources and pages are always included in the `X-WP-Total` and `X-WP-TotalPages` HTTP headers.

### Tools ###

Some useful tools you can use to access the API include:

- [Insomnia](https://insomnia.rest) - Cross-platform GraphQL and REST client, available for Mac, Windows, and Linux.
- [Postman](https://www.getpostman.com/) - Cross-platform REST client, available for Mac, Windows, and Linux.
- [RequestBin](https://requestbin.com) - Allows you test webhooks.
- [Hookbin](https://hookbin.com/) - Another tool to test webhooks.

## Learn more ##

Learn more about the REST API checking the <a href="https://developer.wordpress.org/rest-api/">official WordPress REST API documentation</a>.
