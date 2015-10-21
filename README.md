OAuth Redirect
--------------

A simple shim to use an OAauth 2 service and redirect into a development environment.

For example, Dropbox's API requires the endpoint be at either 127.0.0.1 or an HTTPS address.
Neither may be feasible for some dev/staging/uat situations.

In those cases, this Github Pages url can be used as the App endpoint.
Pass an additional parameter to the API called "oauth-redirect" and that will become the new endpoint at runtime.
