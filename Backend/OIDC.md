![[Pasted image 20241226143415.png]]

- **Identity Provider (IdP)**:
    
    - The service or server that performs the authentication and provides identity information (e.g., Google, Microsoft, Okta).
- **Relying Party (RP)**:
    
    - The application or service that requests user authentication and user identity information.
- **ID Token**:
    
    - A JSON Web Token (JWT) issued by the IdP to the client after successful authentication. It contains user identity details like name, email, and an expiration timestamp.
- **Endpoints**:
    
    - **Authorization Endpoint**: Where the user logs in (e.g., `https://idp.com/auth`).
    - **Token Endpoint**: Where the app exchanges an authorization code for tokens.
    - **UserInfo Endpoint**: Provides additional user profile information.

### **OIDC Flow**

#### 1. **Authentication Request**:

- The client (app) redirects the user to the IdP for login.

#### 2. **User Authentication**:

- The IdP authenticates the user (via username/password, biometrics, etc.).

#### 3. **Token Exchange**:

- The client receives an **authorization code** from the IdP.
- The client exchanges this code for:
    - **ID Token** (for user identity).
    - **Access Token** (for API access).

#### 4. **Token Validation**:

- The client validates the ID Token to ensure it's authentic and has not expired.

#### 5. **User Info Retrieval**:

- The client optionally calls the **UserInfo endpoint** to retrieve additional user profile data.


