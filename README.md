# local-info
A simple apigee proxy which fetches the local data using city name.
use "http://ilyasshah3-eval-test.apigee.net/v1/city" in browser or in
some request client and pass "cityname" as query param. The proxy returns
the data in "json" format.
This proxy uses oauthV2 authentication mechanism, so in order to access this
proxy, you need to register your app with this proxy and after registering app
you will recieve "client-id" and "client-secret" keys which will be used to
get access token from the oauth proxy.
https://ilyasshah3-eval-test.apigee.net/oauth/client_credential/accesstoken?grant_type=client_credentials
Use the above proxy to get the access token using client id and client secret, Pass the base64  encoded
version of "client-id":"client-secret" as basic authentication header and also send the
"grant_type" parameter in the request query params or in the request body.
Remember to pass the recieved access token as the bearer Authorization header.
