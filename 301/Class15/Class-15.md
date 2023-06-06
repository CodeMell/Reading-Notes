# Authentication

## [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

1. What is OAuth?
    - an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential

2. Give an example of what using OAuth would look like.
    - when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon

3. How does OAuth work? What are the steps that it takes to authenticate the user?

    1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
    
    2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
    
    3. The first site gives this token and secret to the initiating user’s client software.
    
    4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
    
    5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
    
    6. The user approves (or their software silently approves) a particular transaction type at the first website.
    
    7. The user is given an approved access token (notice it’s no longer a request token).
    
    8. The user gives the approved access token to the first website.
    
    9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
    
    10. The second website lets the first website access their site on behalf of the user.
    
    11. The user sees a successfully completed transaction occurring.
    
    12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).

4. What is OpenID?
    - a single sign-in, vouching for the identities of users


## [Authorization and Authentication flows](https://auth0.com/docs/flows)

1. What is the difference between authorization and authentication?
    - authorization determines whether users are who they claim to be and authentication determines what users can and cannot access

2. What is Authorization Code Flow?
    - involves exchanging an authorization code for a token

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
    - an OpenId Connect flow specifically designed to authenticate native or mobile application users

4. What is Implicit Flow with Form Post?
    -  a browser only flow that get a access token after the Resource Owner gave access

5. What is Client Credentials Flow?
    -  used when a client application needs to authenticate itself and directly access resources on behalf of itself, rather than a specific user

6. What is Device Authorization Flow?
    - used for devices that have limited input capabilities and cannot interactively authenticate like a regular web application

7. What is Resource Owner Password Flow?
    - an OAuth flow where the client requests the user's credentials (username and password) and exchanges them directly with the authorization server for an access token, typically used for trusted applications


## Bookmark and Review
[Auth0 for single page apps](https://auth0.com/docs/libraries/auth0-react)

## Things I want to know more about
