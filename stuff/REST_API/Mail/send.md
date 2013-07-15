mail/send
===

Send a mail using our service.

Parameters:

 * `from` - can be string (email address) or associative array with its key as name and its value as email address
 * `to` - can be string (email address) or associative array with its key as name and its value as email address (if you send email to multiple candidates here can be multiple rows in array)
 * `cc` - can be string (email address) or associative array with its key as name and its value as email address (if you send email to multiple candidates here can be multiple rows in array)
 * `bcc - can be string (email address) or associative array with its key as name and its value as email address (if you send email to multiple candidates here can be multiple rows in array)
 * `subject` - subject of email
 * `body` - email body, can be in html format
 * `attachment - email attachment. Associative array, contains 2 fields: `name` and `body`. `name` - file name. `body` - base64 encoded data of file.

Example:

```
\WU_API::apiCall('mail/send', array(
    'from' => array( 'Vitaly Dyatlov' => 'vitaly@wutalent.co.uk' ),
    'to' => array( 'Steve Walker' => 'steve@idibu.com' ),
    'cc' => array( 'Vitaly Dyatlov' => 'vitaly@idibu.com' ),
    'subject' => 'Email Example',
    'body' => 'body of email',
    'attachment' => array(
        'name' => 'example.txt',
        'body' => base64_encode( 'file content goes here and should be base64 encoded' )
    )
));
```