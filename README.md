# ZainCash-Integration
- PHP v1
- ASP.NET
- Magento
- Opencart for v1
- Opencart for v2
- Wordpress (WooCommerce)
- Wordpress (EasyDigitalDownloads)

# Credentials
- You will need the following credentials which you can get by contacting ZainCash:

Msisdn: 96478XXXXXXXX

Merchant Id: XXXXXXXXXXXXXXXX

Secret: XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

- The server used for development is https://test.zaincash.iq/

The request.php and redirect.php both are in your server, so the redirection URL will be created upon your server/ domain and according to where you will put your file/ code that will get the token from our end to check the status of the payment and complete any other process you need.
To make it clearer here is the payment steps:

You will create a token according to your merchant and secret (its a JWT tokens you can find the way in the files attached).

You will set the token data for every payment which:

- The amount of money (a number in IQD and it should be more than 250).

- The service Type (a string, any string from your side prefer to be your website name).

- The MSISDN (a string has your wallet number).

- The orderId (string or number, it refers to an id in your system, you will get this id in the redirecting so you can check the status of the operation).

- The redirectUrl (a string of a URL in your system/ server that has the redirect.php file so ZainCash redirects to it after finishing from his side).

- The iat & exp are the expiry time for the token, please leave it as it is.

You will set your redirect RUL ie: example.com/somthing/redirect.php.

You will get the status of the operation by checking the redirected token.

You can find in that token:

- The status (’success’ or ‘fail’) to inform you that the payment completed or not.

- The orderId (the same orderId you’ve sent, this can help you track your payments and closing your orders)

- The id is the transaction id from ZainCash side, it’s recommended to save this one inside your system/ DB you can know which payment is for whom).

- The iat & exp you can ignore this two if you like.
