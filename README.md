# asktoniauthentication
Authenticating and Authorizing life changing food recommendations

Approach
--------
Using dotnet core Identity template, configured to use Postgre SQL as DB
OOTB template is augmented by IdentityServer open source project

## Client
The sample client that I have been using to test out the flow is under "AskToniAuthJavaScriptClient"

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

## Hosting
The identity server app is hosted in Azure.

## Database
The identity server is configured to use PostgreSQL. The database can queried using PGadmin in both development and prod.
### Connection details
The connection string is provided as a key-value pair with:

key = "DbConnectStr"

connectionstring = in format: "User ID={UserName};Password={Password};Host={Host};Port={Port};Database={DB Name};Pooling=true;
And add "Use SSL Stream=True;SSL Mode=Require;TrustServerCertificate=True;" for heroku

### Credentials in development environment
These are dependant on your local installation of PostgreSQL. They should be stored in your dotnet user-secrets, the 
### Credentials in production environment
The production database is hosted in Heroku Postgre. The credentials to log in to the database can be obtained by logging in to the Heroku web portal. -> Ask John for Credentials

### Database Schema
#### AspNetUsers Table
#### AspNetUser Logins

### Tips for working with database
#### Tips for PGAdmin 4
1. If you right-click on a table, you can get some premade queries under "Scripts"

