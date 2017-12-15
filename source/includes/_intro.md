# Introduction

Documentation for Royal Flying Doctor Service Application Program Interface.

# Preliminaries

## Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "host"
  -H "Authorization: Bearer jwtToken"
```

> Replace `jwtToken` with your API key.

**Unless otherwise stated**, the *Authorization* header must be provided with a value of 
*Bearer* followed by a whitespace and the token to be used. For example:

Assuming Token has a value of _jwtToken_, then the Header to be provided would be:

`Authorization: Bearer jwtToken`

<aside class="notice">
You must replace <code>jwtToken</code> with your RFDS API Token.
</aside>
## API Prefix

**Except otherwise noted**, all API endpoints must be prefixed with _/api/v1_. 
For example, to use the _/incidents_ endpoint, the request should be made to:

`$HOST/api/v1/incidents` 

where **$HOST** is the url of the server hosting the API.

## Content Type

**Unless otherwise noted**, all API requests must include the _Accept_ header with a value 
of _application/json_. All responses from the API will be valid JSON.

```shell
curl "HOST/api/v1/some/endpoint"
  -H "Authorization: Bearer token" -H "Accept: application/json"
```