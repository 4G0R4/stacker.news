To attach CLNRest as an receiving wallet protocol, you'll need a rune and the cert.

# host and port

`cln:3010`

# host and port (onion)

Run:

```bash
sndev onion cln
```

# create rune

```bash
sndev cli cln --regtest createrune restrictions='["method=invoice"]'
```

# get cert

This is static in dev env so you can use this one:

```bash
LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tDQpNSUlCY2pDQ0FSaWdBd0lCQWdJSkFOclN2UFovWTNLRU1Bb0dDQ3FHU000OUJBTUNNQll4RkRBU0JnTlZCQU1NDQpDMk5zYmlCU2IyOTBJRU5CTUNBWERUYzFNREV3TVRBd01EQXdNRm9ZRHpRd09UWXdNVEF4TURBd01EQXdXakFXDQpNUlF3RWdZRFZRUUREQXRqYkc0Z1VtOXZkQ0JEUVRCWk1CTUdCeXFHU000OUFnRUdDQ3FHU000OUF3RUhBMElBDQpCQmptYUh1dWxjZ3dTR09ubExBSFlRbFBTUXdHWEROSld5ZnpWclY5aFRGYUJSZFFrMVl1Y3VqVFE5QXFybkVJDQpyRmR6MS9PeisyWFhENmdBMnhPbmIrNmpUVEJMTUJrR0ExVWRFUVFTTUJDQ0EyTnNib0lKYkc5allXeG9iM04wDQpNQjBHQTFVZERnUVdCQlNFY21OLzlyelMyaFI2RzdFSWdzWCs1MU4wQ2pBUEJnTlZIUk1CQWY4RUJUQURBUUgvDQpNQW9HQ0NxR1NNNDlCQU1DQTBnQU1FVUNJSENlUHZOU3Z5aUJZYXdxS2dRcXV3OUoyV1Z5SnhuMk1JWUlxejlTDQpRTDE4QWlFQWg4QlZEejhwWDdOc2xsOHNiMGJPMFJaNDljdnFRb2NDZ1ZhYnFKdVN1aWs9DQotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0tDQo=
```

Which is generated with the following command

```bash
openssl base64 -A -in docker/cln/ca.pem
```