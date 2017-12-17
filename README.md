# asktoniauthentication
Authenticating and Authorizing life changing food recommendations

Approach
--------
Using dotnet core Identity template, configured to use Postgre SQL as DB
OOTB template is augmented by IdentityServer open source project

## Build setup
```
# Note:
Need to request user-secrets from repo owners to connect to databases

# Check to see if Secret Manager is working
dotnet user-secrets -h

# Add user secrets
dotnet user-secrets set MySecret ValueOfMySecret

# Build code
dotnet build

# Run project
dotnet run

```

## Endpoint

The auth endpoint is live at:
[http://asktoniauthentication.azurewebsites.net](http://asktoniauthentication.azurewebsites.net)