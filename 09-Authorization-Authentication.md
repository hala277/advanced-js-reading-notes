# Authorization/Authentication

## Review, Research, and Discussion

+ What header(s) are used in authentication and authorization? 

**authorization:**
*The HTTP Authorization request header can be used to give credentials to a server that authenticates a user agent and grants access to a protected resource.*

**authentication:**
*A request has a header field in the form of Authorization: in basic HTTP authentication. Basic credentials, where credentials is the Base64 encoding of the user's ID and password, separated by a colon.*

+ What is safe to put into a JWT?

*They're suitable for usage as ID or Access Tokens, and they're safe to use because the tokens are normally signed or encrypted. Nonetheless, only the server should have access to the "secret" that is used to produce the JWT; however, this is dependent on how the token is stored. Local storage is less secure than cookies (reference), but cookies are vulnerable to CSRF and XSRF attacks.*

+ How are JWTs validated? 

*Because JWTs are signed, they can't be changed while in transit. When an authorization server creates a token, it uses a key to sign it. When a client receives an ID token, he or she must also validate the signature using a key. We should also check some registered claims. Registered Claim Names, Public Claim Names, and Private Claim Names are some of the most important registered claims.*

## Term

+ Role-based access control(RBAC):
*is a way of restricting network access based on individual users' positions within an organization. RBAC guarantees that employees only have access to the information they need to complete their jobs and keeps them from seeing material that isn't relevant to them.*

+ User Roles:
*User Roles are permission settings that control access to the Professional Archive Platform's sections and capabilities. A Role must be assigned to each User account.*

+ JWT Token:
*JSON Web Token is a proposed Internet standard for producing data with optional signatures and/or encryption, with the payload including JSON that asserts a set of assertions. A private secret or a public/private key is used to sign the tokens.*

