# REST API: GET emailings (Publisher)

A method to request a list of all mailings sent from Publisher. 
This is an HTTP GET call to the following address:

`https://api.copernica.com/v2/publisher/emailings?access=token=xxxx`

You can find all the call to retrieve all Marketing Suite emailings [here](./rest-get-ms-emailings).

## Available parameters

* **type**: The type of mailing between mass or individual, defaults to both.
* **followups**: Indicates if we only use follow-up mailings ("yes"), only mailings 
that were *not* the result of a follow-up ("no") or all mailings ("both"). Defaults to "both".
* **test**: Indicates if we only use test mailings ("yes"), only mailings 
that were *not* a test ("no") or all mailings ("both"). Defaults to "both".
* **mindestinations**: Only retrieve mailings at least this many destinations.
* **maxdestinations**: Only retrieve mailings with at most this many destinations.
* **fromdate**: Only retrieve mailings sent after this date.
* **todate**: Only retrieve mailings sent before this date.

This method also supports [paging parameters](./rest-paging).

## Returned fields

The method returns a JSON array containing the start index, limit and 
count. It also contains a data array with the mailings matching the 
given parameters. For each mailing we return the following:

* **id**: ID of the mailing
* **timestamp**: Timestamp of the mailing
* **destinations**: Amount of destinations the mailing was sent to
* **type**: Type of mailing (individual or mass)
* **document**: The ID of the document used for the mailing.
* **template**: The ID of the template used for the mailing.
* **clicks**: The total amount of clicks that this mailing received.
* **impressions**: The total amount of impressions that this mailing received.
* **contenttype**: Type of mailing content
* **target**: Contains the target type and the ID and type of other 
entities above it (for example the database a collection belongs to)

## PHP Example

The following script demonstrates how to use this method. Because we use the 
CopernicaRestApi class, you don't have to worry about escaping special characters 
in the URL; it is done automatically.

```php
// dependencies
require_once('copernica_rest_api.php');

// change this into your access token
$api = new CopernicaRestAPI("your-access-token", 2);

// parameters to pass to the call
$parameters = array(
    'limit'             => 10,
    'type'              => 'mass',
    'followups'         => 'no',
    'registerclicks'    => 'yes',
);

// do the call, and print result
print_r($api->get("publisher/emailings", $parameters));
```

The example above requires the [CopernicaRestApi class](./rest-php).

## More information

* [Overview of all API calls](./rest-api)
* [Get Marketing Suite mailings](./rest-get-ms-emailings)