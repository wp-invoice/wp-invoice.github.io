---
title: WP Invoice API
sidebar_title: API
permalink: /docs/api/
---

XML-RPC based API for interacting with the internal WP-Invoice API.

Original WordPress XML-RPC API (http://codex.wordpress.org/XML-RPC_WordPress_API)

Extending (http://codex.wordpress.org/XML-RPC_Extending)

***

### XML-RPC Method

There is a single XML-RPC method **`wp.invoice`** which is in fact used as something like NAMESPACE. Three different arguments should be passed during request to this method in following order:

1. Internal Method Name
2. Credentials
3. Internal Method Arguments

***

### Internal Methods

Current API is new and we are going to add new methods for some time.

##### Create Invoice
Allows to create invoices from the information passed.

Method: `create_invoice`

##### Get Invoice
Returns invoice object by passed ID.

Method: `get_invoice`

##### Delete Invoice
Deletes invoice object by passed ID and returns boolean.

Method: `delete_invoice`

##### Refund Invoice
Refund invoice by ID. Note that it does not do refund on merchant side.

Method: `refund_invoice`

##### Pay Invoice
Pay invoice by ID

Method: `pay_invoice`

##### Update Invoice
Update some of the invoice attributes.

Method: `update_invoice`

***

### Credentials

Credentials are simply WordPress login and password of WordPress user.

***

### Internal Method Arguments

It is the third argument that should contain an Associative Array of parameters. It varies depending on methods. Detailed lists of arguments you can find in WP-Invoice installation. Settings->Help->WP-Invoice XML-RPC API Reference. 

***

### Examples

**Creating an invoice**

    include_once( ABSPATH . WPINC . '/class-IXR.php' );
    include_once( ABSPATH . WPINC . '/class-wp-http-ixr-client.php' );

    $client = new WP_HTTP_IXR_Client( 'http://example.site.com/xmlrpc.php' );

    $client->query('wp.invoice', array(
      $method = 'create_invoice',
      $credentials = array('xmlrpc-user', 'password'),
      $args = array(
          'subject'     => 'Test API Invoice',
          'description' => 'Invoice descriptive information.',
          'type'        => 'invoice',
          'user_data'   => array(
              'user_email' => 'recipient@email.com',
              'first_name' => 'John',
              'last_name'  => 'Smith'
          ),
          'deposit'     => 15.99,
          'due_date'    => array(
              'month' => '09',
              'day'   => '10',
              'year'  => '2013'
          ),
          'currency'    => 'USD',
          'tax'         => 10.5,
          'tax_method'  => 'after_discount',
          'status'      => 'active',
          'discount'  => array(
              'name'   => 'Your Discount',
              'type'   => 'amount',
              'amount' => 1.20
          ),
          'items' => array(
              array(
                  'name' => 'Test item 1',
                  'description' => 'Item 1 description',
                  'quantity' => 2,
                  'price' => 2.65,
                  'tax_rate' => 1 //global 'tax' will be used in order to priority
              ),
              array(
                  'name' => 'Test item 2',
                  'description' => 'Item 2 description',
                  'quantity' => 4,
                  'price' => 3.85
              )
          ),
          'charges' => array(
              array(
                  'name' => 'Fee 1',
                  'amount' => 0.56
              ),
              array(
                  'name' => 'Fee 2',
                  'amount' => 0.99,
                  'tax' => 15 //global 'tax' will be used in order to priority
              )
          )
      )
    ));

    $new_invoice = $client->getResponse();

**Getting an invoice**

    include_once( ABSPATH . WPINC . '/class-IXR.php' );
    include_once( ABSPATH . WPINC . '/class-wp-http-ixr-client.php' );

    $client = new WP_HTTP_IXR_Client( 'http://example.site.com/xmlrpc.php' );

    $client->query('wp.invoice', array(
        $method = 'get_invoice',
        $credentials = array('xmlrpc-user', 'password'),
        $args = array(
            'ID' => 43508300
        )
    ));

    $the_invoice = $client->getResponse();

**Deleting an invoice**

    include_once( ABSPATH . WPINC . '/class-IXR.php' );
    include_once( ABSPATH . WPINC . '/class-wp-http-ixr-client.php' );

    $client = new WP_HTTP_IXR_Client( 'http://example.site.com/xmlrpc.php' );

    $client->query('wp.invoice', array(
        $method = 'delete_invoice',
        $credentials = array('xmlrpc-user', 'password'),
        $args = array(
            'ID' => 43508300
        )
    ));

    if ( $client->getResponse() ) {
      echo 'Invoice has been deleted';
    } else {
      echo 'Cannot delete invoice';
    }