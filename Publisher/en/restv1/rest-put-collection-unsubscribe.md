# REST API: PUT collection unsubscribe

Warning: You are viewing the documentation for the old REST API. We recommend 
using [version 2](../restv2/rest-api.md) of the REST API.

For every collection you may also set the unsubscribe settings separately. 
When Copernica’s servers receive an unsubscription the unsubscribe 
behaviour determines what happens with the profile: should it be edited 
or removed?

To set this algorithm using an API call, make an HTTP PUT request to the 
following URL:

`https://api.copernica.com/v1/collection/$id/unsubscribe?access_token=xxxx`

In this, the variable `$id` has to be replaced by the numerical identifier 
of the collection you wish to set the unsubscribe behaviour for. The 
new setting should be added to the body of the HTTP request.

## Available data

The following variables must be put into the body of the request:

- **behavior**: the setting itself
- **fields**: the new profile setting (only applicable if ‘behavior’ is 
set to ‘update’)

‘behavior’ has three possible values: 'nothing', 'remove' and 'update'. 
'Nothing' means unsubscriptions are simply ignored, 'remove' deletes 
unsubscribers and 'update' can be used to change a property of the 
profile such that you can keep the information while respecting their 
wish not to receive more email.

## PHP example

The following PHP script demonstrates how to use the method. In this 
example, when somebody unsubscribes, the field ‘newsletter’ is set to ‘no’.

```php
// dependencies
require_once('copernica-rest-api.php');

// change this into your access token
$api = new CopernicaRestApi("your-access-token");

// declare the id of the collection that you want to edit
$id = 1;

// data to be sent to the api
$data = array(
    'behavior'      =>  'update',
    'fields'        =>  array('newsletter' => 'no')
);

// do the call
$api->put("collection/{$id}/unsubscribe", $data);
```

The example above requires the [CopernicaRestApi class](rest-php).

## More information

- [Overview of all API method](rest-api)
- [GET collection unsubscribe](rest-get-collection-unsubscribe)
