# Authentication #

Geodirectory includes two ways to authenticate with the WP REST API. It is also possible to authenticate using any [WP REST API authentication](http://v3.wp-api.org/guide/authentication/) plugin or method.

## REST API keys ##

Pre-generated keys can be used to authenticate use of the REST API endpoints. New keys can be generated either through the WordPress admin interface or they can be auto-generated through an endpoint.

### Generating API keys in the WordPress admin interface ###

To create or manage keys for a specific WordPress user, go to Geodirectory > Settings > API > Keys.

![Geodirectory REST API keys settings](images/geodirectory-api-keys-settings.png)

Click the "Create an API Key" button. In the next screen, add a description and select the WordPress user you would like to generate the key for. Use of the REST API with the generated keys will conform to that user's WordPress roles and capabilities.

Choose the level of access for this REST API key, which can be _Read_ access, _Write_ access or _Read/Write_ access. Then click the "Generate API Key" button and Geodirectory will generate REST API keys for the selected user.

![Creating a new REST API key](images/geodirectory-creating-api-keys.png)

Now that keys have been generated, you should see two new keys, a QRCode, and a Revoke API Key button. These two keys are your Consumer Key and Consumer Secret.

![Generated REST API key](images/geodirectory-api-key-generated.png)

If the WordPress user associated with an API key is deleted, the API key will cease to function. API keys are not transferred to other users.

### Auto generating API keys using our Application Authentication Endpoint ###

This endpoint can be used by any APP to *allow users to generate API keys* for your APP. This makes integration with Geodirectory API easier because the user only needs to grant access to your APP via a URL. After being redirected back to your APP, the API keys will be sent back in a separate POST request.


<aside class="warning">
	This endpoint works exclusively for users to generate API keys and facilitate integration between the Geodirectory REST API and an application. In no way is this endpoint intended to be used as login method for customers.
</aside>

#### URL parameters ####

|   Parameter    |  Type  |                                                                                  Description                                                                                  |
|----------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `app_name`     | string | Your APP name <i class="label label-info">mandatory</i>                                                                                                                       |
| `scope`        | string | Level of access. Available: `read`, `write` and `read_write` <i class="label label-info">mandatory</i>                                                                        |
| `user_id`      | string | User ID in your APP. For your internal reference, used when the user is redirected back to your APP. NOT THE USER ID IN GEODIRECTORY <i class="label label-info">mandatory</i> |
| `return_url`   | string | URL the user will be redirected to after authentication <i class="label label-info">mandatory</i>                                                                             |
| `callback_url` | string | URL that will receive the generated API key. Note: this URL should be over **HTTPS** <i class="label label-info">mandatory</i>                                                |


### OAuth tips ###

* The OAuth parameters may be added as query string parameters or included in the Authorization header.
* Note there is no reliable cross-platform way to get the raw request headers in WordPress, so query string should be more reliable in some cases.
* The required parameters are: `oauth_consumer_key`, `oauth_timestamp`, `oauth_nonce`, `oauth_signature`, and `oauth_signature_method`. `oauth_version` is not required and should be omitted.
* The OAuth nonce can be any randomly generated 32 character (recommended) string that is unique to the consumer key.
* The OAuth timestamp should be the unix timestamp at the time of the request. The REST API will deny any requests that include a timestamp outside of a 15 minute window to prevent replay attacks.
* You must use the store URL provided by the index when forming the base string used for the signature, as this is what the server will use. (e.g. if the store URL includes a `www` sub-domain, you should use it for requests)
* Note that the request body is *not* signed as per the OAuth spec.
* If including parameters in your request, it saves a lot of trouble if you can order your items alphabetically.
