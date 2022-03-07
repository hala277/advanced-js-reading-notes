# BearerAuthorization

1. What can you do with an authorization code?

*An authorization code is an alphanumeric password that allows its owner to buy, sell, or transfer products, as well as enter data into a secure area.*

2. What can you do with an access token?

*Access tokens are used by programs to make API requests on a user's behalf. The access token denotes a certain application's permission to access specified elements of a user's data.*

3. What’s a benefit of using OAuth instead of your own basic authentication?

*It allows programs to gain limited access to a user's data (scopes) without revealing the user's password. It separates authentication and authorisation and provides a variety of use cases that handle various device capabilities. Server-to-server apps, browser-based apps, mobile/native apps, and consoles are all supported.*

## Term

* Client ID:  is a unique identity for an application that aids with OAuth 2.0 client/server authentication for ArcGIS client APIs.
* Client Secret: The OAuth Client uses the Client Secret (OAuth 2.0 client secret) to authenticate with the Authorization Server.
* Endpoint authentication: is a security feature that ensures that only authorized devices can access a network, site, or service.
* Apps send requests to get an access token for a user at the token endpoint.
* Access Token Endpoint: Apps send requests to get an access token for a user at the token endpoint.
* API Endpoint: A digital location where an API receives requests concerning a certain resource on its server is known as an API endpoint.
* Authorization Code:The authorization code is a one-time use code that the client will use to obtain an access token. The code is retrieved from the authorization server, which allows the user to view the information requested by the client and approve or deny the request.
* Access Token: Access tokens are used by programs to make API queries on a user's behalf. The access token denotes a certain application's permission to access specified elements of a user's data.

## JWTs Explained
*JWT: refers to JSON Web Token*

**what is JSON Web Token?**

*JSON Web Token (JWT) is an open standard (RFC 7519) that specifies a compact and self-contained method for securely communicating information as a JSON object between two parties. Because it is digitally signed, this information can be checked and trusted.*

*JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.*

**When to use JSON Web Tokens?**

1. Authorization: The most typical case in which JWT is used is for authorization. Each subsequent request will include the JWT once the user has logged in, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a popular feature that makes use of JWT nowadays due to its low overhead and ability to be used across multiple domains.

2. Information Exchange: JSON Web Tokens are an excellent way to send information securely between parties. You can be sure the senders are who they say they are because JWTs can be signed—for example, using public/private key pairs. You may also check that the content hasn't been altered with because the signature is calculated using the header and payload.

**JSON Web Token structure:**
1. Header: *The type of token, which is JWT, and the signature technique, such as HMAC SHA256 or RSA, are often included in the header.*
2. Payload: *The payload, which contains the claims, is the second element of the token. Claims are statements and supplementary data about an entity (usually the user). Registered, public, and private claims are the three sorts of claims.*
3. Signature: *You must sign the encoded header, the encoded payload, a secret, and the procedure indicated in the header to construct the signature section.*

*JWT typically looks like this:* `xxxxx.yyyyy.zzzzz`

**How do JSON Web Tokens work?**

*When a user successfully signs in with their credentials, a JSON Web Token is returned in authentication. Because tokens are credentials, extreme caution must be exercised to avoid security risks. In general, don't store tokens for longer than necessary.Due to the lack of security, you should not save important session data in browser storage.The user agent should deliver the JWT whenever the user wishes to access a protected route or resource, often in the Authorization header using the Bearer schema.*

## Are JWTs Secure?

*JWTs can be signed, encrypted, or both at the same time. If a token is signed but not encrypted, anyone can read its contents, but you can't change it unless you know the secret key. Otherwise, the recipient will discover that the signatures are no longer identical.JWT stands for Json Web Tokens and is a fairly current, easy, and safe technique. Json Web Tokens are a stateless authentication method.*

*As a result, there's no need to retain any session data on the server, which is ideal for restful APIs. Restful APIs should always be stateless, therefore the most common alternative to utilizing JWTs for authentication is to utilize sessions to keep the user's log-in state on the server. However, it does not adhere to the idea that restful APIs should be stateless, which is why solutions like JWT have become popular and effective.So, let's have a look at how Json Web Tokens function in terms of authentication.*

*Assume we already have a person in our database who has registered. So the user's client sends a post request with the username and password, the application checks whether the user exists and if the password is correct, and then generates a unique Json Web Token for that user alone.A secret string is used to generate the token, which is kept on a server. After that, the server delivers the JWT back to the client, who stores it in a cookie or in local storage.*

*All of this communication must take place over https, which means secure encrypted Http, to ensure that no one can access passwords or Json Web Tokens. Only then will we have a system that is truly secure.*

## npm jsonwebtoken docs

**to install:**
`npm install jsonwebtoken`

### Usage:
* (Asynchronous) If a callback is supplied, the callback is called with the err or the JWT.
* Synchronous) Returns the JsonWebToken as string
* payload could be an object literal, buffer or string representing valid JSON.
* secretOrPrivateKey is a string, buffer, or object containing either the secret for HMAC algorithms or the PEM encoded private key for RSA and ECDSA. In case of a private key with passphrase an object { key, passphrase } can be used (based on crypto documentation), in this case be sure you pass the algorithm option.

### resource
* [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo) 
* [Intro to JWT](https://jwt.io/introduction/)
* [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
* [npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)




