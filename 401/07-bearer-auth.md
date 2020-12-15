# Reading: Bearer Authorization

- [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)
- [Intro to JWT](https://jwt.io/introduction/)
- [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
- [npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)

Write the following steps in the correct order:

1. Register your application to get a client_id and client_secret
2. Ask the client if they want to sign in via a third party
3. Redirect to a third party authentication endpoint
4. Make a request to a third-party API endpoint
5. Receive authorization code
6. Make a request to the access token endpoint
7. Receive access token

[What can you do with an authorization code?](https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/#:~:text=The%20authorization%20code%20is%20a,approve%20or%20deny%20the%20request.)

  - The authorization code is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.

[What can you do with an access token?](https://auth0.com/docs/tokens/access-tokens)

  - Access tokens are used in token-based authentication to allow an application to access an API. The application receives an access token after a user successfully authenticates and authorizes access, then passes the access token as a credential when it calls the target API.

[What’s a benefit of using OAuth instead of your own basic authentication?](https://www.tutorialspoint.com/oauth2.0/oauth2.0_overview.htm)

  - It is a server side web app that uses authorization code and does not interact with user credentials.

## Vocabulary

- [Client ID](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/) - The client_id is a public identifier for apps

- [Client Secret](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/) - The client_secret is a secret known only to the application and the authorization server.

- [Authentication Endpoint](https://auth0.com/docs/protocols/protocol-oauth2) -  is used to interact with the resource owner and get the authorization to access the protected resource

- [Access Token Endpoint](https://auth0.com/docs/protocols/protocol-oauth2) - used by the application in order to get an access token or a refresh token. It is used by all flows except for the Implicit Flow because in that case an access token is issued directly.

- [API Endpoint](https://en.wikipedia.org/wiki/Web_API#Endpoints) -  they specify where resources lie that can be accessed by third party software. Usually the access is via a URI to which HTTP requests are posted, and from which the response is thus expected.

- [Authorization Code](https://oauth.net/2/grant-types/authorization-code/) - The Authorization Code grant type is used by confidential and public clients to exchange an authorization code for an access token.

- [Access Token](https://auth0.com/docs/tokens/access-tokens) - used in token-based authentication to allow an application to access an API. The application receives an access token after a user successfully authenticates and authorizes access, then passes the access token as a credential when it calls the target API.
