# OAuth Redirect

A tiny shim to redirect an OAauth callback to a dynamic URI
Intentionally kept simple and transparent for peace of mind.

## Example use case:

Dropbox's API requires the "Redirect URI" be inserted manually, 
and the result must be at either 127.0.0.1 or an HTTPS address.
This may not be feasible for some environments or when distributing examples.

## Usage:

  1. Add the "Redirect URI" to your OAuth app: https://heathdutton.github.io/oauth-redirect/redirect
  2. When making an OAuth authentication request ensure your code specifies the same redirect URI if needed.
  3. Include an extra GET param in the "URL State" of authentication requests. It should be "oauth-redirect=<dynamic redirect uri>" where <dynamic redirect uri> is the endpoint in your project that will accept incomming authentication tokens.

Note: For obvious reasons POST is not supported here.
