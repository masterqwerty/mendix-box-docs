# Get Token Service Account \*\*BROKEN\*\*

This activity is completely broken. The implementation isn't done correctly, since it doesn't build the JWT the correct way. In particular, the encryption method used to sign the JWT is not one supported by the Box API, namely `HS256`. Then in the JWT header, it says the encryption method used is `RS256`. The supported algorithms are `RS256`, `RS384`, and `RS512`. The workaround I have requires an entirely new microflow, and it requires the JWT mendix module, so make sure you have that installed.

## New Microflow Implementation

This microflow will build the JWT from scratch, and request an access token through the Box API.