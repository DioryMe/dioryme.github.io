# Diograph Authentication

A way to save token and API baseUrl in the localStorage where Diograph Apps can read and use them to access the Diograph Server.

```
npm install diograph-authentication

import { DiographAuthentication } from "diograph-authentication"

DiographAuthentication.token
DiographAuthentication.onLogin() = () => { }
DiographAuthentication.onLogout() = () => { }
```

## \<diograph-login> element

Authentication can be done with <diograph-login> element in two ways:

1) Using the token field and save button on app html page

2) Giving url-parameter "token" on that page where <diograph-login> exists
```
http://diory-test-app.surge.sh/login?token=test-token
```

## API

### DiographAuthentication.token
=> token used to authenticate requests

### DiographAuthentication.onLogin()
=> callback to be executed after login when token is set

### DiographAuthentication.onLogout()
=> callback to be executed after logout when token is removed
