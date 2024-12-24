**It is a security standard, where you give one application permission to access your data in another application.**
### OAuth Flow
Resource Owner - **Me**
Client - **Any application I'm going to login**
Authorization server - **Application that knows resource owner, where resource owner already has an account**
Resource server - **The service/API the client wants to use on behalf of resource owner**
Redirect URI - **The site the Authorization server redirects the resource owner back to after granting permission to the client** / *callback url*
Response Type - **Type of information the clients expects to receive** "*mostly authorization code*"
Scope - **Granular permissions the client want**
Consent - **Authorization server takes the scopes the client is aking and verifies with the resource owner whether or not to give the client the permission**
Client ID - **This ID is used to identify the client with the authorization server**
Client Secret - **secret password/key only the client and Authorization server knows**
Authorization Code - **Authorization server sends back to the client, the client then sends the authorization code with the client secret in exchange for Access token**
Access Token - **An access token is the key the client will use, to communicate with the resource server**